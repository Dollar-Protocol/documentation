# Parameters

{% hint style="info" %}
For the latest list of parameters and calleable functions, please visit [Governance](https://dollarprotocol.com/#/governance).
{% endhint %}

**dollars.sol**

* bondToShareRatio \(uint256\)
* lpToShareRatio \(uint256\)

**dollarsPolicy.sol**

* deviationThreshold \(uint256\)
* rebaseLag \(uint256\)
* cpi \(uint256\)
* minRebaseTimeIntervalSec \(uint256\)
* lastRebaseTimestampSec \(uint256\)
* rebaseWindowOffsetSec \(uint256\)
* rebaseWindowLengthSec \(uint256\)
* rebaseMintPerc \(uint256\)
* maxSlippageFactor \(uint256\)
* treasury \(address\)

**poolReward.sol**

* minimumStakingSeconds \(mapping \(uint256 =&gt; uint256\)\)
* PoolInfo\[\] public poolInfo

```javascript
struct PoolInfo {
    uint256 allocPoint;
}
```

