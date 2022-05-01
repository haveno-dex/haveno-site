---
layout: default
title: FAQ
permalink: /faq/
summary: Frequently asked questions about Haveno
---

# Table of contents

## General

- [What's the meaning of Haveno?](#whats-the-meaning-of-haveno)
- [When will Haveno be ready for use?](#when-will-haveno-be-ready-for-use)
- [What currencies will be listed?](#what-currencies-will-be-listed)
- [What's the structure of Haveno?](#whats-the-structure-of-haveno)
- [Will there be KYC?](#will-there-be-kyc)
- [Where can I find the details on how the platform will work?](#where-can-i-find-details-on-how-the-platform-will-work)
- [Do you have more docs?](#do-you-have-more-docs)
- [What are arbitrators? Why do you need them?](#what-are-arbitrators-why-do-you-need-them)
- [What are the fees for trading on Haveno?](#what-are-the-fees-for-trading-on-haveno)
- [Is Haveno ready? Can we test it?](#is-haveno-ready-can-we-test-it)
- [Can I already try Haveno?](#can-i-already-try-haveno)
- [How can I exchange Monero for fiat without involving banks?](#how-can-i-exchange-monero-for-fiat-without-involving-banks)

## Bisq and Haveno

- [Why a new platform? What are the key differences compared to Bisq?](#why-a-new-platform-what-are-the-key-differences-compared-to-bisq)
  - [Haveno is privacy-focused](#haveno-is-privacy-focused)
  - [Haveno is simpler](#haveno-is-simpler)
  - [Haveno is cheaper](#haveno-is-cheaper)
  - [Haveno is faster](#haveno-is-faster)
- [What are the differences in the trade protocol](#what-are-the-differences-in-the-trade-protocol)
- [Will there be an Haveno token like Bisq has BSQ?](#will-there-be-an-haveno-token-like-bisq-has-bsq)
- [Why no DAO?](#why-no-dao)

# General

## [What's the meaning of Haveno?](#whats-the-meaning-of-haveno)

Haveno is an Esperanto word that means 'harbour' or 'port'.

Pronunciation:

PA(key): /haˈveno/
Hyphenation: ha‧ve‧no

## [When will Haveno be ready for use?](#when-will-haveno-be-ready-for-use)

We hope Haveno will be ready to be deployed by the end of 2022.

## [What currencies will be listed?](#what-currencies-will-be-listed)

We only support projects that we consider interesting or useful. We will launch with support for:

| Crypto | Fiat |
|---|---|
| Bitcoin (BTC) | US Dollars (USD) |
| Ether (ETH) | Euro (EUR) |
| Bitcoin Cash (BCH) | British Pounds (GBP) |
| Litecoin (LTC) |

*Note that all assets are paired with XMR, which is the base currency of the platform (XMR/EUR, XMR/USD, XMR/BTC, etc).*

As soon as we feel the platform is solid enough, we will add support for more crypto and fiat currencies, initially targeting some of the assets already listed on Bisq. The community can suggest assets by [opening an issue on the 'listing' repository](https://github.com/haveno-dex/listing) and using the correct template.

## [What's the structure of Haveno?](#whats-the-structure-of-haveno)

We explained the structure of Haveno in detail in a [dedicated blog post]({{ site.baseurl }}/2022/02/02/haveno-structure.html). Here's a summary:

- Half of the fees paid on Haveno will be used to advance Monero and Haveno development

- There will be a CCS-like entity called Engine, which will decide which projects/individuals to sponsor using the fees sent by Haveno

- Engine will be administrated by a council (Engine Council) consisting of 5 trusted members from the Monero and Haveno developer community (including one Monero Core Team member)

Thanks to the funds that will be sent to Engine, Haveno will be a major contributor to Monero development, allowing Monero to cease its reliance on generous donors and become self-sustaining.

While this structure is exciting and opens a lot of doors, we want Haveno to be as decentralized and robust as possible. That's why we will always look for ways to decentralize things further.

## [Will there be KYC?](#will-there-be-kyc)

No. Haveno was created out of the desire to provide people a peer to peer and decentralized way to exchange Monero for fiat currency. Haveno is and will always be non-KYC.

## [Where can I find details on how the platform will work?](#where-can-i-find-details-on-how-the-platform-will-work)

Haveno's trade protocol is [explained in detail on Github](https://github.com/haveno-dex/haveno/blob/master/docs/trade_protocol/trade-protocol.md).

## [Do you have more docs?](#do-you-have-more-docs)

Our documentation can be found [in our GitHub Repository](https://github.com/haveno-dex/haveno/tree/master/docs). It contains protcol details, contributing guides, installation instructions, and more.

## [What are arbitrators? Why do you need them?](#what-are-arbitrators-why-do-you-need-them)

Arbitrators are the last step of conflict resolution on Haveno, coming after traders attempt to settle disputes by themselves using the chat embedded in the platform, and we inherit them from Bisq. They have a crucial role in the trade process, because they hold one of the three keys during a trade.

Holding one of the three keys makes them a sensitive role, because they could theoretically collude with one of the 2 traders. We are exploring the possibility of [migrating to a 2/2 multisig protocol instead of 2/3](https://github.com/haveno-dex/haveno-meta/issues/14), but for the time being, we will adopt several measures to drastically reduce the risks for traders:

- Arbitrators will be picked up randomly from the pool of available arbitrators. This reduces drastically the possibility of collusion, because traders have no possibility of choosing an arbitrator.

- Arbitrators will probably set bonds. These bonds will be locked in the [Engine platform](#whats-the-structure-of-haveno) and will be used to cover the loss of the victim in case of a malicious arbitrator.

- Arbitrators will be trusted members of the Haveno and Monero community, and they will be appointed by the Engine Council in collaboration with the aforementioned community.

## [What are the fees for trading on Haveno?](#what-are-the-fees-for-trading-on-haveno)

Haveno traders will pay two fees. The fee for transacting on the Monero network (a fraction of a cent) and the Haveno fee.

We haven't made a final decision on the amount of the Haveno fee, but it will most likely be less than 1% of the traded amount.

All fees paid on Haveno will be sent to Engine (see [What's the structure of Haveno?](#whats-the-structure-of-haveno)), where they will be used to reward contributors, pay for Haveno development and infrastructure, fund Monero development and research, and more. Fees are also used as an anti-spam mechanism to avoid abuse.

## [Is Haveno ready? Can we test it?](#is-haveno-ready-can-we-test-it)

Haveno is not ready yet, but the trade protocol is already working (like most of the backend). People can already make test trades using the legacy user interface (inherited from Bisq).

## [Can I already try Haveno?](#can-i-already-try-haveno)

Yes, it's already possible to make test trades on our shared Monero stagenet, using the legacy user interface. It's possible to test trades between xmr <-> fiat and xmr <-> crypto. See the instructions for [running your local Haveno test instance](https://github.com/haveno-dex/haveno/blob/master/docs/installing.md).

## [How can I exchange Monero for fiat without involving banks?](#how-can-i-exchange-monero-for-fiat-without-involving-banks)

Haveno will support payment methods that don't require users to have a bank account, like "Cash in person" (for face to face trades) and "Cash by mail".

# Bisq and Haveno

## [Why a new platform? What are the key differences compared to Bisq?](#why-a-new-platform-what-are-the-key-differences-compared-to-bisq)

Haveno is a fork of Bisq and shares some of its strengths, such as:

- Censorship resistance, thanks to the absence of a central server (P2P network).
- Being non custodial. The user has the total control of their wallet.
- Being built on Tor.

But Haveno brings several improvements over Bisq:

### [Haveno is privacy-focused](#haveno-is-privacy-focused)

Bisq doesn't offer strong privacy to its users and has had multiple issues which resulted in the privacy of their users being compromised.

- Because of [Bitcoin's lack of fungibility](https://sethforprivacy.com/posts/fungibility-graveyard/) and privacy, every transaction and address on the BTC blockchain is easily traceable. Anybody can check who a BTC user transacted with and the amount of the transaction. This design flaw has allowed and empowered blockchain surveillance companies.
- It's trivial to identify which transactions come from a Bisq exchange on the Bitcoin blockchain. This compromises the privacy of Bisq's traders.
- As a result of the points above: there have been reports of Bisq users seeing [their accounts on centralized exchanges frozen](https://bisq.community/t/dirty-btc-coins-on-the-xmr-market/7798) after they sent BTC from Bisq to the account on the exchange. This means exchanges actively flag coins coming from Bisq as risky.
- The BSQ token is a huge privacy concern: when used to pay transaction fees on Bisq, it makes possible to link a transaction with a specific Bisq user.
- A [recent paper](https://arxiv.org/pdf/2007.07048.pdf) demonstrated that it's possible to track Bisq contributors participating in Bisq's DAO and deanonymize them.
- Bisq's [trade history is public](https://bisq.network/markets/) and it's posted with details such as dates and traded amounts.
- [We found and disclosed a vulnerability in Bisq]({{ site.baseurl }}/2021/07/07/bisq-vulnerability.html), which until its discovery had allowed malicious actors to harvest payment info like bank accounts, names and potentially home addresses of Bisq users.

From the points above we can see how trading on Bisq is not private and could result in the deanonymization of traders and contributors. Haveno has no token- it's based on Monero and has privacy as a core principle.

### [Haveno is simpler](#haveno-is-simpler)

Bisq has a very complex and resource hungry user interface. One of our main goals is to provide the user with a simple tool that won't require any technical knowledge.

### [Haveno is cheaper](#haveno-is-cheaper)

Bisq is based on Bitcoin and inherits its historically high transaction fees, which are added to tradefees on the platform.

Haveno is based on Monero, allowing traders to take advantage of very low transaction fees (see the [comparison between XMR and BTC](https://bitinfocharts.com/comparison/transactionfees-btc-xmr.html#1y)), resulting in more convenient trades, especially for low amounts.

### [Haveno is faster](#haveno-is-faster)

Haveno will be faster because of three main factors:

- The bitcoin network is slow and blocks are often full. This results in the user having to wait for long time (sometimes even >24h) or pay high transaction fees to see their transaction included in a block. Haveno has Monero instead of Bitcoin at its core. This results in exponentially lower transaction fees and faster inclusion in a block (dynamic blocksize).
- [Research](https://github.com/haveno-dex/haveno-meta/blob/master/haveno-performance-report.md) by a Haveno contributor demonstrated that the resource consumption of Bisq is dominated by JavaFX, which causes the entire app to be slow and sometimes unresponsive. Haveno will have its own frontend separated by the backend. This will result in much lower resource usage and a much better experience for the end user.
- It has no DAO, which is very resource hungry and needs to be synchronized each time the app is launched on Bisq. This impacts user experience heavily, especially if the user hasn't used Bisq in a long time. This important problem will not affect us, since we will not use the DAO, as explained [later in this FAQ](#why-no-dao).

## [What are the differences in the trade protocol?](#what-are-the-differences-in-the-trade-protocol)

The current trade protocol of Haveno is on Github: [docs/trade-protocol.md](https://github.com/haveno-dex/haveno/blob/master/docs/trade_protocol/trade-protocol.md)

Bisq recently adopted a protocol based on 2/2 multisig, while Haveno will use their previous protocol: 2/3 multisignature. In a 2/3 multisignature trade, each trader owns one key; this key will be paired with the key of the other trader and will be used to unlock funds and deposits. It's a 2 of 3 (2/3) protocol because you need only two out of three keys to move funds from the multisignature wallet.

If everything goes fine, the two traders will use their keys to complete the transfer process. If something goes wrong, one of the two parties won't use their key to complete the transaction, and this is where the arbitrator comes to action.

Arbitrators are inherited from Bisq's 2/3 protocol. They are a trusted role and have the duty of releasing the funds to one of the two parties in case of a conflict. To do so, they use the third key of the 2/3 multisig protocol.

Using arbitrators has drawbacks:

- The arbitrator owns a key, so they could potentially collude with a trader and use their key to send arbitrary transactions
- Arbitrators could be hacked and their key stolen

These issues are solved by employing a small number of trusted arbitrators with strong operational security knowledge that will serve in their roles anonymously.

## [Will there be an Haveno token like Bisq has BSQ?](#will-there-be-an-haveno-token-like-bisq-has-bsq)

No. The BSQ token is meant to be the key factor of Bisq's DAO. We won't implement Bisq's DAO and the trades on the platform are based on multisignature transactions. There is no need for a token in the Haveno protocol.

## [Why no DAO?](#why-no-dao)

Bisq's DAO is an interesting and innovative governance mechanism, but currently seems to be an unnecessary complication that takes a lot of resources to maintain. Bisq contributors earn BSQ tokens according to how much they contribute to Bisq and the roles they cover inside the project. The more BSQ a person has earned, the more voting power they have.

Bisq's DAO has several important flaws that make its effectiveness as a tool for decentralized governance dubious:

- BSQ tokens can also be bought. Acquired BSQ has less "voting power" than earned BSQ, but less doesn't mean none. A wealthy and malicious attacker could buy the amount of BSQ necessary to influence a vote. This is a major hole for a decentralized governance system.

- Bisq itself acknowledges that not everything can be managed by the DAO in its current state. For example, changes to the DAO itself still require the approval of Manfred (the creator of the DAO). This is an odd approach outside of the DAO governance system.

- Arbitrators are trusted entities that need to gain the trust of the creator of Bisq, who [declared he will not give keys to people he doesn't know or trust](https://github.com/bisq-network/proposals/issues/52#issuecomment-433489213). This is factually bypassing the DAO and centralizes the choice of the arbitrators on one person.

- The DAO as used by Bisq, is heavily based on GitHub, which is a centralized entity that has the power to shut down repositories at will. If that would ever happen, Bisq's governance structure will be effectively frozen until the structure is migrated somewhere else and the Bisq app will be adapted. Such migration would take a lot of time and effort.

- There seems to be no expiring date for roles or maximum amount of roles that a contributor can cover. As a result, long term Bisq contributors (who already cover multiple roles) will always gain more BSQ than a newcomer, and unless they decide on their own to leave some roles, there is no way for a new contributor to have as much voting power as a veteran Bisq contributor. The new contributor could make large contributions that would earn them a huge amount of BSQ, but even in that case the release of BSQ is voted on with the mechanism we mentioned earlier, so veteran Bisq contributors (with more voting power) could vote against releasing rewards to the newcomer if they feel their power threatened.

- We already mentioned that a [recent paper](https://arxiv.org/pdf/2007.07048.pdf) demonstrated that it's possible to track Bisq contributors participating to Bisq's DAO and deanonymize them.