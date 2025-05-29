---
AIP: 1
Title: "Universal Transfer Protocol (UTP)"
Authors: "AB DAO"
Status: Draft
Categories: Technical
Types: Protocol
Created: 2025-05-16
---

[TOC]

## Overview

Universal Transfer Protocol (UTP) is a general-purpose protocol designed within the AB ecosystem for transferring ARC20 assets on-chain. It aims to simplify the cross-chain operation process for on-chain assets and lower the participation threshold for users. The core idea of UTP is to introduce a unified fee payment mechanism for cross-chain transfers.

Users do not need to prepare native tokens of each target chain to pay for gas fees. UTP allows the use of protocol-approved assets (such as stablecoins or AB tokens) to pay transaction fees. This mechanism makes cross-chain asset movement more convenient and secure. In summary, UTP is committed to providing users with a lower-barrier, higher-liquidity cross-chain asset transfer solution.

## Motivation

In traditional blockchain transfers, users must hold native tokens (such as AB or ETH) to pay network fees. This requirement raises the usage threshold, especially in multi-chain interactions or when users operate on a particular chain for the first time. They must obtain the native tokens of the corresponding chain in advance to pay for the fees, which is cumbersome and inconvenient.

To address this pain point, UTP introduces a new mechanism that allows "paying transaction fees using protocol-approved assets". With this mechanism, users can use assets supported by the protocol (such as AB, USDT, USDC, etc.) to directly perform operations and pay the corresponding fees, completely eliminating the dependency on native tokens.

This greatly reduces the threshold for users to interact with blockchain applications and significantly enhances user experience. Users no longer need to prepare and manage native tokens for each blockchain to pay gas fees. The process of cross-chain operations or using a new chain for the first time becomes smoother. This not only benefits users but also enables wallets, DApps, and cross-chain tools to provide a unified entry point for fee payments; users can complete operations without switching tokens across different chains, thus simplifying fee management in multi-chain scenarios.

## Specification

### Using ARC20 Assets as Network Fees

Users can initiate a 0-gas-fee ARC20 transfer transaction. The protocol deducts a portion of the ARC20 asset as the network fee and sends the remaining amount to the user’s target chain address.

### Using AB as Network Fee

Users initiate an ARC20 transfer transaction with a high gas fee. The gas fee serves as the network fee, and the transferred ARC20 amount is sent 1:1 to the user’s target chain address.

## Rationale (optional)

TBD

## Test Cases (optional)

TBD

## Implementation (optional)

## References

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
