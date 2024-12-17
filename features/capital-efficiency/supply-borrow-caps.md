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

Borrow caps limit the maximum amount of each asset that can be borrowed, protecting against over-leverage during market volatility. For instance, if a cap is 500 units and 450 are borrowed, new borrowing is halted at 500 units.

## Supply Caps

Supply caps limit the maximum deposit for each asset, reducing exposure to riskier assets. For example, with a 1,000-unit cap, users can’t deposit beyond this threshold.

> Default caps are 0, indicating no restrictions, and are adjusted based on liquidity and total asset volume within the protocol.

## Setting Caps

The default cap for supply and borrow is set at 0, indicating no supply or borrow limit. Caps can be adjusted based on on-chain liquidity and the total volume of assets in the protocol.
