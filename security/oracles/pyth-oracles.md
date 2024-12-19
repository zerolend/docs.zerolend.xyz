---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# PYTH Oracles

## Using PYTH Oracles

Pyth Network is a decentralized oracle solution built on the Solana blockchain that sources real-time price data from trusted institutional venues, guaranteeing high-quality market feeds.

By integrating Pyth Network into ZeroLend, the lending protocol gains access to up-to-date and reliable price information for accurate asset valuations, dynamic interest rate adjustments, and timely liquidations.&#x20;

This integration enhances the security and transparency of ZeroLend's lending operations. Integrating reliable and secure oracles like Pyth also instills confidence among users to lend/borrow on ZeroLend without worrying about asset price manipulation risks.&#x20;

### How does ZeroLend utilize Pyth?

By utilizing Pyth Network's real-time price feeds and decentralized Oracle services, we enhance ZeroLend protocol's accuracy, transparency, and reliability. This integration helps create a secure and efficient lending ecosystem while minimizing the risks associated with collateral valuation.

ZeroLed uses Pyth for major protocol operations:&#x20;

* **Real-Time Asset Valuation:** As a lending protocol, ZeroLend needs up-to-date and accurate price information to determine the value of digital assets provided as collateral by borrowers. The protocol leverages the Pyth Network's decentralized oracle service to fetch real-time price data for various cryptocurrencies and other financial assets.
* **Determining LTV:** Pyth Network sources data from reputable and trusted institutional venues, aggregating high-quality market data. ZeroLend relies on these reliable price feeds to calculate the collateral's current value, ensuring the LTV (loan-to-value) ratio remains accurate and up-to-date.
* **Liquidation Triggers:** ZeroLend has a liquidation mechanism for under-collateralized loans to mitigate risks and protect lenders' funds. The protocol can automatically trigger a liquidation event if the collateral's value drops below a certain threshold. ZeroLend uses Pyth Network’s precise and real-time price feeds to determine when the protocol should trigger liquidation.
* **Calculating Interest Rates:** The lending protocol may use interest rates based on market dynamics. Pyth Network provides interest rate data for various lending assets, allowing ZeroLend to adjust interest rates dynamically based on supply and demand conditions.
* **Verification and Transparency:** Pyth Network enables Zerolend users to independently verify the accuracy and validity of the price feeds. This transparency helps users verify if our lending protocol operates fairly and without manipulation.
* **Integration with Smart Contracts:** ZeroLend integrates Pyth Network's Oracle service into its smart contracts to fetch and process the required price data. Smart contracts are programmable and self-executing, enabling the lending protocol to automate various processes based on the real-time data received from Pyth.

### Deployments

ZeroLend has also created Chainlink interfaces for Pyth Network. It helps us seamlessly integrate the robustness of Chainlink's Oracle infrastructure with Pyth's real-time price data, ensuring a secure and reliable lending ecosystem for our users.

The source for these oracles can be found here:[ https://github.com/zerolend/pyth-oracles](https://github.com/zerolend/pyth-oracles)
