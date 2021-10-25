---
layout: default
title: FAQ
permalink: /faq/
summary: Frequently asked questions about Haveno
---

# Table of contents

- [What's the meaning of Haveno?](#whats-the-meaning-of-haveno)
- [When will Haveno be ready for use?](#when-will-haveno-be-ready-for-use)
- [What currencies will be listed?](#what-currencies-will-be-listed)
- [Why a new platform? What are the key differences compared to Bisq](#why-a-new-platform-what-are-the-key-differences-compared-to-bisq)
  - [Haveno is privacy-focused](#haveno-is-privacy-focused)
  - [Haveno is simpler](#haveno-is-simpler)
  - [Haveno is cheaper](#haveno-is-cheaper)
  - [Haveno is faster](#haveno-is-faster)
- [What are the differences in the trade protocol](#what-are-the-differences-in-the-trade-protocol)
- [UX differences from Bisq](#ux-differences-from-bisq)
- [Will there be an Haveno token like Bisq has BSQ?](#will-there-be-an-haveno-token-like-bisq-has-bsq)
- [Why no DAO?](#why-no-dao)

## What's the meaning of Haveno?

Haveno is an Esperanto word that means 'harbour' or 'port'.

Pronunciation:

PA(key): /haˈveno/
Hyphenation: ha‧ve‧no

## When will Haveno be ready for use?

We hope Haveno will be ready to be deployed by the end of 2022.

## What currencies will be listed?

We plan to have a small set of currencies at launch, but more will follow shortly after. We plan to launch with support for at least: XMR, BTC, BCH, ETH, EUR, USD

## Why a new platform? What are the key differences compared to Bisq

Haveno is a fork of Bisq and share some of its strengths, like:

- Censorship resistant, thanks to the absence of a central server (P2P network).
- Non custodial. The user has the total control of their wallet.
- Built on Tor.

But Haveno brings several improvements over Bisq:

### Haveno is privacy-focused

Bisq doesn't offer strong privacy to its users and have had multiple problems, which resulted in their user's privacy being compromised in past.

- Because of Bitcoin's lack of [fungibility](https://www.getmonero.org/resources/moneropedia/fungibility.html) and privacy proprieties, every transaction and address on the BTC blockchain are easily traceable. Anybody can check who a BTC user transacted to and the amount of the transaction. This design flaw has allowed and empowered blockchain surveillance companies, which make Bitcoin's blockchain a surveillance paradise and a privacy nightmare.
- It's trivial to identify on the Bitcoin blockchain which transactions come from a Bisq exchange. This compromises the privacy of Bisq's traders.
- The BSQ token is a huge privacy concern, when used to pay transaction fees on Bisq, it makes possible to link a transaction with a specific Bisq user.
- A [recent paper](https://arxiv.org/pdf/2007.07048.pdf) demonstrated that it's possible to track Bisq contributors participating to the DAO and deanonymize them.
- Bisq's [trade history is public](https://bisq.network/markets/) and it's posted along details like dates and traded amounts.
- [We found and disclosed a very bad vulnerability in Bisq](https://twitter.com/HavenoDEX/status/1412782658887766016), which until its discovery had allowed malicious actors to harvest payment info like bank accounts, names and potentially home addresses of Bisq users.

Haveno has no token and it's based on Monero, thus taking advantage of its privacy-preserving technologies, resolving the problems mentioned above simply by design or by choice.

### Haveno is simpler

Bisq has a very complex and clunky interface, which limits its ability to reach non technical users. As a result, Bisq is mostly used by power users.

One of our key goals is to offer a simple and smooth user experience, where the user can go from wanting to trade to begin the trade in few minutes.

### Haveno is cheaper

Bisq is based on Bitcoin and inherits its historically high transaction fees, which will have to be added to the trade fee of the platform.

Haveno is based on Monero allowing traders to take advantage of the very low transaction fees (see the [comparison between XMR and BTC](https://bitinfocharts.com/comparison/transactionfees-btc-xmr.html#1y)), resulting in more convenient trades, especially for low amounts.

### Haveno is faster

Because of the hard capped block size in Bitcoin, blocks are often full. To have a transaction confirmed in a reasonable time, the user needs to pay astronomical transaction fees. Bisq doesn't offer the possibility to pay higher fees for Bitcoin transactions, resulting in users having to wait hours (in some cases even more than 24 hours) to see their transaction confirmed and begin the trade, if the network is congested.

Haveno is based on Monero, which beside having much lower transaction fees, it has a dynamic block-size, which makes it more scalable and flexible than Bitcoin.

## What are the differences in the trade protocol

The current trade protocol of Haveno is in [docs/trade-protocol.md](https://github.com/haveno-dex/haveno/blob/master/docs/trade-protocol.md)

Bisq recently adopted a protocol based on a 2/2 multisignature, while Haveno will use their previous protocol: 2/3 multisignature. In a 2/3 multisignature trade, each trader owns one key, this key will be paired with the key of the other trader and will be used to unlock funds and deposits. It's a 2 of 3 (2/3) protocol because you need only two out of three keys to move funds from the multisignature wallet.

If everything goes fine, the two traders will use their keys to complete the transfer process. If something goes wrong, one of the two parties won't use their key to complete the transaction, this is where the arbitrator comes to action.

Arbitrators are inherited from Bisq's 2/3 protocol. They are a trusted role and have the duty of releasing the funds to one of the two parties in case of a conflict. To do so, they use the third key of the 2/3 multisig protocol.

Using arbitrators has drawbacks:

- The arbitrator owns a key, so they could potentially collude with a trader and use their key to send arbitrary transactions
- Arbitrators could be hacked and their key stolen

These issues are solved by employing few and trusted arbitrators with strong operation security knowledge, that will act their role anonymously.

## UX differences from Bisq

Haveno aims to have a much better user experience than Bisq, which suffers of an overcomplicated user interface and an extremely resource-intensive platform, which cannot be even opened on some hardware. Haveno aims to be easy to use and light on the user's system.

## Will there be an Haveno token like Bisq has BSQ?

No. The BSQ token is meant to be the key factor of Bisq's DAO. We won't implement Bisq's DAO and the trades on the platform are based on multisignature transactions. No need for a token.

## Why no DAO?

Bisq's DAO is an interesting and innovative governance mechanism, but currently seems to be an unnecessary complication that takes a lot of resources to maintain. Bisq contributors earn BSQ tokens according to how much they contribute to Bisq and the roles they cover inside the project. More BSQ a person has earned, more their vote count when it comes to vote (for releasing rewards, protocol changes, etc).

Bisq's DAO has several important flaws that make its effectiveness as a tool for decentralized governance dubious:

- BSQ tokens can also be bought. Acquired BSQ has less "voting power" than earned BSQ, but less doesn't mean 'none'. A wealthy and malicious attacker could buy the amount of BSQ necessary to influence a vote. This is a major hole for a decentralized governance system.

- Bisq itself acknowledges that not everything can be managed by the DAO in its current state. For example Changes to the DAO itself still require the approval of Manfred (the creator of the DAO). This is an odd approach outside of the governance system, which is supposed to governed by the DAO.

- Arbitrators are trusted entities that need to deserve the trust of the creator of Bisq. Which [declared he will not give keys to people he doesn't know or trust](https://github.com/bisq-network/proposals/issues/52#issuecomment-433489213). This is factually bypassing the DAO and centralizes the choice of the arbitrators on one person.

- The DAO as used by Bisq, is heavily based on GitHub, which is a centralized entity that has the power to shut down repositories at will. If that would ever happen, Bisq's governance structure will be effectively frozen until the structure is migrated somewhere else and the Bisq app will be adapted. Such migration would take a lot of time and effort.

- There seems to be no expiring date for roles or maximum amount of roles that a contributor can cover. As a result, long term Bisq contributors (who already cover multiple roles) will always gain more BSQ than a newcomer and unless they decide on their own to leave some roles, there is no way for a new contributor to have as much voting power as a veteran Bisq contributor. The new contributor could make such large contributions that would earn them a huge amount of BSQ, but even in that case the release of BSQ is voted with the mechanism we mentioned earlier, so veteran Bisq contributors (with more voting power) could vote against releasing rewards to the newcomer if they feel their power threatened.
