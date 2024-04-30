---
description: This page talks in detail about ZeroLend’s lending protocol.
---

# Decentralized Lending

ZeroLend's core product is its decentralized non-custodial liquidity market. It is a fork of[ AAVE V3](https://aave.com/) with different incentive mechanisms that make it similar to [Radiant Capital](https://radiant.capital/).

## How does lending work in TradFi?      &#x20;

TradFi loans are not inclusive and permissionless, as intermediaries like banks and credit agencies manage user data and dictate loan terms. Unlike DeFi, where you can get a loan within a few seconds, securing a massive loan in traditional banking involves lengthy approval processes.&#x20;

## How is ZeroLend different from TradFi lending?

ZeroLend introduces a permissionless lending protocol where users can lend/borrow in a trustless manner regardless of their financial or geographical background.&#x20;

With ZeroLend, you can connect your wallet, deposit the required collateral, and instantly get the loan amount in your wallet. We don’t have lengthy paperwork or take weeks to approve loans selectively.     &#x20;

Unlike traditional banking, you earn incentives to supply and borrow crypto assets on ZeroLend. Our users get competitive supply and borrow APY, ecosystem points, and points from our partner projects.&#x20;

In the future, we will also introduce self-repaying loans with $ONEZ, where your loan amount is paid from the investment returns the protocol earns from your collateral. Read [$ONEZ documentation](https://docs.onez.cash/) to learn more.&#x20;

## Leverage market opportunities with DeFi loans on ZeroLend

<figure><img src="../.gitbook/assets/ZL Doc - Lending Compared.png" alt=""><figcaption></figcaption></figure>

Crypto is an opportunity-cost market, which makes it important to use your capital efficiently. With DeFi loans, you can leverage to hold multiple tokens against the same collateral.\
\
Let's understand this with an example.\
\
Suppose you're an $ETH investor who believes in the long-term potential of ETH-based tokens. Instead of holding $ETH in your wallet, you can deposit it as collateral on ZeroLend and borrow $USDT to buy other tokens in the $ETH ecosystem. Of course, all of this comes with the added risk of leverage. However, if you manage your positions well, you can combat this risk and multiply your yields. \




## The Basics of ZeroLend

<figure><img src="../.gitbook/assets/ZL Doc - Lending Borrowing.png" alt=""><figcaption></figcaption></figure>

* [Lend crypto on Zerolend](https://docs.zerolend.xyz/tutorials/how-to-supply-on-zerolend) and earn lending interest + rewards from partner projects.
* [Borrow crypto on ZeroLend](https://docs.zerolend.xyz/tutorials/how-to-borrow-on-zerolend) and earn borrow APY + rewards from partner projects.&#x20;
* In case of liquidation, you only pay a 5% flat penalty fee (no hidden charges). &#x20;

## The Advanced Features of ZeroLend

ZeroLend offers advanced features such as:&#x20;

* [High-efficiency mode](https://docs.zerolend.xyz/capital-efficiency/high-efficiency-mode-e-mode): This mode helps users increase their collateralization power by supplying collateral from the same category. For example, if you borrow another stablecoin against your deposited stablecoin, your borrowing capacity increases. &#x20;
* [Isolation mode:](https://docs.zerolend.xyz/capital-efficiency/isolation-mode) Under isolation mode, ZeroLend adds a risk ceiling on some volatile or new assets to help users combat market risks.&#x20;
* [Credit delegation](https://docs.zerolend.xyz/capital-efficiency/credit-delegation): With credit delegation, depositors can delegate their borrowing power to others to earn additional yield.&#x20;

## Important parameters for DeFi Lending

If you are new to DeFi lending/borrowing, you must understand these parameters:

### **Max LTV (Loan to Value)**

Maximum LTV indicates the maximum amount you can borrow against your deposited collateral. For instance, $WETH has an 80% LTV on ZeroLend's Linea Market. Here, you can borrow 0.8 $WETH for every $WETH you deposit as collateral on ZeroLend.&#x20;

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

### **Liquidation Threshold**

The liquidation threshold is the value at which your loan becomes undercollateralized and is at risk of liquidation. On ZeroLend's Linea Market, the liquidation threshold for $WETH loans is 82.50%. This means if your $WETH debt value becomes worth 82.50% of your deposited collateral, the protocol can sell the collateral to pay back the loan.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

### **Liquidation Penalty**

&#x20;If your deposited collateral is liquidated, a liquidation penalty will be added to your loan amount. If you borrow a loan on ZeroLend and your collateral is liquidated, you pay a 5% liquidation penalty.&#x20;

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

### **Utilization Rate**

This is the percentage of funds currently being borrowed compared to the total funds available. For example, a utilization rate of 82.34% means that out of all the funds available to be lent out, 82.34% are currently borrowed by users. This rate can affect the interest rates charged on the loans. The higher the utilization rate, the higher the interest rates, as the demand for the funds is higher relative to the supply.

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

### **Health Factor**

The health factor indicates the liquidation risk. A health factor above 1 means you are not at immediate liquidation risk. If the health factor falls below 1, the loan is undercollateralized and may be liquidated. You can check your loan's health factor under your ZeroLend 'Dashboard.'

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
