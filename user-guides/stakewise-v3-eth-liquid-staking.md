---
description: >-
  Similar to Lido and Rocketpool, StakeWise V3 is making a comeback enabling
  permissionless Ethereum Pooled Staking for validators such as KysenPool
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Ethereum Staking (ETH via Stakewise)

## ETH Liquid Staking <a href="#42ab" id="42ab"></a>

<figure><img src="https://cdn-images-1.medium.com/max/800/0*Rrp411ujp8p4RxJr" alt=""><figcaption></figcaption></figure>

StakeWise V3 aims to address the concerns around Ethereum’s centralization in staking services, which inherently affects Ethereum’s security. By developing a decentralized staking protocol, **StakeWise V3 now allows independent commercial node operators and solo staking operators to host ETH staking services** via a user-friendly interface.

Retail holders of ETH can freely allocate ETH to specific node operators, and make their stake liquid with osETH\* token to farm, trade and borrow other coins in DeFi, alongside collecting the staking yield. The goal is to reduce staking centralization by making solo staking more appealing and giving users more control over their node operators. Institutions and crypto exchanges can also create private mini-pools within this protocol.

{% hint style="info" %}
osETH is a liquid staked Ether token which protects holders against slashing on the StakeWise nodes with an extra buffer of staked ETH collateral.
{% endhint %}

***

## Introducing osETH

StakeWise V3 introduces osETH, a liquid ERC-20 token representing an overcollateralized staked Ether with a 1:1 peg but without passing on slashing losses to holders. osETH can be minted or traded on decentralized exchanges, and protects holders against slashing penalties that can be experienced by the nodes in StakeWise with an extra buffer of staked ETH collateral. Overcollateralization is the result of letting stakers in Vaults make only up to 90% of their capital liquid, using the remaining 10% as the extra buffer against slashing in their Vault.

This isolates the capital losses and protects osETH holders from slashing. Individual Loan-to-Value (LTV) metrics are used to maintain collateralization, and a Liquidation Threshold is set to prevent excessive risk. Liquidators can claim ETH by liquidating positions that breach the threshold, incentivized by a Liquidation Premium. Safe LTV is determined based on expected slashing losses, liquidation premium, and extra capital buffer.

StakeWise V3 is aiming to facilitate pooled staking for staking participants. Solo stakers often lack tokenization opportunities to access decentralized finance (DeFi) with their staked assets. The StakeWise V3 protocol provides an option to allow solo stakers to tokenize their stakes into osETH tokens for DeFi access and operational flexibility, while also enabling them to host validators for additional revenue.

Commercial node operators can open private or public Vaults, making staking non-custodial and reducing risks. Institutions and exchanges can create private Vaults to work with specific node operators, ensuring compliance with regulations and expanding access to liquidity and DeFi utility.

