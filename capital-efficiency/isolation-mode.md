---
description: This page talks Isolation mode for risk management.
---

# Isolation Mode

Isolation Mode is a risk management feature that limits the risk of new assets used as collateral. In our evaluation process, if an asset is identified as high risk, we activate Isolation Mode upon listing. When an asset is listed on ZeroLend under Isolation Mode, it can only borrow stablecoins that we have permissioned.

Once an asset is successfully placed in Isolation Mode, borrowing capabilities are limited to a specified debt ceiling. This ceiling is defined as the maximum amount in USD that can be borrowed against the user's collateral, with precision up to two decimals.

## Supplying in Isolated Mode

When supplying an Isolated Asset, users with other collateral-enabled assets can lend the Isolated Asset for yield. However, it's important to note that in this scenario, the Isolated Asset cannot be utilized as collateral.

In essence, while users can contribute Isolated Assets to the pool for yield generation, they are restricted from leveraging these assets as collateral within the system.

## Borrowing in Isolated Mode

In Isolated Mode borrowing, users can only use a specific Isolated Asset as collateral and borrow assets allowed in Isolation Mode. No other assets, including other Isolated Assets, can be enabled as collateral.

## **How Can I Enter Isolation Mode?**&#x20;

To access Isolation Mode, follow these steps:

* From the dashboard, select an isolated asset that you want to supply.
* You'll receive an information notification explaining that you are entering Isolation Mode.
* Once you've successfully entered Isolation Mode, you can proceed to supply the isolated asset.
* Borrowing assets is also possible while in Isolation Mode. However, you can only borrow stablecoins; your borrowing limit is subject to the predefined debt ceiling.

## **How Can I Exit Isolation Mode?**&#x20;

To exit Isolation Mode, you need to disable the collateralized isolated asset you supplied. Follow these steps:

* Click the slider button from the "Your Supplies" section to disable the isolated asset.
* Confirm the disabled Isolation Mode setting.
* Congratulations, you've successfully exited Isolation Mode.\
