---
description: This page talks about the $ONEZ stablecoin launched by ZeroLend
---

# ONEZ Stablecoin

{% hint style="info" %}
$ONEZ is currently depolyed on the zkSync mainnet at [0x90059C32Eeeb1A2aa1351a58860d98855f3655aD](https://explorer.zksync.io/address/0x90059C32Eeeb1A2aa1351a58860d98855f3655aD)
{% endhint %}

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

ONEZ is a unique stablecoin created by the ZeroLend Protocol. It's designed to always be worth one U.S. Dollar and is made by users who provide collateral. When someone borrows, they must offer collateral at a certain ratio to get ONEZ.

When borrowed positions are paid back or if there's a liquidation, the ONEZ goes back to ZeroLend and is removed from circulation. What's special is that the interest paid by ONEZ users goes into the ZeroLend DAO treasury, unlike other assets where interest is essentially removed.

In a world where people want a decentralized, well-backed, and adaptable stablecoin, ONEZ fills a gap. Recent market events have shown how important decentralized stablecoins can be when markets are shaky. With ZeroLend in charge, ONEZ can become an essential part of DeFi, supported by the community.

For more details on how ONEZ works and its role, check out the ONEZ documentation, including the Technical Paper and Smart Contracts sections. Together, we're bringing stability and empowerment to decentralized finance.

## How to mint/redeem ONEZ?

ONEZ is minted and burned by the smart contracts on demand when a user borrows and repays, respectively.

In the context of ZeroLend's ecosystem, when a user provides USDC as collateral and expresses the intention to borrow ONEZ, there is no prerequisite for the user to have initially deposited ONEZ. The ZeroLend's Protocol introduces an innovative approach where the initiation of ONEZ tokens occurs dynamically, orchestrated by a direct interaction with the ONEZ contract. When it comes to the repayment of ONEZ debt, a sophisticated smart contract mechanism comes into play: ONEZ tokens are burned automatically when the repayment amount exceeds the accrued interest, rather than being returned to the suppliers.

This design yields a heightened level of adaptability compared to conventional assets within the pool. The unique aspect of ONEZ being minted as per the user's request eliminates the reliance on pre-supplied ONEZ tokens, providing users with unparalleled flexibility.

Within this framework, designated facilitators hold the authority to engage in the minting of ONEZ tokens. For a comprehensive understanding of the pivotal role that Facilitators play in the ONEZ ecosystem, please refer to the dedicated Facilitators page, where their responsibilities and contributions are elaborated upon.

## The Oracle Price for ONEZ is Firmly Anchored to 1 USD

Irrespective of prevailing market conditions, the Zerolend Protocol steadfastly values 1 ONEZ token at an equivalent of 1 USD, maintaining unwavering stability even in the face of market fluctuations.

By enforcing a fixed price, immediate avenues emerge to fortify ONEZ's peg to its target value.

For instance, when the market value of ONEZ surpasses the peg, users can mint 1 ONEZ in exchange for $1 worth of debt. This enables users to capitalize on market conditions and sell ONEZ above its nominal value, generating a surplus. This augmented supply of ONEZ contributes to a reduction in asset price. Subsequently, the minter can settle their debt at the fixed $1 value, retaining the difference from their ONEZ sale. Conversely, during periods where the market value of ONEZ dips below the peg, minters have the opportunity to procure 1 ONEZ from the market at a value lower than $1, and employ it to offset $1 worth of debt. This strategic move contracts the supply of ONEZ, inducing an escalation in asset price.

ONEZ adopts an over-collateralized model, ensuring that each ONEZ token is backed by collateral exceeding the $1 value. This proven model has demonstrated its resilience within the DeFi ecosystem over the course of several years.
