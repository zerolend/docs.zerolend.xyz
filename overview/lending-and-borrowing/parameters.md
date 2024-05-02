---
description: This page talks about important parameters related to DeFi Lending/Borrowing
---

# Parameters

### **Max LTV (Loan to Value)**

Maximum LTV indicates the maximum amount you can borrow against your deposited collateral. For instance, $WETH has an 80% LTV on ZeroLend's Linea Market. Here, you can borrow 0.8 $WETH for every $WETH you deposit as collateral on ZeroLend.&#x20;

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

### **Liquidation Threshold**

The liquidation threshold is the value at which your loan becomes undercollateralized and is at risk of liquidation. On ZeroLend's Linea Market, the liquidation threshold for $WETH loans is 82.50%. This means if your $WETH debt value becomes worth 82.50% of your deposited collateral, the protocol can sell the collateral to pay back the loan.

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

### **Liquidation Penalty**

&#x20;If your deposited collateral is liquidated, a liquidation penalty will be added to your loan amount. If you borrow a loan on ZeroLend and your collateral is liquidated, you pay a 5% liquidation penalty.&#x20;

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>



### **Utilization Rate**

This is the percentage of funds currently being borrowed compared to the total funds available. For example, a utilization rate of 82.34% means that out of all the funds available to be lent out, 82.34% are currently borrowed by users. This rate can affect the interest rates charged on the loans. The higher the utilization rate, the higher the interest rates, as the demand for the funds is higher relative to the supply.

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

### **Health Factor**

The health factor indicates the liquidation risk. A health factor above 1 means you are not at immediate liquidation risk. If the health factor falls below 1, the loan is undercollateralized and may be liquidated. You can check your loan's health factor under your ZeroLend 'Dashboard.'

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>



