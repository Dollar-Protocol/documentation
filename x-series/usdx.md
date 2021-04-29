---
description: Detailed Explanation of USDx (Dollars Token)
---

# USDx

![](../.gitbook/assets/usdx_bg.png)

## **Overview**

**USDx** is the object of stabilization for the USD synthetic asset in Dollar Protocol.

* USDx Contract: [0x2f6081e3552b1c86ce4479b80062a1dda8ef23e3](https://etherscan.io/address/0x2f6081e3552b1c86ce4479b80062a1dda8ef23e3)
* USDx/USDC 12H TWAP Oracle: [0x54e8fccc1f6789b1ad36eb96713c6836a1f02a4c](https://etherscan.io/address/0x54e8fccc1f6789b1ad36eb96713c6836a1f02a4c#code)

When USDx is trading &gt; $1.05 according to the 12H TWAP, a supply delta is calculated.

$$
Δ = (x_{12H} - cpi) * TS / r_{lag}
$$

* **x\_12H** represents the 12H TWAP price of USDx
* **TS** represents the total supply of USDx
* **CPI** represents the price index of the pegged assets. In this case it is USD
* **r\_lag** represents the rebase lag, a governance parameter that serves as a smoothing factor to decrease supply-side volatility

### Positive Rebase

Let's take the following example of a **positive rebase**.

* x\_12H = $1.50
* TS = 15,000,000
* CPI = $1
* r\_lag = 7

The supply delta in this case would be \(1.50 - 1.00\) \* 15,000,000 / 7 = 1,071,428.57 USDx. In this rebase period, around 1.07M USDx would be minted and distributed to protocol stakeholders.

### Negative Rebase

Conversely, let's look at an example of a **negative rebase**:

* x\_12H = $0.90
* TS = 15,000,000
* CPI = $1
* r\_lag = 7

The supply delta would be \(0.90 - 1.00\) \* 15,000,000 / 7 = 214,285.71 USDx.

{% hint style="info" %}
The USDx Debase will eventually be discontinued once the protocol matures past its bootstrapping phase. This will be explained more in the roadmap section with composability.
{% endhint %}



