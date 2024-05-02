---
description: >-
  This page explains how supply and borrow caps help you manage risks while
  lending/borrowing on Zerolend.
---

# Supply/Borrow Caps

<figure><img src="../../.gitbook/assets/ZL Doc - Risk Management.png" alt=""><figcaption></figcaption></figure>

In an event where one of the underlying collateral collapses faster than the risk team can possibly delist or stop the borrowing of that asset, borrow/supply caps start to play a role in limiting the possible bad debt that could occur from within collateral collapse.

Borrow/supply caps are vital for minimizing bad debt when collateral value drops faster than risk management actions. For example, if you supply collateral A and its value decreases, your collateral might be liquidated. To avoid insolvency in such cases, we add borrow caps.&#x20;

## Borrow Caps

Borrow caps define the maximum amount of an asset users can borrow on ZeroLend. It prevents excessive borrowing, especially during volatile market conditions, to avoid the risk of insolvency.

Example: If the borrowing cap for a particular asset is set at 500 units and the total borrowed amount reaches 450 units, borrowers cannot initiate new borrowings for that asset.

## Supply Caps

Supply caps define the maximum amount of an asset deposited into ZeroLend. It limits the protocol's exposure to riskier assets and prevents potential issues arising from excessive deposits.

\
Example: If the supply cap for a specific asset is set at 1,000 units and the current deposited amount reaches 900 units, users can no longer deposit that asset.

> Please note that both supply and borrow caps are optional parameters.

## Setting Caps

The default cap for supply and borrow is set at 0, indicating no supply or borrow limit. Caps can be adjusted based on on-chain liquidity and the total volume of assets in the protocol.
