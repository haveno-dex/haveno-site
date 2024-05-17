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

Haveno can be used now on Monero's main network by using a third party Haveno network.

We do not officially endorse any networks at this time, but they can be found online.

## [What currencies will be listed?](#what-currencies-will-be-listed)

We only support projects that we consider interesting or useful. We will release with support for at least:

| Crypto | Fiat |
|---|---|
| Bitcoin (BTC) | US Dollars (USD) |
| Ether (ETH) | Euro (EUR) |
| Bitcoin Cash (BCH) | British Pounds (GBP) |
| Litecoin (LTC) | Brazilian Real (BRL) |
| | Swiss Franc (CHF) |
| | Indian Rupee (INR) |
| | Canadian Dollar (CAD) |
| | Australian Dollar (AUD) |
| | Japanese Yen (JPY) |

*Note that all assets are paired with XMR, which is the base currency of the platform (XMR/EUR, XMR/USD, XMR/BTC, etc).*

As soon as we feel the platform is solid enough, we will add support for more crypto and fiat currencies, initially targeting some of the assets already listed on Bisq. The community can suggest assets by [opening an issue on the 'listing' repository](https://github.com/haveno-dex/listing) and using the correct template.

## [What's the structure of Haveno?](#whats-the-structure-of-haveno)

The structure and configuration of a Haveno network can be customized when deploying a network instance.

The Haveno project is an open source platform for public reference. We do not operate a live network instance for Monero's main network, but you can test Haveno with Monero's stagenet by following [these instructions](https://github.com/haveno-dex/haveno/blob/master/docs/installing.md).

## [Will there be KYC?](#will-there-be-kyc)

No. Haveno was created out of the desire to provide people a peer to peer and decentralized way to exchange Monero for fiat currency. Haveno is and will always be non-KYC.

## [Where can I find details on how the platform will work?](#where-can-i-find-details-on-how-the-platform-will-work)

Haveno's trade protocol is [explained in detail on Github](https://github.com/haveno-dex/haveno/blob/master/docs/trade_protocol/trade-protocol.md).

## [Do you have more docs?](#do-you-have-more-docs)

Our documentation can be found [in our GitHub Repository](https://github.com/haveno-dex/haveno/tree/master/docs). It contains protcol details, contributing guides, installation instructions, and more.

## [What are arbitrators? Why do you need them?](#what-are-arbitrators-why-do-you-need-them)

Arbitrators are the last step of conflict resolution on Haveno, coming after traders attempt to settle disputes by themselves using the chat embedded in the platform.

In case the traders are unable to complete the trade normally, the arbitrator may return funds to the traders based on the circumstances.

Arbitrators never have custody of trade funds, because they hold only one of three keys during the trade.

## [What are the fees for trading on Haveno?](#what-are-the-fees-for-trading-on-haveno)

By default, Haveno traders pay two fees. The fee for transacting on the Monero network (a fraction of a cent) and a small trading fee.

The trading fee is configurable when deploying a Haveno network.

## [Is Haveno ready? Can we test it?](#is-haveno-ready-can-we-test-it)

Haveno is still work in progress, but it's already possible to do test trades with other people in our test network using stagenet Monero coins, which hold no value. See [the instructions](https://github.com/haveno-dex/haveno/blob/master/docs/installing.md). You can test with both crypto and fiat currencies.

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

These issues can be solved by employing a small number of bonded arbitrators with strong operational security knowledge that will serve in their roles anonymously.

## [Will there be an Haveno token like Bisq has BSQ?](#will-there-be-an-haveno-token-like-bisq-has-bsq)

No. The BSQ token is meant to be the key factor of Bisq's DAO. We won't implement Bisq's DAO and the trades on the platform are based on multisignature transactions. There is no need for a token in the Haveno protocol.

## [Why no DAO?](#why-no-dao)

Bisq's DAO is an interesting and innovative governance mechanism, but currently seems to be an unnecessary complication that takes a lot of resources to maintain. Bisq contributors earn BSQ tokens according to how much they contribute to Bisq and the roles they cover inside the project. The more BSQ a person has earned, the more voting power they have.

Bisq's DAO has several important flaws that make its effectiveness as a tool for decentralized governance dubious:

- BSQ tokens can also be bought. Acquired BSQ has less "voting power" than earned BSQ, but less doesn't mean none. A wealthy and malicious attacker could buy the amount of BSQ necessary to influence a vote. This is a major hole for a decentralized governance system.

- Bisq itself acknowledges that not everything can be managed by the DAO in its current state. For example, changes to the DAO itself still require the approval of Manfred (the creator of the DAO). This is an odd approach outside of the DAO governance system.

- The DAO as used by Bisq, is heavily based on GitHub, which is a centralized entity that has the power to shut down repositories at will. If that would ever happen, Bisq's governance structure will be effectively frozen until the structure is migrated somewhere else and the Bisq app will be adapted. Such migration would take a lot of time and effort.

- There seems to be no expiring date for roles or maximum amount of roles that a contributor can cover. As a result, long term Bisq contributors (who already cover multiple roles) will always gain more BSQ than a newcomer, and unless they decide on their own to leave some roles, there is no way for a new contributor to have as much voting power as a veteran Bisq contributor. The new contributor could make large contributions that would earn them a huge amount of BSQ, but even in that case the release of BSQ is voted on with the mechanism we mentioned earlier, so veteran Bisq contributors (with more voting power) could vote against releasing rewards to the newcomer if they feel their power threatened.

- We already mentioned that a [recent paper](https://arxiv.org/pdf/2007.07048.pdf) demonstrated that it's possible to track Bisq contributors participating to Bisq's DAO and deanonymize them.
