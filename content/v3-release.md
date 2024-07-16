---
title: "V3 release of Damn Vulnerable DeFi"
draft: false
summary: Damn Vulnerable DeFi v3 is out! Here are the details.
images:
    - /img/v3-release-cover.png
---

// January 13, 2023

Dear breakers of DeFi, today is a good day. Today a new version of Damn Vulnerable DeFi is out!

![Cover of the article](/img/v3-release-cover.png)

**Featuring:**

- Two and a half fresh new challenges: [Puppet v3]({{< ref "challenges/puppet-v3" >}}), [ABI Smuggling]({{< ref "challenges/abi-smuggling" >}}) and [Wallet Mining]({{< ref "challenges/wallet-mining" >}}). The last kind of already existed, but it's been reworked from scratch. Good as new!
- Introduction of [ERC4626](https://eips.ethereum.org/EIPS/eip-4626), [ERC3156](https://eips.ethereum.org/EIPS/eip-3156) and [ERC2612](https://eips.ethereum.org/EIPS/eip-2612).
- Tokens, authorization schemes and utilities from [Solmate](https://github.com/transmissions11/) and [Solady](https://github.com/Vectorized/solady), bringing new flavors on top of the usual [OpenZeppelin Contracts](https://github.com/OpenZeppelin/openzeppelin-contracts/) stuff. Welcome aboard!
- Tweaks, niceties and cool tricks all around the existing challenges to make them more interesting and (slightly?) increase complexity.
- An absurd amount of QoL changes in tests, dependencies, custom errors, error messages, naming, docs, code organization and gas optimizations (assembly, yay!). 

See the full set of changes [here](https://github.com/theredguild/damn-vulnerable-defi/compare/v2.2.0...v3.0.0).

---

Overall, the testing environment hasn't changed. Solidity 0.8, Ethers and Hardhat. Before you ask, yes, I did consider moving to Foundry. Though it wasn't the right time. I couldn't afford refactoring everything from scratch _and_ adding new features and challenges. If you're a Foundry maxi, remember there're forks ported to Foundry. I expect them to quickly catch up with this new release.

So what's changed ?

Well, all existing challenges have been refactored - from the ground up. I reviewed and updated all Solidity and Javascript code. To the extent probably none of your existing solutions will work anymore. Although the goals for each challenge _mostly_ remain the same, interfaces may have changed, and the code's average complexity has increased. This is due to the introduction of ERC implementations (tokenized vaults, flash loans, permit, etc.), gas optimizations and assembly. Hope these updates make challenges even more fun, as well as reflect part of the evolution that real DeFi contracts have undergone in the past year.

Speaking of introductions, v3 also welcomes new cool building blocks to Damn Vulnerable DeFi. Whereas v2 was solely using OpenZeppelin Contracts, in v3 we have Solmate and Solady bringing new flavors to the game. This should expose you to a broader set of new-ish libraries that have gone into the mainstream.

As of the new challenges, they're simplified versions of issues that were (or could have been) exploited in mainnet. To solve them, you will need to dive into TWAPs, ABI encoding, smart contract wallets, predictable deployments, upgrades, and more. Really looking forward to seeing you tearing them apart.


I've been amazed at the amount of writeups, discussions, videos, threads, around this wargame. I've seen it organically recommended everywhere. I've overheard people at conferences discussing challenges. Even auditing firms are using it for trainings. It's impact has grown well beyond my original expectations. I cannot be more grateful for your love, support and feedback.

A brief reminder before I leave you. Damn Vulnerable DeFi is, and forever will be, an educational resource for the community. It is intended to be a safe playground to train security researchers that will help protect Ethereum applications. In solving these challenges, you may learn how to exploit vulnerabilities in smart contracts. They might resemble the ones you'll uncover during your own research of contracts in production. If that's the case, **always** follow each project's responsible disclosure processes, usually via bug bounty programs or security contacts.

Damn Vulnerable DeFi v3 is waiting for you [here]({{< ref "/" >}}).

Happy hacking :)
