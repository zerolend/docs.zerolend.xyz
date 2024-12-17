---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Assets Listings

## Asset Listing Criteria

In a lending platform like ZeroLend, deposited collateral can be considered assets, as one can sell it to recover the loan amount. On the other hand, borrowed amounts are liabilities, as it is an obligation to repay the lender. Asset and liability tokens often differ, with borrowed tokens typically in stablecoins and collateral tokens being volatile.&#x20;

Conducting a thorough analysis before listing a token on ZeroLend is important to reduce market risks.&#x20;

ZeroLend considers a comprehensive set of criteria to evaluate the suitability of adding an asset to the lending pool, like:

* Evaluating the liquidity of the asset to ensure sufficient market depth.
* Conducting a thorough security audit to identify potential risks associated with the token's smart contract.
* Determining the appropriate collateralization ratio for the token to balance risk and ensure the safety of the lending pool.
* Supporting assets with the best risk profiles as collateral.
* Assets with oracles that can be easily manipulated are listed as single-borrow assets.
* Examining the level of community support and engagement for the token.
* New, volatile assets with lower liquidity are considered for listing in [Isolation mode](../features/capital-efficiency/isolation-mode.md) to enable supplying/borrowing for such assets.&#x20;

## Asset Types and Roles

### Collateral Assets

#### Assets deposited as loan security:

* Generally more volatile (e.g., ETH, BTC)
* Must have reliable price feeds
* Requires sufficient market liquidity

## Borrowable Assets

#### Assets available for borrowing:

* Typically stablecoins and major cryptocurrencies
* Must have deep liquidity
* Requires stable price discovery

***

## Key Evaluation Criteria

#### 1. Market Liquidity

* Minimum daily trading volume requirements
* Multiple active trading pairs
* Adequate market depth
* Consistent trading activity

#### 2. Security

* Smart contract audit reports
* Production history
* Security incident record
* Open-source verification

#### 3. Risk Parameters

* Loan-to-Value (LTV) ratio
* Liquidation threshold
* Liquidation penalty
* Market size caps

#### 4. Oracle Infrastructure

* Multiple independent price feeds
* Update frequency
* Manipulation resistance
* Backup price sources

#### 5. Community Metrics

* Active user base
* Developer activity
* Team transparency
* Token distribution

***

## Listing Categories

#### Standard Listing

* Full functionality enabled
* Multiple collateral pairs
* Standard risk parameters

#### Isolation Mode

For newer or volatile assets:

* Limited borrowing pairs
* Restricted collateral usage
* Enhanced monitoring

#### Single-Borrow Assets

For oracle-sensitive assets:

* One borrowable asset at a time
* Stricter liquidation parameters
* Enhanced security measures

## Risk Mitigation

* Regular parameter reviews
* Market cap limits
* Borrowing caps
* Emergency suspension procedures

## Governance

* Community proposal review
* Technical assessment
* Risk evaluation
* Implementation timeline

Assets must meet these criteria to ensure protocol safety and user protection. Parameters are regularly reviewed and adjusted based on market conditions.

{% hint style="info" %}
Want us to list your favorite assets? Share your suggestions on ZeroLend’s [Discord](https://discord.gg/zerolend) server.&#x20;
{% endhint %}

