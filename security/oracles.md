---
description: >-
  This section explains how ZeroLend uses oracles to determine the price of
  various assets.
---

# Oracles

In decentralized lending protocols like ZeroLend, an oracle is essential for fetching accurate and reliable price data of digital assets and other financial instruments.&#x20;

By providing this external information to the blockchain, oracles enable smart contracts to make informed decisions based on real-time market conditions. Oracles help determine collateral values, interest rates, and liquidation events.&#x20;

ZeroLend uses three Oracle providers to determine price feeds for various assets:

* [Pyth Network](oracles.md#using-pyth-oracles)
* [Redstone](oracles.md#using-redstone-oracles)
* Chainlink
* [API3](oracles.md#api3-oracles)

## Using PYTH Oracles

Pyth Network is a decentralized oracle solution built on the Solana blockchain that sources real-time price data from trusted institutional venues, guaranteeing high-quality market feeds.

By integrating Pyth Network into ZeroLend, the lending protocol gains access to up-to-date and reliable price information for accurate asset valuations, dynamic interest rate adjustments, and timely liquidations.&#x20;

This integration enhances the security and transparency of ZeroLend's lending operations. Integrating reliable and secure oracles like Pyth also instills confidence among users to lend/borrow on ZeroLend without worrying about asset price manipulation risks.&#x20;

### How does ZeroLend utilize Pyth?

By utilizing Pyth Network's real-time price feeds and decentralized oracle services, we enhance ZeroLend protocol's accuracy, transparency, and reliability. This integration helps create a secure and efficient lending ecosystem while minimizing the risks associated with collateral valuation.

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

***

## Using Redstone Oracles

RedStone is a multi-chain Oracle service that provides frequently updated, reliable, and diverse data feeds. ZeroLend utilizes price feeds from Redstone Oracles to calculate collateral value and liquidations.

RedStone protects all ZeroLend's markets on Zircuit, Manta, and Blast and also provides LRT feeds on ETH mainnet and Linea. You can find the exact contract addresses in RedStone Docs:

{% embed url="https://docs.redstone.finance/docs/smart-contract-devs/price-feeds" %}

### Asset-Specific Oracle Information

#### **$STONE**&#x20;

For $STONE on ZeroLend, RedStone provides oracle price feeds essential for market operations.

* Overview:[ $STONE on ZeroLend](https://app.zerolend.xyz/reserve-overview/?underlyingAsset=0xec901da9c68e90798bbbb74c11406a32a70652c3\&marketName=proto_manta_v3)
* Oracle Address:[ RedStone Oracle for $STONE](https://pacific-explorer.manta.network/address/0x36c44B353a340fbC5c7a6A0b8C56269CAC6967A3)

**$wUSDM**&#x20;

RedStone provides $wUSDM price feed for [ZeroLend's Manta Market](https://app.zerolend.xyz/?marketName=proto_manta_v3), ensuring reliable and up-to-date pricing information.

* Overview:[ $wUSDM on ZeroLend](https://app.zerolend.xyz/reserve-overview/?underlyingAsset=0xbdad407f77f44f7da6684b416b1951eca461fb07\&marketName=proto_manta_v3)
* Oracle address:[ RedStone Oracle for $wUSDM](https://pacific-explorer.manta.network/address/0x06D3ddB240A0848FF6d6952742fe814306F86356)

***

## API3 Oracles

This page talks about ZeroLend’s API3 Oracle integration.

\
dAPIs are on-chain data feeds sourced from off-chain first-party Oracle nodes owned and operated by API providers. Thanks to the first-party architecture, source transparency is realized, enabling the independent verification of whether an oracle uses multiple data sources and is thus decentralized.&#x20;

dAPIs operate in a familiar push model, meaning the price is updated on-chain according to pre-determined Oracle specifications. These are 0.25%, 0.5%, 1% and 5% update thresholds, with all Oracles having a 24hr heartbeat.

{% hint style="info" %}
You can learn more about dAPIs in the API3 documentation: [https://docs.api3.org/reference/dapis/understand/](https://docs.api3.org/reference/dapis/understand/)
{% endhint %}

### Oracles operated by API3&#x20;

API3 provides the following dAPIs for Zerolend to operate the correlating markets on the respective chain.

<table><thead><tr><th width="266">Data feed </th><th>Chain</th></tr></thead><tbody><tr><td>DAI/USD</td><td>X Layer </td></tr><tr><td>USDT/USD</td><td>X Layer </td></tr><tr><td>USDC/USD</td><td>X Layer </td></tr><tr><td>BTC/USD</td><td>X Layer </td></tr><tr><td>ETH/USD</td><td>X Layer</td></tr><tr><td>OKB/USD</td><td>X Layer </td></tr></tbody></table>

***

## Using ChainLink Oracles

ZeroLend utilizes Chainlink oracles across various networks, including Base, Linea, and Ethereum Mainnet, for accurate and decentralized asset price feeds.&#x20;

**Why Chainlink?**

Chainlink's decentralized oracle network ensures:

* Reliable and tamper-proof data.
* Seamless integration with smart contracts.
* Support for multi-chain operations is essential for ZeroLend's expanding ecosystem.

**Referencing Chainlink Developer Resources**

For developers, detailed documentation on Chainlink integration can be found here:

* [Chainlink GitHub Documentation](https://github.com/smartcontractkit/documentation?tab=readme-ov-file#referencing-chainlink-documentation)
* [Chainlink Quick Links](https://docs.chain.link/builders-quick-links)

These resources provide guidance on fetching on-chain data, deploying price feeds, and testing integrations.
