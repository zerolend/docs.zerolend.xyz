---
description: This page talks about the $ONEZ stablecoin launched by ZeroLend
---

# ONEZ

ONEZ is the pioneering decentralized, overcollateralized stablecoin native to the ZeroLend Protocol. ONEZ, pronounced "one-zee," stands as a groundbreaking stablecoin that finds its genesis within the assets contributed to the ZeroLend Protocol. Designed to be aligned with the value of the U.S. Dollar, ONEZ maintains its peg through efficient market mechanisms.

Functioning as an zkSync decentralized stablecoin, ONEZ is minted through active participation of users. Just as with any borrowing activity within the ZeroLend Protocol, individuals are required to provide collateral at a specified ratio in order to generate ONEZ.&#x20;

In parallel fashion, repayment of a borrowed position or any liquidation event results in the ONEZ being returned to the ZeroLend pool and subsequently burned. Unique to the ecosystem, the interest payments garnered by ONEZ minters will directly contribute to the ZeroLend DAO treasury.&#x20;

This stands in contrast to the conventional reserve factor collection in the case of other borrowed assets, where principal is effectively burned.

In a landscape yearning for a truly decentralized, overcollateralized, and adaptable stablecoin, the demand for ONEZ has never been more evident. Recent market events underscore the role of decentralized stablecoins in preserving value amidst market turmoil. With governance vested in ZeroLend, ONEZ holds the potential to become an indispensable element within the burgeoning DeFi sphere, further fueled by the unwavering support of the community.

Delve into the comprehensive ONEZ documentation to grasp its inner workings and the pivotal role it plays within the broader ecosystem. Detailed insights can be found in the Technical Paper and Smart Contracts sections, offering invaluable guidance for seamless ONEZ integration. Together, we usher in a new era of stability and empowerment within the decentralized financial landscape.

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
