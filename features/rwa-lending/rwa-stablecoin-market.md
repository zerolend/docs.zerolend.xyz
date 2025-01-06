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

# RWA Stablecoin Market

The **RWA Stablecoin Market** on ZeroLend allows users to lend and borrow **real-world-asset (RWA) backed** stablecoins. These stablecoins are typically pegged to fiat currencies (e.g., USD) and backed by tokenized collateral—such as government bonds, cash equivalents, or other traditional financial instruments—held in reserve.

#### Key Characteristics

* **High Loan-to-Value (LTV) Ratios**: RWA stablecoins often allow higher LTV ratios because they are backed by tangible assets.
* **Competitive Yield Opportunities**: Users supplying RWA stablecoins can receive APYs based on market demand, as well as any partner rewards or incentives.
* **Reduced Volatility**: Because they are pegged to real-world reserves, most RWA stablecoins are designed to maintain price stability (e.g., 1:1 to USD).

***

### Supported Assets

Below is an illustrative list of **RWA stablecoins** in the market. Actual availability may vary over time:

<table><thead><tr><th>Asset Name</th><th>Symbol</th><th data-hidden>Typical Backing</th></tr></thead><tbody><tr><td><strong>USD Coin</strong></td><td>USDC</td><td>USD Reserves</td></tr><tr><td><strong>Tether</strong></td><td>USDT</td><td>Cash, Cash Equivalents</td></tr><tr><td><strong>ether.fi USD</strong></td><td>eUSD</td><td>ETH Staking + RWA Reserves</td></tr><tr><td><strong>Staked USDe</strong></td><td>USDe</td><td>Treasury + DeFi Strategies</td></tr><tr><td><strong>Usual USD</strong></td><td>USUD</td><td>USD Reserves</td></tr><tr><td><strong>USDO Liquid Bond</strong></td><td>USDO++</td><td>US Treasuries</td></tr><tr><td><strong>USDS Stablecoin</strong></td><td>USDS</td><td>Fiat Reserves</td></tr><tr><td><strong>ZAI Stablecoin</strong></td><td>ZAI</td><td>Various RWAs</td></tr><tr><td><strong>YieldFi Stable Token</strong></td><td>yUSD</td><td>USD Treasuries + Yield Instruments</td></tr><tr><td><strong>Syrup USDC</strong></td><td>Syrup USDC</td><td>USDC + Additional Yield</td></tr><tr><td><strong>PT Ethena sUSDe 27MAR2025</strong></td><td>PT-sUSDe</td><td>Fixed-term RWA instrument</td></tr></tbody></table>

{% hint style="info" %}
The above list is static and needs manual updating. Always check our [RWA Stablecoin Markets](https://app.zerolend.xyz/?marketName=proto_mainnet_rwa_v3) to confirm which stablecoins are currently supported.
{% endhint %}

***

### Lending (Supplying) RWA Stablecoins

1. **Navigate to the RWA Stablecoin Market**
   * Go to [https://app.zerolend.xyz](https://app.zerolend.xyz) and select **“RWA Stablecoins Market”** in the market dropdown.
2. **Choose a Stablecoin**
   * Review the available RWA stablecoins to see their supply APY and any additional reward icons (e.g., partner tokens, Zero Gravity Points).
3. **Supply Your Tokens**
   * Click **“Details”** to open the asset-specific page.
   * Enter the amount of the chosen stablecoin you want to supply.
   * Confirm the transaction via your connected wallet.
4. **View Earned Rewards**
   * Once supplied, track your APY in real-time within the ZeroLend interface.
   * Some assets may have extra incentives or rewards (e.g., from Merkle, Pendle PT, or $ZERO boosts).

#### Redeeming Your Supplied Tokens

* At any time, you can withdraw supplied stablecoins by selecting **“Withdraw”** on the asset’s page.
* Ensure any outstanding debts or other constraints (like lockup periods on partner tokens) have been addressed.

***

### Borrowing RWA Stablecoins

1. **Collateral Setup**
   * Before borrowing, deposit a supported collateral asset (which can be a crypto token or another RWA stablecoin) into ZeroLend.
   * Review the **health factor** or **collateral ratio** associated with each asset.
2. **Select an RWA Stablecoin to Borrow**
   * In the **RWA Stablecoins Market**, click **“Details”** next to the stablecoin you wish to borrow.
   * The Borrow APY, maximum borrow limit, and any additional terms will be displayed.
3. **Execute Borrow Transaction**
   * Enter the desired borrow amount (up to your limit).
   * Confirm the transaction via your connected wallet.
4. **Manage Your Position**
   * Monitor the health factor to avoid liquidation if your collateral value fluctuates.

#### Repaying Borrowed Amount

* Go to the same stablecoin’s **“Details”** page to repay the borrowed amount.
* After repayment, your collateral is unlocked (assuming no other outstanding debts).

***

### RWA Stablecoin Market Benefits

1. **Stable Value**
   * RWA stablecoins are designed to maintain value relative to real-world assets (often $1), helping to reduce volatility.
2. **Diverse Backing**
   * Assets may be backed by Treasuries, fiat, or a combination of yield-generating strategies, providing a variety of risk profiles.
3. **Potential for Higher Yields**
   * Certain RWA stablecoins integrate with yield protocols or partner reward systems, offering more competitive returns than standard stablecoins.
4. **Flexible Borrowing Options**
   * Higher LTV ratios may be possible if the stablecoin’s backing is considered lower risk, giving borrowers more flexibility than in crypto-only markets.

***

### Risk Considerations

* **Collateral Liquidation**: If the value of your collateral drops or if borrow APYs become unfavorable, a liquidation event may occur.
* **Backing Transparency**: RWA stablecoins rely on verifiable real-world reserves. It is recommended to review the documentation of each stablecoin issuer to understand audits, reserve holdings, or redemption processes.
* **Smart Contract Vulnerabilities**: All lending interactions involve smart contracts. While ZeroLend employs security audits, no system is entirely risk-free.

***

### Getting Started

1. **Connect Your Wallet**
   * Use any supported wallet (e.g., MetaMask) at [https://app.zerolend.xyz](https://app.zerolend.xyz).
2. **Review Market Details**
   * Check the RWA Stablecoins Market for APYs, borrowing rates, and any active incentive programs.
3. **Approve & Execute Transactions**
   * When supplying or borrowing, grant approval for the stablecoin in your wallet, then finalize the transaction.
4. **Manage Ongoing Positions**
   * Periodically review your supply/borrow positions. Adjust based on updated APYs, collateral ratios, or market conditions.
