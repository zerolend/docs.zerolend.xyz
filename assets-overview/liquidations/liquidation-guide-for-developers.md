---
description: >-
  This guide provides a comprehensive overview for developers looking to
  participate in the liquidation process within the ZeroLend Protocol.
---

# Liquidation Guide for Developers

Developers and traders can participate in liquidations through:

1. **Direct Calls:** Execute the `liquidationCall()` directly on the Pool or L2Pool contracts.&#x20;
2. **Automation:** Use or develop automated systems or bots designed to identify and execute profitable liquidation opportunities.

### **Profitability Considerations**

To ensure liquidation actions are profitable, consider the gas costs involved. The liquidation may not be economically feasible if the gas price is too high.

**Liquidation Details in Zerolend v3**

ZeroLend allows for up to 100% of the debt to be liquidated in a single `liquidationCall()` if the HF is below a certain threshold (CLOSE\_FACTOR\_HF\_THRESHOLD).

### **Prerequisites for Liquidation**

Before making a `liquidationCall()`, ensure you:

* Identify the user account with an HF below 1.
* Know the valid debt amount and the asset to cover (debtToCover & debtAsset).
* Understand the applicable liquidation close factor based on the HF.

### **Obtaining Liquidation Targets**

User accounts in ZeroLend are individual addresses that have interacted with the protocol. These can be either externally owned accounts or contracts. Accounts eligible for liquidation have an HF < 1. You can identify these accounts:

* **On-Chain:** Monitor protocol events and maintain an up-to-date index of user data. Use `getUserAccountData()` to check an account's current HF.
* **GraphQL:** Utilize GraphQL to gather user account data and compute health factors using Zerolend utilities or SDKs, as real-time data like HF may not be directly available.

### **Executing a Liquidation Call**

To liquidate an account, calculate the collateral that can be liquidated:

1. Retrieve user reserve data using `getUserReserveData()`.
2. Determine the maximum debt clearance allowed by the liquidation close factor.
3. Optionally, set `debtToCover` to uint(-1) to liquidate the maximum amount permitted.
4. Calculate the maximum collateral that can be liquidated based on the liquidation bonus and current asset prices.

### **Calculating Profitability vs. Gas Cost**

To assess the profitability of a liquidation, consider:

1. Collateral details (address, decimals, liquidation bonus).
2. User's collateral balance.
3. Asset prices from Zerolend's oracle using `getAssetPrice()`.
4. Maximum collateral bonus and the cost of your transaction, including gas prices and usage.
5. Your potential profit is calculated as the value of the collateral bonus minus the transaction cost.

By closely following these steps and calculations, developers can effectively contribute to the protocol's health while potentially securing a profit through successful liquidations.
