---
description: This section explain how supply and borrow caps act as protective measures.
---

# Supply/Borrow Caps

In an event where one of the underlying collateral collapses faster than the risk team can possibly delist or stop the borrowing of that asset, borrow/supply caps start to play a role in limiting the possible bad debt that could occur from within collateral collapse.

## **Borrow Caps** <a href="#borrow-caps" id="borrow-caps"></a>

Borrow caps define the maximum amount of an asset that can be borrowed from ZeroLend. It prevents excessive borrowing, especially during volatile market conditions, to avoid the risk of insolvency.

**Example:** If the borrow cap for a particular asset is set at 500 units and the total borrowed amount reaches 450 units, borrowers cannot initiate new borrowings for that asset.

## **Supply Caps** <a href="#supply-caps" id="supply-caps"></a>

Supply caps define the maximum amount of an asset that can be deposited into [ZeroLend.It](http://zerolend.it) limits the protocol's exposure to riskier assets and prevents potential issues from excessive deposits.

**Example:** If the supply cap for a specific asset is set at 1,000 units and the current deposited amount reaches 900 units, no more of that asset can be added to the protocol.

> Supply and borrow caps come into play to limit potential bad debt and protect the protocol from insolvency. Both Supply and Borrow Caps are optional parameters.

## Setting Caps

The default cap for both supply and borrow is set at 0, indicating no cap. Caps can be adjusted based on on-chain liquidity and the total volume of assets in the protocol.&#x20;
