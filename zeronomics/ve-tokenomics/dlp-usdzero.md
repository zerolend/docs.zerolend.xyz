# dLP $ZERO

The dynamic Liquidity Provision (dLP) model for $ZERO is specifically designed for users who contribute to liquidity pools. When users stake dLP tokens, consisting of 50% $ZERO and 50% of a partner token like $ETH, their $ZERO portion is effectively doubled in value for staking purposes.

#### **Enhanced Weighting for $ZERO**

A distinctive feature of the dLP ve-staking model is the enhanced weighting given to $ZERO tokens at the time of staking. When calculating the value of a user's contribution to the liquidity pool, the $ZERO component is effectively considered double its presence in the pool.&#x20;

**Example:** If a user's liquidity pool token consists of 50% $ZERO and 50% $ETH, the weighting mechanism acknowledges the $ZERO component as if it were 100% of the contribution.&#x20;

{% hint style="info" %}
When staking is locked, the dLP weighting for $ZERO is counted as double its amount in the liquidity pool token.
{% endhint %}

### **Calculation Method**

$veZERO earned  is the product of the quantity of dLP tokens staked and a locking factor $$L_{dLP}$$. As mentioned already, $ZERO tokens in the dLP stake are given double weight. Hence, $$(2 \times \$\textrm{ZERO})$$.&#x20;

$$
\$\textrm{veZERO} =  dLP \times L_{dLP}
$$

$$
\$\textrm{veZERO} = (2 \times \$\textrm{ZERO}_2) \times L_{dLP}
$$

#### Time-Locking Coefficients

Another distinctive feature of the dLP ve-staking model is time-locking coefficients. ZeroLend modifies the time-locking coefficients for dLP stakes to suit the unique risk profile of liquidity pool tokens. The following is the time-scale for dLP:

| Time Lock | L\_dLP - Value |
| --------- | -------------- |
| 1-Months  | 0.0625         |
| 3-Months  | 0.25           |
| 6-Months  | 0.5            |
| 12-Months | 1.0            |

This adjusted time-scale reflects the nuanced differences in risk profile compared to staking single assets.

#### Practical Example

A user staking 10,000 dLP tokens, split into 5,000 $ZERO and an equal value of $ETH for a 6-month period, will be allocated 5,000 $veZERO.&#x20;

**Formula for $veZERO Allocation:**

The total $veZERO a user receives is determined by:

$$
\$\textrm{veZERO} = \$\textrm{ZERO} \times L_{ZERO} + dLP \times L_{dLP}
$$

In this equation:

* $$L_{ZERO}$$ and $$L_{dLP}$$ represent the time-locking coefficients for single-asset $ZERO and dLP stakes, respectively.
* $$dLP$$ is valued as twice the amount of $ZERO present at the time of staking.

To clarify, the formula accounts for the different quantities of $ZERO in single and dLP stakes:

$$
\$\textrm{veZERO} = \$\textrm{ZERO}_1 \times L_{ZERO} + (2 \times \$\textrm{ZERO}_2) \times L_{dLP}
$$

Here, $$\$\textrm{ZERO}_1$$ and $$\$\textrm{ZERO}_2$$ denote the respective amounts of $ZERO in single staking and within the dLP.
