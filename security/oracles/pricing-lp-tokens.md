---
description: This section explains how ZeroLend evaluates the price of various LP tokens
---

# Pricing LP Tokens

{% hint style="danger" %}
LP tokens are depreciated and are no longer used in the ZeroLend protocol.
{% endhint %}

In recent times, the DeFi space has witnessed vulnerabilities in protocols due to price manipulation, which can have detrimental consequences. A prominent example is the Warp Finance hack, where an attacker exploited vulnerable Uniswap LP token prices, siphoning a substantial sum of DAI for a fraction of the collateral value left in the protocol. This attack employed the classic flash loan attack vector:

1. Flash loans to influence asset prices.
2. Attack the targeted protocol.
3. Revert asset prices and repay the flash loan.

To fortify the security and reliability of ZeroLend, we understand the significance of establishing a resilient oracle system. As a result, we have implemented a solution that aims to ensure the pricing of LP tokens remains unmanipulatable, safeguarding our protocol from potential flash loan and price skew attacks. We refer to this secure pricing mechanism as the "Fair LP Price."

## **Fair LP Token Pricing**

The price of an LP token is intrinsically determined by the combined value of its underlying assets:

**LP Price** = ∑ (Asset Price \* Reserve per LP Token)

Here, only two factors influence the value of an LP token: the fair price of underlying assets (Asset Price) and the fair reserve of underlying assets per LP token (Reserve per LP Token).

However, these individual factors, Asset Price and Reserve per LP Token, may be susceptible to manipulations, particularly through flash loan attacks. To combat this vulnerability, we have devised a mechanism to calculate both Fair Asset Prices and Fair Asset Reserves.

## **Fair Asset Prices**

To obtain Fair Asset Prices on-chain, several options exist, each with its merits and limitations:

1. **Decentralized Price Oracle:** Utilizing oracles like ChainLink or Band Protocol, which support specific assets but are limited by oracle support.
2. **On-chain TWAP:** Leveraging on-chain solutions such as Uniswap's TWAP or Keep3r Network, which provide prices for assets available in Uniswap pools.
3. **Centralized Feed:** Self-feeding on-chain prices from multiple centralized sources, such as CoinGecko, CoinMarketCap, or CryptoCompare, offering a broader range of asset prices.

From these options, we can assume that we have access to Fair Asset Prices. The next challenge is deriving Fair Asset Reserves.

## **Fair Asset Reserves Solution**

The fundamental idea is to infer the reserve ratio based on the ratio of Fair Asset Prices of underlying assets. This is achieved through the following steps:

1. Retrieve the current reserves of underlying assets from on-chain sources to compute the product K (e.g., using Uniswap's `getReserves()`).
2. Calculate the Fair Price ratio (P) between underlying assets based on their Fair Asset Prices.
3. Calculate the Fair Asset Reserves using the derived Fair Price ratio, ensuring the security of the pricing mechanism.

The Fair LP Token Pricing, secured by combining Fair Asset Prices and Fair Asset Reserves, forms an unmanipulatable pricing mechanism resilient to attack vectors like flash loan attacks.

At ZeroLend, we prioritize the security and stability of our protocol. By implementing this robust oracle system, we aim to fortify our lending ecosystem, providing our users with a secure and reliable platform for their DeFi needs.
