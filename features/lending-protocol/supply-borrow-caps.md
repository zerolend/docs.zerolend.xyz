---
description: >-
  This section explains what are supply/borrow caps and how it is used to
  protect the protocol.
---

# Supply/Borrow Caps

In an event where one of the underlying collateral collapses faster than the risk team can possibly delist or stop the borrowing of that asset, borrow/supply caps start to play a role in limiting the possible bad debt that could occur from within collateral collapse.

## **Borrow Caps** <a href="#borrow-caps" id="borrow-caps"></a>

Borrow caps define the maximum amount of an asset that can be borrowed. Borrow caps can be used to prevent traditional and flash borrowing of an asset which may experience a price exploit and lead to protocol insolvency.

A borrow cap is an optional parameter, and the value will depend on-chain liquidity of the asset and the total volume of borrowed assets in the pool. By default borrow cap of an asset is 0, which signifies no cap. Anyone who has been granted `RISK_ADMIN` or `POOL_ADMIN` role via the ACLManager can call `setBorrowCap` method in PoolConfigurator to update the max total borrow (stable + variable) for the given reserve.

In case the `Borrow Cap` of the reserve is set lower than the current `totalDebt` the existing borrowers are not affected, but no more borrows (stable or variable) can be initiated for that reserve.

## **Supply Caps** <a href="#supply-caps" id="supply-caps"></a>

Supply caps define the maximum amount of an asset that can be supplied to the protocol. Supply caps can be used to limit the protocol’s exposure to riskier assets and protect against infinite minting exploits.

A supply cap is an optional parameter, and the value will depend on the on-chain liquidity of the asset and the total volume of collateral assets in the pool. By default supply cap of an asset is 0, which signifies no cap. Anyone who has been granted `RISK_ADMIN` or `POOL_ADMIN` role via the ACLManager can call `setSupplyCap` method in PoolConfigurator to update the liquidity supply for the given reserve.

In case the Supply Cap of the reserve is set lower than the current liquidity of the reserve, the existing suppliers are not affected, but no more liquidity can be supplied to that reserve.

### FAQs <a href="#faqs" id="faqs"></a>

#### How are supply/borrow caps assigned? <a href="#how-are-supply-borrow-caps-assigned" id="how-are-supply-borrow-caps-assigned"></a>

​Governance can, at any point in time, appoint `RISK_ADMIN` and `POOL_ADMIN` who have the ability to configure the Borrow and Supply Caps of the individual reserves.
