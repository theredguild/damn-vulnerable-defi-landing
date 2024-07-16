---
title: "V2 Release"
draft: false
---

// November 02, 2021

Dear breakers of DeFi, today is a good day. Today a new version of Damn Vulnerable DeFi is out!

**Featuring:**

- Fully refactored testing environment, now using [Hardhat](https://hardhat.org) + [Ethers](https://docs.ethers.io/v5/single-page/).
- Most contracts upgraded to Solidity 0.8.
- Four brand new levels: Puppet v2, Free Rider, Backdoor and Climber.
- New (flawed?) integrations with Uniswap v2, Gnosis Safe wallets, timelocks, NFTs and upgradeability patterns.
- A few tweaks here and there in previous challenges after community feedback.
- Dependecy management with yarn.

The biggest and breaking change is obviously the new testing environment, on top of the switch to Solidity 0.8. I hope these changes enhance your experience playing Damn Vulnerable DeFi. Particularly the debugging capabilities of Hardhat should make your life easier.

Prompts and solutions for challenges 1 to 8 should remain the same, but given the refactor your existing code for them won't work anymore. In any case, I recommend just playing their most up-to-date versions. The new testing environment with Hardhat and Ethers is really worth it.

As of the new four challenges, as usual, they're somewhat simplified versions of issues that were (or could have been) exploited in mainnet. So hopefully they serve as learning examples.

Final note: remember Damn Vulnerable DeFi is an educational resource. Throughout these challenges you may learn how to exploit vulnerabilities in smart contracts, and you might run into similar stuff during your own research of real-life deployed contracts. If that's the case, **always** follow each project's responsible disclosure guidelines, usually via bug bounty programs.

Happy hacking :)
