# Upgrades / Process

### Voting Requirements

In order to ensure the governance process isn't gamed there are a number of required thresholds for a vote to meet before it can be implemented. These are the following parameters when voting on chain:

* **Proposal threshold:** 1% ownership or delegated ownership of SHARE \(210,000 tokens\)
* **Vote length:** A vote lasts for 17280 blocks \(roughly 3 days\)
* **Minimum Quorum:** 20% of the delegated SHARE must vote in the affirmative
* **Queue:** Successful votes will undergo a timelock delay before execution, currently set at 259200 seconds. This can be modified by governance and set to a minimum of 2 days and a maximum of 14

### Protocol Upgrades

To propose a protocol level upgrade \(to proxy-admin and admin-upgradeability\), a user must:

* [ ] Deploy new contract implementation
* [ ] Verify the source code on Etherscan
* [ ] Submit a PR to the Dollar Protocol Github with a link to the proposal and verified contracts
* [ ] Include a completed audit \(if the change is substantial\). This will be determined by Governance Guardian and community

Any protocol level upgrade that does not meet these requirements will be cancelled by the Guardian.

