---
description: This page discusses Isolation mode, ZeroLend’s risk management feature.
---

# Isolation Mode

Isolation Mode is a risk management feature that limits the risk of volatile assets used as collateral. In our evaluation process, if an asset is identified as high risk, we activate Isolation Mode upon listing.

When an asset is listed on ZeroLend under ‘Isolation Mode,’ you can only borrow permitted stablecoins against it. Once an asset is successfully placed in the isolation mode, borrowing capabilities are limited to a specified debt ceiling. This ceiling is the maximum USD amount that can be borrowed against the respective asset as collateral, with precision up to two decimals.

The debt ceiling and limited assets to borrow against isolated assets prevent users from overborrowing and thus combat market risks.&#x20;

## Supplying in Isolated Mode

When supplying an isolated asset, users with other collateral-enabled assets can lend it for yield. However, the isolated asset cannot be utilized as collateral in this scenario.

While users can contribute isolated assets to the pool for yield generation, they are restricted from leveraging these assets as collateral within the protocol.

## Borrowing in Isolated Mode

Users can only use a specific isolated asset as collateral in isolated mode. If you have enabled collateralization for an isolated asset under the isolation mode, you cannot enable another asset as collateral until it is enabled as collateral.

## **How Can I Enter Isolation Mode?**&#x20;

To access isolation mode, follow these steps:

1. From your ZeroLend dashboard, select an isolated asset that you want to supply.
2. You'll receive a notification explaining that you are entering Isolation Mode.
3. You can deposit the isolated asset once you've successfully entered isolation mode. For a detailed walkthrough, read our step-by-step guide on [how to supply crypto assets on ZeroLend](https://docs.zerolend.xyz/tutorials/how-to-supply-on-zerolend).&#x20;
4. As discussed, you can borrow crypto assets in isolation mode. However, you can only borrow stablecoins, and the predefined debt ceiling will determine the loan amount. Read our [guide](https://docs.zerolend.xyz/tutorials/how-to-borrow-on-zerolend) on borrowing for detailed steps on how to borrow crypto on ZeroLend.&#x20;

## **How Can I Exit Isolation Mode?**&#x20;

To exit isolation mode, you must disable collateralization for the isolated asset you supplied.&#x20;

Follow these steps:

1. Click the slider button from the "Your Supplies" section to disable the isolated asset.
2. Confirm the disabled isolation mode setting.
3. You've successfully exited Isolation Mode.&#x20;
