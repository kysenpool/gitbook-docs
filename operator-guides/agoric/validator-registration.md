---
description: Sample script to register validators
---

# Validator Registration

## Register your validator

1. Make sure chain is fully synced.
2. Make sure wallet used has enough tokens for gas and self bond amount
3. `PUBKEY` can be found on same node with: `agd tendermint show-validator`

```bash
#!/bin/bash
MONIKER="🌐 KysenPool Build 🏗️"
CHAIN_ID="agoric-3"
FROM_WALLET="agoricwallet"
PUBKEY='{"@type":"/cosmos.crypto.ed25519.PubKey","key":"[YOUR PUBKEY]"}'
GAS_PRICE="0.02ubld"
NODE="tcp://127.0.0.1:26657"
HOME="[YOUR INSTALL DIRECTORY]/.agoric/"
IDENTITY="2474........6BC5"
DETAILS="Unlock the Power of Staking with Our Trusted Blockchain Infrastructure Services"
WEBSITE="[<https://www.kysenpool.io>](<https://www.kysenpool.io/>)"
[SSCONTACT="admin@kysenpool.io](mailto:SSCONTACT=%22admin@kysenpool.io)"

agd tx staking create-validator \\
--amount  1000000ubld \\
--pubkey "${PUBKEY}" \\
--moniker "${MONIKER}"  \\
--chain-id "${CHAIN_ID}" \\
--commission-rate "0.1" \\
--commission-max-rate "0.2" \\
--commission-max-change-rate "0.02" \\
--website "${WEBSITE}" \\
--security-contact "${SSCONTACT}" \\
--details "${DETAILS}" \\
--identity "${IDENTITY}" \\
--min-self-delegation "1" \\
--gas-prices ${GAS_PRICE} \\
--gas auto \\
--gas-adjustment "1.5" \\
--keyring-backend file \\
--keyring-dir "${HOME}" \\
--from "${FROM_WALLET}" \\
--home "${HOME}" \\
--node "${NODE}" \\
--broadcast-mode block \\
--yes
```

