---
description: This page discusses Isolation mode, ZeroLend’s risk management feature.
---

# Isolation Mode

Isolation Mode limits risk when volatile assets are used as collateral on ZeroLend. Assets identified as high risk enter Isolation Mode upon listing, restricting borrowing to specific stablecoins and enforcing a debt ceiling—the maximum USD amount that can be borrowed against the asset, precise to two decimal places.

### **Supplying in Isolation Mode**

Users can supply isolated assets for yield, but these assets cannot serve as collateral if other collateral-enabled assets are in the account.

### **Borrowing in Isolation Mode**

If an isolated asset is used as collateral, no additional assets can be enabled as collateral until isolation is removed, ensuring borrowing limits are maintained within the protocol's risk parameters.

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
