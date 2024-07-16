---
title: "Releasing Damn Vulnerable DeFi V4"
draft: false
summary: Damn Vulnerable DeFi V4 is out!
images:
    - /img/v4-release-cover.png
---

**July 16, 2024**

Yes yes yessss! Rumours are true. We've made it. **A new version of Damn Vulnerable DeFi is out!**

![Cover of the article](/img/v4-release-cover.png)

## What's in V4?

- Full migration from Hardhat to Foundry.
- Updated all dependencies to the latest versions (e.g., OpenZeppelin Contracts v5), and all contracts to Solidity 0.8.25.
- Four brand new challenges: [Curvy Puppet]({{< ref "challenges/curvy-puppet">}}), [Shards]({{< ref "challenges/shards">}}), [Withdrawal]({{< ref "challenges/withdrawal">}}) and [The Rewarder]({{< ref "challenges/the-rewarder" >}}). The last one has been completely reworked.
- Introduction of fancy stuff like multicalls, meta-transactions, permit2, merkle proofs, and ERC1155.
- Modernized all existing challenges. Your past solutions might not work anymore.
- All challenges now require players to deposit funds into designated recovery accounts.
- Various quality-of-life changes, including improvements in errors, events, code organization, variable names, documentation, and optimizations.
- New style for the landing page.

More details about the changes are available in the [CHANGELOG](https://github.com/theredguild/damn-vulnerable-defi/blob/v4.0.0/README.md) or the [unreadable diff with v3](https://github.com/theredguild/damn-vulnerable-defi/compare/v3.0.0...v4.0.0).

## I played v3, should I play V4?

If you passed all V3 challenges, I recommend:

- Playing the new challenges: [Curvy Puppet]({{< ref "challenges/curvy-puppet">}}), [Shards]({{< ref "challenges/shards">}}), [Withdrawal]({{< ref "challenges/withdrawal">}}) and [The Rewarder]({{< ref "challenges/the-rewarder" >}}).
- Revisiting [Naive Receiver]({{< ref "challenges/naive-receiver">}}), as it has been extended with a meta-transactions implementation.

The rest of the challenges have been modified, but remain essentially the same.

## More comments on V4

Damn Vulnerable DeFi has come a long way, with almost a year and a half since the [v3 release]({{< ref "v3-release" >}}) and almost 4 years since v1.

V4 brings a**complete overhaul of the challenges**. The migration to Foundry required refactoring all JavaScript code to Solidity, which was not as cumbersome as I initially expected. Although it did require some rethinking around the challenges' structure, necessary cheatcodes, and new libraries.

**Upgrading dependencies** forced me to rework many challenges. Fortunately for the ecosystem (but not for Damn Vulnerable DeFi), libraries keep making it harder to write bad code, so I had to find workarounds to still misuse them or integrate them with unsafe code without being too obvious. I also removed all references to selfdestruct, which triggered non-trivial changes.

From now on, players will always need to **deposit rescued assets into designated recovery accounts**. This change aligns with the latest progress in initiatives like [SEAL and their Safe Harbor agreement](https://github.com/security-alliance/safe-harbor).

The **four new challenges** in V4 are based on real-world cases and ideas suggested by the community. They cover a wide range of topics, including AMMs, liquidations, merkle proofs, bridge withdrawals, token distributions, fractional NFTs, and more. I hope v4 continues to reflect the evolution of real smart contracts and their (weird) use cases.

**Damn Vulnerable DeFi is a public good** for the security community, with no paywalls, logins, or business model. It's a **forever-free educational resource** to train developers and security researchers who want to dive into smart contract security.

By the way, I've transferred Damn Vulnerable DeFi's assets to [The Red Guild](https://theredguild.org/). Because I want the project to grow beyond just me, and The Red Guild seemed the perfect fit for this public good.

Final reminder: in Damn Vulnerable DeFi you might learn how to detect and exploit smart contract vulnerabilities to rescue funds at risk. But don't be deceived. **Reality is much more complex than these simplified educational challenges**. If you discover a real vulnerability, you must **ALWAYS** follow the projects' responsible disclosure processes, usually via bug bounty programs, their Safe Harbor agreement, or security contacts.

If you ever need assistance with a real vulnerability disclosure, **contact [SEAL 911](https://t.me/seal_911_bot)** to get proper guidance from experts.

All said. Enjoy [Damn Vulnerable DeFi v4]({{< ref "/" >}})!