To learn more about osETH, visit the official documentation site at [https://docs-v3.stakewise.io/protocol-overview-in-depth/oseth](https://docs-v3.stakewise.io/protocol-overview-in-depth/oseth)

***

## How StakeWise V3 Vaults Work

<figure><img src="https://cdn-images-1.medium.com/max/800/0*pPl0SrAX8RKh-bGu" alt=""><figcaption></figcaption></figure>

StakeWise V3 introduces a staking system with the first layer based on Vaults, permissionless mini “pools” that receive ETH delegations. Users can choose Vaults operated by any node operator, whether they are commercial node operators or solo staker groups. Vault operators register Ethereum validators for every 32 Ether deposited, and staking rewards go to stakers in the Vaults, net of the Vault’s staking fee.

<figure><img src="https://cdn-images-1.medium.com/max/800/0*LnuRH2xZ3tStWzel" alt=""><figcaption></figcaption></figure>

Vault Operators set parameters, including staking fees, approach to capturing MEV, and Vault branding. StakeWise DAO assigns a Vault Score (under the “**Performance**” field) based on operational performance. The Vault Scoring System that aims to rank Vaults on parameters other than performance (e.g. client diversity, slashing insurance, use of DVT etc) is also in the works.

<figure><img src="https://cdn-images-1.medium.com/max/800/0*FQcLbtLNSFkVFqhJ" alt=""><figcaption></figcaption></figure>

***

## Why are there Commissions and How does it affect Stakers?

Vault Operators, or in Ethereum validator terms called Node Operators, offer their commercial and independent node operation services for a fee. These fees are in the form of commissions, to help operators pay for a range of enterprise-grade cloud services to solo staking at-home operators. There are similar terminologies used in other earlier Proof-of-Stake blockchain protocols and staking terminologies such as Cosmos, Polkadot, Cardano, etc.

As an example, let’s say you as a staker put up 100 ETH to stake via StakeWise V3 on KysenPool. And also let’s say the total rewards meets the [CESR](https://www.coindesk.com/indices/ether/cesr) average of 4.13% plus MEV rewards, it could amount towards 5 ETH for a year’s worth of staking rewards from the total 100 ETH was staked. In this example, the gross staking rewards of 5 ETH are accumulated into a splitter wallet in the vault over the course of the year, staked with KysenPool via StakeWise V3. Since KysenPool’s vault is set to a 4% commission on the 5 ETH rewards (not 100 ETH), approximately 0.2 ETH will then be split towards KysenPool vault fee recipient address while you as a staker receives approximately 4.8 ETH back to your wallet which you staked from (when you Unstake).

{% hint style="info" %}
According to CoinDesk’s [Composite Ether Staking Rate (CESR)](https://www.coindesk.com/indices/ether/cesr), the annualized staking yield for the Ethereum validator population is 4.13%, which only includes Ethereum protocol’s consensus layer rewards and transaction fees. But with StakeWise V3, there’s also MEV rewards. Plus StakeWise V3 enables compounded rewards. The net annualized staking yield could be slightly higher if the operator such as KysenPool operates with high availability.
{% endhint %}

KysenPool believes in enabling the public to make the choice in staking their ETH and we’ve limited our initial node operation service for the first 16,000 ETH (500 validators) to a low 4% commission on the rewards while offering a commercial grade staking service.

***

## Why is KysenPool on StakeWise V3?

<figure><img src="https://cdn-images-1.medium.com/max/800/0*Chsyezxc-HDPeHwr" alt=""><figcaption></figcaption></figure>

KysenPool is now expanding its offering by first enabling self-custodied ETH holders to participate in staking rewards by spinning up your own validators via [**JinOro**](https://jinoro.xyz). Now, **StakeWise V3 protocol enables exposure into a crowd-staking platform** for ETH holders with any amount of ETH to be able to participate in staking via the StakeWise V3 protocol, while receive MEV rewards shared across all stakers in KysenPool’s vault operations, as KysenPool provides a validator as a Software-as-a-Service (SaaS).

## **Stake Now with KysenPool Zen** :man\_in\_lotus\_position: on [Stakewise V3](https://app.stakewise.io/vault/0xe2d8f982708ce1e3814c8986cbab624ca926288a)

***

## Summary

StakeWise V3 and KysenPool aims to counter the centralization trend in Ethereum caused by the existing liquid staking players today, by encouraging the allocation of new Ether inflows to an independent set of commercial node operators and promoting the participation of solo operators.

The StakeWise V3 concept introduces a 2-layer architecture, allowing individuals and organizations to mint osETH, a liquid staked ETH token, without compromising the safety of the DeFi ecosystem, thanks to being able to mint osETH from any node and due to the overcollateralized nature of osETH. The goal is to garner support from the Ethereum community for StakeWise DAO in finalizing the core components of the new product.

{% hint style="danger" %}
DISCLAIMER: Before engaging in any token minting activities, it is crucial to thoroughly verify for compliance with the local laws and regulations in your jurisdiction. Token minting, especially in the context of cryptocurrencies and blockchain, may be subject to various legal considerations that vary from one region to another. Ensure that you are aware of and adhere to all relevant legal requirements to avoid any potential legal consequences. Always seek legal advice if you are uncertain about the legal implications of minting tokens in your specific location.
{% endhint %}



***

## About Us

### **🌐 KysenPool Validator**

_Unlock the Power of Staking with Our Trusted Blockchain Infrastructure Services!_

We aim to decentralize the Proof-of-Stake blockchain ecosystem. We’re highly familiar with the Tendermint-based blockchains such as **Cosmos**, Kava, Quicksilver; **Ethereum** and EVM-chains like Harmony; and substrate-based chains such as **Cardano**. Our global team is continuously improving our automations and constantly monitoring our operations to ensure high availability and resilience.

Our infrastructure is a hybrid of data centers bolstered with **Hardware Security Modules (HSMs)**, and distributed globally at multiple Cloud providers. Our mission is to help **provide a sound infrastructure, share toolings and offer foundational services**, so that token holders can stake with confidence while the blockchain ecosystems which we support continues to strengthen. We hope you like our contributions into the ecosystems that we support. To find out more about networks that we support, checkout our website below.

{% embed url="https://kysenpool.io" %}

### **Stake with KysenPool**

* on Ethereum via [JinOro](https://www.jinoro.xyz/staking) or [Stakewise V3](https://app.stakewise.io/vault/0xe2d8f982708ce1e3814c8986cbab624ca926288a)
* on Cosmos via [Keplr Wallet](https://wallet.keplr.app/chains/cosmos-hub?modal=validator\&chain=cosmoshub-4\&validator\_address=cosmosvaloper146kwpzhmleafmhtaxulfptyhnvwxzlvm87hwnm)
* on Cardano visible at [PoolTool](https://pooltool.io/pool/490353aa6b85efb28922acd9e0ee1dcf6d0c269b9f0583718b0274ba/delegators) via [AdaLite](https://adalite.io/)
* on Kava via [Keplr Wallet](https://wallet.keplr.app/chains/kava?modal=validator\&chain=kava\_2222-10\&validator\_address=kavavaloper1rpwemvmt3sex4d8qt4menglfx9rhl0x3py69wj)
* on Quicksilver via [Keplr Wallet](https://wallet.keplr.app/chains/quicksilver?modal=validator\&chain=quicksilver-2\&validator\_address=quickvaloper1s64h9vqlnrue4d9s3y0825tdes59mgg8wwezt0)
* on Aura at [AuraScan](https://aurascan.io/validators/auravaloper1se04rpyxc9tmphuq8ewr747ds77jhv48s7hl42)
* on Desmos via [Forbole X](https://medium.com/kysenpool/how-to-delegate-your-tokens-on-forbole-x-874ea383f383)
* on Harmony via [Staking Explorer](https://staking.harmony.one/validators/mainnet/one1ctwewx0pmg8k0tc8vnx4guyq9jm7dwz5k98tlm) (upon sign-in)

### **Our Dapps**

* JinOro (Ethereum self-custody staking): [https://jinoro.xyz/](https://jinoro.xyz/)
* Cosmos Outpost (Analytics):  [https://cosmosoutpost.io/](https://cosmosoutpost.io/)

### **Official Channels**

* Email: [developers@kysenpool.io](mailto:developers@kysenpool.io)
* Website: [https://kysenpool.io/](https://kysenpool.io/)
* Twitter: [https://twitter.com/kysenpool](https://twitter.com/kysenpool)
* Telegram: [https://t.me/kysenpool](https://t.me/kysenpool)
* Medium: [https://medium.com/kysenpool](https://medium.com/kysenpool)
