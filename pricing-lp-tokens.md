---
description: This section explains how ZeroLend evaluates the price of various LP tokens
---

# Pricing LP Tokens

{% hint style="warning" %}
This section has been depreciated because LP Tokens are now more enabled as collateral in the protocol
{% endhint %}

For ZeroLend to accept LP tokens as collateral, a fair oracle is a crucial component to accurately determine the real-time price of these LP tokens. LP tokens represent a user's share in a liquidity pool, and their value is derived from the underlying assets in the pool, which may consist of multiple cryptocurrencies.

To determine the fair value of LP tokens, the ZeroLend leverages a fair oracle that utilizes a decentralized and tamper-resistant price feed mechanism. Here's how the oracle works:

1. Data Aggregation: The fair oracle aggregates price data from multiple reputable decentralized exchanges (DEXs) where the LP tokens are actively traded. By sourcing data from various exchanges, the fair oracle ensures a more accurate representation of the LP token's value, minimizing the influence of any single exchange's price.
2. Weighted Averaging: After gathering data from multiple sources, the fair oracle calculates a weighted average of the prices. The weighting is determined by the trading volume and liquidity of each exchange. Exchanges with higher trading volume and liquidity contribute more significantly to the final average, as they are considered to have a more substantial impact on the LP token's true market value.
3. Outlier Detection: To prevent manipulation or inaccurate data, the fair oracle employs outlier detection mechanisms. It filters out data points that significantly deviate from the majority of price data, ensuring that extreme values or anomalies do not skew the final price calculation.
4. Decentralized Governance: The fair oracle's price feed is maintained through decentralized governance mechanisms. A network of independent validators or token holders may participate in the process of updating and verifying the price data. This distributed governance model ensures transparency and reduces the risk of single points of failure or manipulation.
5. Security and Transparency: The fair oracle's smart contract is audited to ensure security and reliability. The smart contract publicly records all price data and calculations, providing transparency and accountability to users of the lending protocol.

By utilizing a fair oracle to determine the price of LP tokens, the DeFi lending protocol ensures that the collateral's value is accurately reflected in the borrowing process. This accurate valuation is crucial for maintaining the protocol's stability, managing risk, and protecting both borrowers and lenders in the lending ecosystem.
