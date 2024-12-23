---
description: This page talks about important parameters related to DeFi Lending/Borrowing
---

# Parameters

### **Max LTV (Loan to Value)**

The Loan to Value ratio represents the maximum amount you can borrow against your collateral. It's expressed as a percentage of the collateral's value.

For instance, $WETH has an 80% LTV on ZeroLend's Linea Market. Here, you can borrow 0.8 $WETH for every $WETH you deposit as collateral on ZeroLend.&#x20;

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

#### How LTV Works:

* If an asset has an LTV of 75%, you can borrow up to 75% of your collateral's value
* Example: With $10,000 worth of ETH as collateral at 75% LTV:
  * Maximum borrowing capacity = $10,000 × 75% = $7,500
* Different assets have different LTV ratios based on their volatility and risk profile
* Stablecoins typically have higher LTVs than volatile assets

#### Formula

$$
LTV = (Borrowed Amount / Collateral Value) × 100%
$$

## Utilization Rate

Measures how much available capital in a lending pool is currently being borrowed.

<figure><img src="../../.gitbook/assets/Utilisation.png" alt=""><figcaption></figcaption></figure>

$$
Utilization Rate = (Total Borrowed / Total Available) × 100%'
$$

### Impact on Protocol:

* Influences interest rates dynamically
* Higher utilization → Higher interest rates
* Optimal utilization target: 80%

{% hint style="info" %}
The interest rate model adjusts to maintain balanced utilization
{% endhint %}

### Interest Rate Correlation:

* Low utilization (<80%): Gradual APY increase
* High utilization (>80%): Steep APY increase to encourage repayments
* Maximum utilization (>95%): Emergency APY levels

## **Health Factor**

The health factor indicates the liquidation risk. A health factor above 1 means you are not at immediate liquidation risk. If the health factor falls below 1, the loan is undercollateralized and may be liquidated. You can check your loan's health factor under your ZeroLend 'Dashboard.'

<figure><img src="../../.gitbook/assets/image (1) (3).png" alt=""><figcaption></figcaption></figure>

#### Formula:

$$
Health Factor = (Collateral Value × Liquidation Threshold) / Total Borrowed Value
$$

### Health Factor Interpretation:

* Health Factor > 1: Position is safe
* Health Factor = 1: Position at liquidation point
* Health Factor < 1: Position can be liquidated

#### Example Health Factor Calculation:

```
Scenario:
- Collateral: $10,000 ETH
- Liquidation Threshold: 82%
- Borrowed: $7,000 USDC

Health Factor = ($10,000 × 82%) / $7,000 = 1.17
```

***

## Liquidation Threshold

The Liquidation Threshold is the percentage at which your position becomes eligible for liquidation. It's always higher than the LTV to provide a safety buffer.

<figure><img src="../../.gitbook/assets/Liquidation threshold.webp" alt=""><figcaption></figcaption></figure>

#### **Key Points:**

Represents the maximum ratio of the borrowed amount to collateral before liquidationCreates a safety margin between maximum borrowing capacity and liquidation point&#x20;

* Example: If ETH has:
  * LTV: 75%
  * Liquidation Threshold: 82% This creates a 7% buffer zone between maximum borrowing and liquidation

#### **Safety Buffer Calculation:**

```
Safety Buffer = Liquidation Threshold - LTV
```

#### Important Aspects:

* Typically ranges from 5% to 15% depending on asset risk
* Applied to the portion of the position being liquidated
* Covers protocol risks and incentivizes liquidators

#### Example:

* Borrowed Amount: $1,000
* Liquidation Penalty: 10%
* During liquidation, the borrower loses:

```
Additional Cost = $1,000 × 10% = $100
Total Liquidation Cost = $1,000 + $100 = $1,100
```

***

## **Liquidation Penalty**

A fee charged during liquidation events, added to the amount that needs to be repaid.

![](https://docs.zerolend.xyz/~gitbook/image?url=https%3A%2F%2F2402583484-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252Fi9DDwWcSwiiTEJZZlm8R%252Fuploads%252FnIJd7CyzRyhDmdh0FSaS%252Fimage.png%3Falt%3Dmedia%26token%3D474313bb-2486-47fb-a07c-33159dc0a1c1\&width=768\&dpr=4\&quality=100\&sign=268f5fe4\&sv=1)

### **Important Aspects:**

* Typically ranges from 5% to 15% depending on asset risk
* Applied to the portion of the position being liquidated
* Covers protocol risks and incentivizes liquidators

**Example:**

* Borrowed Amount: $1,000
* Liquidation Penalty: 10% During liquidation, the borrower loses:

```
Additional Cost = $1,000 × 10% = $100 Total Liquidation Cost = $1,000 + $100 = $1,100
```

## Liquidation Process

<figure><img src="../../.gitbook/assets/Liquidation Penalty.webp" alt=""><figcaption></figcaption></figure>

### How Liquidation Works

1. The position becomes eligible for liquidation when Health Factor < 1
2. Liquidators can repay part or all of the borrowed amount
3. Liquidators receive collateral at a discount (Liquidation Penalty)
4. Original borrower loses collateral equal to:

```
Lost Collateral = (Repaid Amount × (1 + Liquidation Penalty)) / Collateral Price
```

***

## Risk Management Guidelines

### Maintaining a Safe Position

1. **Monitor Health Factor:**
   * Recommended: Keep Health Factor > 1.5
   * Critical Zone: Health Factor < 1.2
   * Danger Zone: Health Factor < 1.1
2. **Risk Mitigation Strategies:**
   * Maintain lower LTV than the maximum allowed
   * Diversify collateral types
   * Set up Health Factor alerts
   * Keep additional collateral ready
3. **Actions to Improve Health Factor:**
   * Repay part of the borrowed amount
   * Add more collateral
   * Swap to more stable collateral assets

## Avoiding Liquidation

1. **Proactive Monitoring:**
   * Regular Health Factor checks
   * Price movement alerts
   * Market volatility awareness
2. **Safety Buffers:**
   * Maintain Health Factor > 1.5
   * Keep emergency funds available
   * Use stablecoins for lower volatility
3. **Emergency Actions:**
   * Flash loan options for quick repayment
   * Collateral swaps to stable assets
   * Partial position closure
