# Initial setup

This tutorial uses a Terra-specific development suite called Terrain.

Terrain will help you:

* Scaffold your dApp project
* Ease the development and deployment process
* Create custom tasks for blockchain and contract interaction with less boilerplate code
* Access a console (or REPL) for interacting with the Terra blockchain
* Create predefined functions used in tasks and in the console

## Prerequisites

## 1. Set up Rust

Rust is the main programming language used for CosmWasm smart contracts. While WASM smart contracts can theoretically be written in any programming language, CosmWasm libraries and tooling work best with Rust.

Install the latest version of [Rust](https://www.rust-lang.org/tools/install).

```sh
# 1. Set 'stable' as the default release channel:

rustup default stable

# 2. Add WASM as the compilation target:

rustup target add wasm32-unknown-unknown

# 3. Install the following packages to generate the contract:

cargo install cargo-generate --features vendored-openssl
cargo install cargo-run-script
```

## 2. Install Terrain

Use npm to install the terrain command-line tool globally:

```sh
npm install -g @iboss/terrain
```

## 3. Download LocalTerra or configure testnet

LocalTerra is a development environment designed to make it easy for smart contract developers to test their contracts locally.

There's a few situations where LocalTerra isn't working properly today. Please check the following situations to determine if you should use the Bombay testnet instead of LocalTerra: 

1. M1 or ARM based hardware like newer Apple products. 
1. Computer with less than 16 gigs of RAM.

### LocalTerra

To download LocalTerra, run the following command:

```sh
git clone --branch v0.5.2 --depth 1 https://github.com/terra-money/localterra
cd localterra
docker-compose up
```

### Testnet

First create a new wallet using the Terra station extension. It's recommended to name this wallet bombay or testnet so it's easy to remember that it's only used for bombay.

After creating a bombay wallet and storing the seed phrase you can request funds from the testnet faucet: 

https://faucet.terra.money

Make sure you have your seed phrase stored somewhere since you will need it in the next section.
