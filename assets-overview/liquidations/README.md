---
description: This page explains liquidations, its bonuses, risks, and the mechanics.
---

# Liquidations

### **Introduction to Liquidations**

In the Zerolend platform, loan stability and solvency are continuously monitored through a metric known as the Health Factor. This critical ratio compares a user's collateral against the amount they have borrowed. Maintaining a Health Factor above 1 is essential for the safety of the loan. Should a user's Health Factor fall below this threshold, their loan becomes eligible for liquidation to ensure the platform's overall stability. \
\
The ZeroLend protocol defines two critical thresholds for liquidation:&#x20;

* a 50% liquidation occurs when the HF dips below 1, and&#x20;
* a 100% liquidation if the HF falls below a dynamically determined lower threshold.

### **Liquidation Bonuses and Risks**

The incentive for executing a liquidation, known as the liquidation bonus, varies with the collateral's risk profile. Higher-risk collateral results in larger bonuses for the liquidator, encouraging proactive identification and resolution of at-risk loans. ZeroLend closely monitors market trends to offer competitive liquidation bonuses, ensuring alignment with the protocol's risk management framework.

### **Liquidation Mechanics**

To initiate a liquidation, the following inputs are required:

1. **User's Wallet Address:** Must have a Health Factor below 1.
2. **Debt Coverage Amount:** The amount of debt the liquidator intends to cover.
3. **Debt Asset:** Must have a sufficient quantity of the asset, with flash loans playing a crucial role.
4. **Collateral Asset:** Initially provided by the user.
5. **Profit Asset:** Chosen by the liquidator, either in Zerolend's native tokens or the underlying asset.

### **Monitoring Loan Health**

Two pivotal metrics, the Loan-to-Value (LtV) ratio and the liquidation threshold, assist in tracking loan health. The LtV ratio defines the maximum borrowing capacity against specific collateral, while the liquidation threshold marks the point at which a loan is considered under-collateralized and at risk of liquidation.

### **Executing a Liquidation**

Liquidation is a multistep process that can be automated using bots. It involves:

* Verifying the user's low Health Factor.
* Assessing the profitability of the liquidation, considering transaction fees and bonuses.
* Utilizing flash loans if needed.
* Executing necessary collateral swaps.
* Completing the liquidation process.

\
