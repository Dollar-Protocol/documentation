# USDf

USDf is a fractional-algorithmic stablecoin that is protocol governed.

Currently any user can mint new USDf by depositing a mix between USDC and Gaia, which is the algorithmic reserve asset in the USDf ecosystem.

The ratio between USDC and Gaia is called the collateral ratio.

For example, if a user wants to mint 100 USDf, he/she would need to deposit $100 worth of USDC + Gaia.

The value of Gaia is determined by the 1-H TWAP price.

The collateral ratio is determined by the protocol every hour. If the TWAP price of USDf &gt; $1, then the collateral ratio is decreased by 0.50%. If the TWAP price of USDf &lt; $1, then the collateral ratio is increased by 0.50% to a maximum ratio of 100%. The minimum collateral ratio is currently 0%, i.e. 100% algorithmic, but this can also be set to something like 50%, as per governance.

The community treasury is pre-filled with 10B Gaia tokens, which are worth roughly 20% of the total supply. [https://etherscan.io/address/0x4a7644f6dd90e91b66c489240ce1bf77cec1175d](https://etherscan.io/address/0x4a7644f6dd90e91b66c489240ce1bf77cec1175d)

The idea is that the community can use this as a balance sheet to allocate towards community hires for technology development, marketing as well as growing the community treasury.

5B Gaia tokens are reserved for the team on a 4 year vesting schedule. The remaining 35B Gaia tokens are  in the farming contract [https://etherscan.io/address/0xa66949e08612a5e89f8a35301e2b8537f4ee996b](https://etherscan.io/address/0xa66949e08612a5e89f8a35301e2b8537f4ee996b), which is a non-upgradeable contract based on Sushi Swap's masterchef contract.

Users can farm Gaia by buying Gaia on the open market and providing USDf-Gaia liquidity on Uniswap.

UI: [http://dollarprotocol.com/\#/stake?usdf-gaia](http://dollarprotocol.com/#/stake?usdf-gaia)

Farming commences at block [12071940](https://etherscan.io/block/countdown/12071940)

