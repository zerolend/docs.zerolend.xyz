# Deconstructing the Weighted Percentage (T\_p) Calculation

In ZeroLend's model, T\_p represents the Total or Weighted Percentage, crucial for determining rewards. This metric combines the proportions of dynamic Liquidity Provision (dLP\_p) and single-staked $ZERO (Z\_p) relative to the total USD value of a user's lending deposits. Here's a clearer breakdown:

### **Calculating dLP\_p and Z\_p**&#x20;

**dLP\_p Calculation**: Measures the USD value of dLP locked, factoring in the double valuation of $ZERO within LP tokens.

$$
dLP_p = \frac{dLP}{Deposits}  = \frac{\$\textrm{ZERO}_2 \times 2}{Deposits}
$$

**Note:** $$\$\textrm{ZERO}_2$$ adjusts with LP token ratios, while $veZERO earnings depend solely on the $ZERO quantity at deposit time.

**Z\_p Calculation**: Relates to the USD value of $ZERO locked in single asset staking.&#x20;

$$
Z_p = \frac{\$\textrm{ZERO}_1}{Deposits}
$$

Combining for Total Percentage (T\_p)

$$
T_p = 4 \times dLP_p+1\times Z_p = 4 \times \frac{\$\textrm{ZERO}_2 \times 2}{Deposits} + 1 \times \frac{\$\textrm{ZERO}_1}{Deposits}
$$

and,&#x20;

$$
f(T_p) = f(4 \times \frac{\$\textrm{ZERO}_2 \times 2}{Deposits} + 1 \times \frac{\$\textrm{ZERO}_1}{Deposits}) = \begin{cases} 
0 & \text{if } 0.00 \leq T_p< 0.10 \\ 0.5 & \text{if } 0.10 \leq T_p <0.15\\ 0.75 & \text{if } 0.15 \leq T_p < 0.20 \\ 1.0 & \text{if } 0.20 \leq T_p <0.25\\ 1.1 & \text{if } 0.25 \leq T_p < 0.30 \\ 1.25 & \text{if } 0.30 \leq T_p <0.40\\ 1.5 & \text{if } 0.40 \leq T_p < 0.50 \\ 2.0 & \text{if } 0.50 \leq T_p \\

\end{cases}
$$

This function assigns reward levels based on the calculated T\_p value, with different tiers from 0 to 2.0, enhancing rewards progressively as T\_p increases.
