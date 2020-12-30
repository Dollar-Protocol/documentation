# Parameters

{% hint style="info" %}
For the latest list of parameters and calleable functions, please visit [Governance](https://dollarprotocol.com/#/governance).
{% endhint %}

**dollars.sol**

* bondToShareRatio \(uint256\)
  * value between 0 - 100 that represents the percentage of positive rebase seigniorage given to xBond holders. 40 = 40% of positive rebase. The remaining 60% goes to liquidity providers \(LPs\) and Share holders
* lpToShareRatio \(uint256\)
  * value between 0 - 100 that represents the percentage of the positive rebase seigniorage given to LPs as a whole, with the remaining seigniorarge.
  * For example, if value = 70, and bondToShareRatio = 40, then 70% of the remaining 60% goes to LPs as a whole. 60% \* 70% = 42% would go to LPs, which can then be subdivided by points later.
    * xBonds = 40%
    * LPs = 42%
    * Share holders = 18%

**dollarsPolicy.sol**

* deviationThreshold \(uint256\)
  * value between 0 and 10 \* 10 \*\* 16 that represents the allowed neutral range deviation from the peg
  * e.g. value = **5 \* 1e16** = $0.95 &lt; x &lt; $1.05 range for a USD token
* rebaseLag \(uint256\)
  * value greater than 0 that represents a smoothing factor divided into the raw supply delta each rebase
* cpi \(uint256\)
  * value greater than 0 that represents the target peg of the token
  * e.g. $1 = 1e18 \(18
* minRebaseTimeIntervalSec \(uint256\)
  * value in seconds of the minimum time for the next rebase period
  * e.g.  43200 represents half a day
* lastRebaseTimestampSec \(uint256\)
  * value representing the last time the rebase was called successfully
* rebaseWindowOffsetSec \(uint256\)
  * value in seconds representing the offset to shift the rebase. Used if you want to use a rebase period other than 12am UTC \(which is 0\)
  * e.g. a value of 10800 would shift the first rebase to 10800 or 3am UTC roughly
* rebaseWindowLengthSec \(uint256\)
  * value in seconds representing how long the rebase interval is
  * e.g. 900 = 15 minutes. So if your rebase starts at 3am, it would last until 3:15am for a single user to call

**poolReward.sol \(read only\)**

* minimumStakingSeconds \(mapping \(uint256 =&gt; uint256\)\)
  * minimum number of seconds a user must stake in order to withdraw LP
* PoolInfo\[\] public poolInfo
  * public object to show each pool's reward points
* totalAllocPoint \(uint256\)
  * sum of all the individual pool allocPoints
  * e.g. if there are 3 pools, each with 1000 points each, totalAllocPoint = 3000
  * as a result, each pool has a 1000 / 3000 or 33% ownership over the rebase rewards allocated to LP

```javascript
struct PoolInfo {
    uint256 allocPoint;
}
```

