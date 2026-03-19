# Galactic SDK (Legacy)

[![Build SDK](https://github.com/galacticcouncil/sdk/actions/workflows/main.yml/badge.svg)](https://github.com/galacticcouncil/sdk/actions/workflows/main.yml)
[![License](https://img.shields.io/github/license/galacticcouncil/sdk)](https://github.com/galacticcouncil/sdk/blob/master/LICENSE.md)

Legacy packages for [Hydration](https://hydration.net) chain integration. This monorepo contains the stable, `@polkadot/api`-based trading SDK and cross-chain transfer toolkit. These packages are maintained for existing consumers but are not recommended for new projects.

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [SDK](#sdk) — trade router & pool utilities
- [XCM (Cross-Chain)](#xcm-cross-chain) — xcm-core, xcm-cfg, xcm-sdk
- [Examples](#examples)
- [Contributing](#contributing)

## Overview

```
┌────────────────────────────────────────────────────────────┐
│                         Your dApp                          │
├────────────────────────────────┬───────────────────────────┤
│           « sdk »              │       « xcm-sdk »         │
│           ··········           │       ············        │
│           Trade routing        │       Cross-chain         │
│           Pool queries         │       Transfers           │
├────────────────────────────────┴───────────────────────────┤
│             @polkadot/api — Substrate SDK                  │
└────────────────────────────────────────────────────────────┘
```

## Getting Started

### Prerequisites

- Node.js 23+
- npm 10+

### Installation

Pick the packages you need:

```bash
# Trading SDK
npm i @galacticcouncil/sdk

# Cross-chain transfers
npm i @galacticcouncil/xcm-sdk @galacticcouncil/xcm-cfg
```


## SDK

Trade router and pool utilities for Hydration, built on `@polkadot/api`.

<!-- link refs: sdk -->
[sdk_v]: https://img.shields.io/npm/v/@galacticcouncil/sdk.svg
[sdk_npm]: https://www.npmjs.com/package/@galacticcouncil/sdk
[sdk_log]: ./packages/sdk/CHANGELOG.md

| Package | Version | Changelog | Description |
|:---|:---|:---|:---|
| [`@galacticcouncil/sdk`](./packages/sdk) | [![sdk_v]][sdk_npm] | [changelog][sdk_log] | Trade router & pool utilities (`@polkadot/api`) |


## XCM (Cross-Chain)

Stable cross-chain transfer toolkit built on `@polkadot/api`. Production-proven with extensive route coverage.

<!-- link refs: xcm -->
[xcm-core_v]: https://img.shields.io/npm/v/@galacticcouncil/xcm-core.svg
[xcm-core_npm]: https://www.npmjs.com/package/@galacticcouncil/xcm-core
[xcm-core_log]: ./packages/xcm-core/CHANGELOG.md

[xcm-cfg_v]: https://img.shields.io/npm/v/@galacticcouncil/xcm-cfg.svg
[xcm-cfg_npm]: https://www.npmjs.com/package/@galacticcouncil/xcm-cfg
[xcm-cfg_log]: ./packages/xcm-cfg/CHANGELOG.md

[xcm-sdk_v]: https://img.shields.io/npm/v/@galacticcouncil/xcm-sdk.svg
[xcm-sdk_npm]: https://www.npmjs.com/package/@galacticcouncil/xcm-sdk
[xcm-sdk_log]: ./packages/xcm-sdk/CHANGELOG.md

| Package | Version | Changelog | Description |
|:---|:---|:---|:---|
| [`@galacticcouncil/xcm-core`](./packages/xcm-core) | [![xcm-core_v]][xcm-core_npm] | [changelog][xcm-core_log] | Core types, chain & asset definitions |
| [`@galacticcouncil/xcm-cfg`](./packages/xcm-cfg) | [![xcm-cfg_v]][xcm-cfg_npm] | [changelog][xcm-cfg_log] | Pre-built route configs & DEX integrations |
| [`@galacticcouncil/xcm-sdk`](./packages/xcm-sdk) | [![xcm-sdk_v]][xcm-sdk_npm] | [changelog][xcm-sdk_log] | Wallet interface for cross-chain transfers |

### Architecture

```
@galacticcouncil/xcm-sdk  ← Wallet, transfers, fee swaps
@galacticcouncil/xcm-cfg  ← Route configs, DEX implementations
@galacticcouncil/xcm-core ← Core types, chain & asset definitions
```


## Examples

Ready-to-run examples are available in the [`examples/`](./examples) directory:

| Example | Description |
|:---|:---|
| [`sdk-cjs`](./examples/sdk-cjs) | SDK usage with CommonJS |
| [`sdk-esm`](./examples/sdk-esm) | SDK usage with ES Modules |
| [`xcm-transfer`](./examples/xcm-transfer) | XCM cross-chain transfer |


## Contributing

Everything about building, setting up development environment & releasing can be found in [CONTRIBUTING.md](CONTRIBUTING.md).

## Issue Reporting

In case of unexpected SDK behaviour, please create a well-written issue [here](https://github.com/galacticcouncil/sdk/issues/new). It makes it easier to find & fix the problem accordingly.

## Legal

<pre>
This file is part of https://github.com/galacticcouncil/*

               $$$$$$$      Licensed under the Apache License, Version 2.0 (the "License")
            $$$$$$$$$$$$$        you may only use this file in compliance with the License
         $$$$$$$$$$$$$$$$$$$
                     $$$$$$$$$       Copyright (C) 2021-2024  Intergalactic, Limited (GIB)
        $$$$$$$$$$$   $$$$$$$$$$                       SPDX-License-Identifier: Apache-2.0
     $$$$$$$$$$$$$$$$$$$$$$$$$$
  $$$$$$$$$$$$$$$$$$$$$$$        $                      Built with <3 for decentralisation
 $$$$$$$$$$$$$$$$$$$        $$$$$$$
 $$$$$$$         $$$$$$$$$$$$$$$$$$      Unless required by applicable law or agreed to in
  $       $$$$$$$$$$$$$$$$$$$$$$$       writing, software distributed under the License is
     $$$$$$$$$$$$$$$$$$$$$$$$$$        distributed on an "AS IS" BASIS, WITHOUT WARRANTIES
     $$$$$$$$$   $$$$$$$$$$$         OR CONDITIONS OF ANY KIND, either express or implied.
       $$$$$$$$
         $$$$$$$$$$$$$$$$$$            See the License for the specific language governing
            $$$$$$$$$$$$$                   permissions and limitations under the License.
               $$$$$$$
                                                                $$
 $$$$$   $$$$$                    $$                      $$
  $$$     $$$  $$$     $$   $$$$$ $$  $$$ $$$$  $$$$$$$  $$$$  $$$    $$$$$$   $$ $$$$$$
  $$$     $$$   $$$   $$  $$$    $$$   $$$  $  $$     $$  $$    $$  $$     $$$  $$$   $$$
  $$$$$$$$$$$    $$  $$   $$$     $$   $$        $$$$$$$  $$    $$  $$     $$$  $$     $$
  $$$     $$$     $$$$    $$$     $$   $$     $$$     $$  $$    $$  $$$     $$  $$     $$
 $$$$$   $$$$$     $$      $$$   $$$   $$     $$$$   $$$  $$    $$   $$$   $$   $$    $$$
                  $$         $$$$$               $$$$$     $$          $$$$
                $$$
</pre>

For more details read [LICENSE.md](LICENSE.md)
