---
description: >-
  How-To guide to migrate Ethereum validator account keys from a source server
  host to a destination host
---

# Validator Migration

This validator migration guide is a rudimentary example of migrating **validator accounts** (also known as **keys**), from one server hosting (or running) an ETH2 validator client, to a new destination server.  These practices are commonly useful as an exercise to migrate out from degrading servers, rebalancing a server hosting too many validator accounts, for disaster recovery (DR) exercises during DDoS events, or when a server is deemed compromised.

In this example, the validator ETH2 client example uses Prysm.  Validator accounts are private keys stored within a server which is hosting the ETH2 client.  You may find more details at the official reference document of Prysm at [https://docs.prylabs.network/docs/advanced/migrating-keys](https://docs.prylabs.network/docs/advanced/migrating-keys)

This operator guide is a public service to the Ethereum community.  If you have any questions, please feel free to reach out to us at **devops@kysenpool.io**

## Step 1: Export Slashing Protection history

:warning: This is highly recommended :warning: -- to export the JSON blob containing all the historical attestations (and block proposals) for all the validator accounts to be migrated from the ETH client node that have been performed in the history of the ETH2 Proof-of-Stake's chain history.

```
prysm.sh validator slashing-protection-history export \
    --datadir=</path/to/your/validator/db>
    --slashing-protection-export-dir=</path/to/export/dir>
```

{% hint style="info" %}
You can optionally shutdown and remove the validator in question.  Best to review the status of Beaconchain validator or monitor the [beaconcha.in](https://goerli.beaconcha.in/validator/84ab067326b6631ef7eeff6c53452c0ea8f2d463d03e1d760bef530fff1e9e3d0a958b98a29ed452c63a65f465784c0b) dashboard with the validator address(es).
{% endhint %}

## Step 2: Backup Validator accounts

You'll want to backup your validator accounts to be then migrated to the new server.

```
./prysm.sh validator accounts backup
```

Follow the prompts by entering a wallet password (if any) to unlock your validator account database and select the accounts to backup.  Towards the end, you'll be prompted for a password to encrypt the backup file.  We recommend you to add a password for the backup file.  You'll now receive `keystore-file` JSON blobs containing the encrypted validator accounts.

## Step 3: Shutdown the Validator node

You can go ahead and shutdown the service (and the node).  Assuming you have a `systemd` setup to run Prysm client called `prysmvalidator.service` like this

```
[Unit]
Description=Prysm Beacon chain daemon
After=network-online.target

[Service]
ExecStart=/home/prysm/prysm.sh beacon-chain
Restart=on-failure
User=prysm

[Install]
WantedBy=default.target
```

If this is a full migration, you should stop the validator from running

```
sudo systemctl stop prysmvalidator.service
```

You should then check for server processes to see whether Prysm is still operating.  Best yet, delete the validator db directory, and shutdown the entire node itself.

{% hint style="danger" %}
DO NOT issue the [exit validator](https://docs.prylabs.network/docs/wallet/exiting-a-validator) command as you place your validators into the exit queue instead, and you'll not be able to earn any attestation or block production rewards even when you've imported it in the destination node.
{% endhint %}

## Step 4: Delete Validator(s) from your ETH2 client

Run the delete command below, as with Prysm's use case below.  Select the validator keys you'd like to remove, if you have more than one list.

```bash
./prysm.sh validator accounts delete
```

{% hint style="info" %}
This deletion is to remove the validator from your server's validator database only.  This does not exit the validators of interest from the Beacon chain.
{% endhint %}

After deletion is completed, verify account deletion again:

```bash
./prysm.sh validator accounts list
```

The validators that are being migrated should be gone from the account list.

{% hint style="success" %}
Common rule of thumb to be safe, is to start import process on the destination validator node after 2 missed attestations.
{% endhint %}

## Step 5: Import Slashing protection data

Over at the destination server to migrate into, assuming you have set up the server with the ETH1 client and ETH2 Prysm client to your satisfaction including the slashing protection file and the validator database files copied over to the new server, you should **first and foremost above all else** import the slashing protection data.

```
./prysm.sh validator slashing-protection-history import \
    --datadir=</path/to/your/validator/db> \
    --slashing-protection-json-file=</path/to/slashing-protection/json>
```

Verify that the slashing protection is available

## Step 6: Import Validator accounts

Now that the slashing protection history is imported to your ETH2 client, you can now import validator accounts of interest to the new ETH2 client node

```bash
./prysm.sh validator accounts import \
    --keys-dir=</path/to/keystore-file.json>
```

Monitor the Prysm client to look for `Validator activated` keyword in the service journal

```bash
# Follow the system journals for the Prysm service, from the last 100 lines
sudo journalctl -u prysmvalidator.service -f -n100
```

For additional verification, use the [Beaconcha.in](https://beaconcha.in/) service, to see whether your validator account(s) are now attesting properly without incurring any slashing penalties.



:clap: Congratulations, you have now successfully completed the migration of validator accounts to your new node.

***

## Notes from KysenPool Engineering

We have tested and ran more than a dozen permutations of ETH1 and ETH2 client combinations.  Managing validator accounts via ETH2 clients are a common practice but we prefer using external signers such as [Web3Signer](https://github.com/ConsenSys/web3signer), an open-source remote signing service by Consensys (the Prysm team also [mentions this here](https://docs.prylabs.network/docs/wallet/web3signer)).

We take security seriously.  Storing validator account keys on ETH2 client nodes are not desirable but may be slightly more performant.  We prefer to script our key management in order to reach an immutable infrastructure framework, to easily tear down and stand up nodes, and migrating validator accounts safely and securely across data centers.

We have also looked at a **slashing protection implementation using TEEs** (Trusted Execution Environments).  We disagree with associating validator account keys with TEEs to sign for attestations and block proposals.  If the **dependent hardware degrades** then there is no way but to **exit all validators** created under a TEE.  If there is a way to migrate out the same TEE created accounts into a new environment, **this defeats the whole purpose of slashing protection**.  This would mean a loss in customer earning potentials reducing their staking APY by 10% or more due to the entrance and exit queue wait times.  Hence **we have our reservations about using TEEs** as a slashing protection mechanism.

{% hint style="info" %}
KysenPool operates a Hardware Security Module (HSM) to [validate for the Cosmos Hub](../../user-guides/cosmos-staking-atom.md).  There are significant [differences between HSM and TEEs](https://autocrypt.io/hsm-tee-closer-look-at-vehicle-cybersecurity/), and the HSM model may in the future fit for Ethereum as long as the encryption models are using the [same BLS signature scheme](https://ethereum.org/nb/developers/docs/consensus-mechanisms/pos/keys/) in its [elliptical curve cryptography](https://en.wikipedia.org/wiki/Elliptic-curve\_cryptography).
{% endhint %}

This operator guide is a public service to the Ethereum community.  If you have any questions, please feel free to reach out to us at **devops@kysenpool.io**
