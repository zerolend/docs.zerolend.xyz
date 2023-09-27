---
description: >-
  This section explains how ZeroLend uses oracles to determine the price of
  various assets.
---

# Oracles

In the context of decentralized lending protocols like ZeroLend, an oracle is essential for fetching accurate and reliable price data of digital assets and other financial instruments. By providing this external information to the blockchain, oracles enable smart contracts to make informed decisions based on real-time market conditions, such as determining collateral values and interest rates and triggering liquidation events.

ZeroLend uses Pyth Network to ensure the trustworthiness and precision of its lending platform. Pyth Network is a decentralized oracle solution built on the Solana blockchain that sources real-time price data from trusted institutional venues, guaranteeing high-quality market feeds.&#x20;

By integrating Pyth Network into ZeroLend, the lending protocol gains access to up-to-date and reliable price information for accurate asset valuations, dynamic interest rate adjustments, and timely liquidations. This integration enhances the security and transparency of ZeroLend's lending operations, instilling confidence among users and safeguarding the integrity of the lending ecosystem.&#x20;

1. **Real-Time Asset Valuation:** As a lending protocol, ZeroLend needs up-to-date and accurate price information to determine the value of digital assets provided as collateral by borrowers. The protocol leverages the Pyth Network's decentralized oracle service to fetch real-time price data for various cryptocurrencies and other financial assets.
2. **Reliable Price Feeds:** Pyth Network sources data from reputable and trusted institutional venues, aggregating high-quality market data. ZeroLend relies on these reliable price feeds to calculate the collateral's current value, ensuring that the LTV (loan-to-value) ratio remains accurate and up-to-date.
3. **Liquidation Triggers:** To mitigate risks and protect lenders' funds, ZeroLend may implement a liquidation mechanism for under-collateralized loans. If the value of the collateral drops below a certain threshold, the protocol can automatically trigger a liquidation event. To determine when such an event should occur, ZeroLend depends on the precise and real-time price feeds provided by Pyth Network.
4. **Interest Rate Determination:** The lending protocol may use interest rates based on market dynamics. Pyth Network can supply interest rate data for various lending assets, allowing ZeroLend to adjust interest rates dynamically based on supply and demand conditions.
5. **Verification and Transparency:** Pyth Network operates on decentralized principles, allowing users of ZeroLend to independently verify the accuracy and validity of the price feeds. This transparency builds trust among users, ensuring that the lending protocol operates fairly and without any manipulation.
6. **Integration with Smart Contracts:** ZeroLend integrates Pyth Network's oracle service into its smart contracts to fetch and process the required price data. Smart contracts are programmable and self-executing, enabling the lending protocol to automate various processes based on the real-time data received from Pyth.

By utilizing Pyth Network's real-time price feeds and decentralized oracle services, ZeroLend can enhance the accuracy, transparency, and reliability of its lending platform. This integration helps create a secure and efficient lending ecosystem that benefits both borrowers and lenders while minimizing the risks associated with collateral valuation.

## Deployments

ZeroLend has taken a step further in innovation by creating Chainlink interfaces for Pyth Network, seamlessly integrating the robustness of Chainlink's oracle infrastructure with Pyth's real-time price data, ensuring a secure and reliable lending ecosystem for our users.

The source for these oracles can be found here: [https://github.com/zerolend/pyth-oracles](https://github.com/zerolend/pyth-oracles)

The deployment of the various oracles is detailed here:

| Price Feed | Address                                    |
| ---------- | ------------------------------------------ |
| USDC/USD   | 0x75D018f04f9cb37936530F7e3A909474565A2467 |
| WETH/USD   | 0x517F9cd13fE63e698d0466ad854cDba5592eeA73 |
| USDT/USD   | 0xCf58E8e67F2BcDd977e61bB6FDC1B0EEd6E1939d |
