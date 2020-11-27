# SWIP-020 - Swingby Liquidity Provider (SWLP) Token Rate Mechanism

## Summary

A standard interface for handling the fee reward mechanism with a dedicated LP token: the Swingby Liquidity Provider ("SWLP") token.

## Abstract

The following standard allows the implementation of a LP token on the Ethereum blockchain that is used to (1) reward node validators and (2) distribute swap fees to liquidity providers.

This SWIP describes the logic to collect transaction fees for both network validators and liquidity providers through an exchange rate mechanism with SWLP tokens.  

## Motivation

SWLP tokens allows an efficient distribution of swap fees from cross-chain transactions to both liquidity providers and network validators, with a dynamic exchange rate relative to the assets pooled. It prevents distributing transactions _explicitely_, resulting in lower gas fee for all network participants.

## Status

Draft.

## Specification

In Skybridge, LP tokens represent ownership by the owner of the the assets from a pool, which is composed of **two assets meant to have the same value** (_"the bridged assets"_).

The first iteration of Skybridge focuses on a **BTC/WBTC pool** and its LP token is referred to as "SWLP-WBTC".

This document explains the process on how the SWLP exchange rate (vs. BTC) fluctuates, with a focus on the following cases:

1. Users swapping assets (WBTC -> BTC and BTC -> WBTC)
2. Liquidity providers depositing assets (aka minting LP tokens)
3. Liquidity providers withdrawing assets (aka burning LP tokens)

Similar to other DeFi protocols like Compound, the price of the LP token increases over time to reflect the transaction fees being incorporated into the pools. However, there are two categories of LP owners in Skybridge: LP owners and node owners who collect fees in LP tokens.

## Implementation

## License

Copyright (c) 2020 Swingby Labs Pte. LTD. The text content of this specification file is licensed under an MIT license found in the root of this repository.
