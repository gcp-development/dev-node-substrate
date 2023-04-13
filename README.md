# dev-node-substrate

It's assumed that these software are installed and running:

<ul>
  <li><a href="https://www.rust-lang.org/tools/install" target="_blank">Rust</a></li>
  <li><a href="https://rust-lang.github.io/rustup/installation/index.html#installing-nightly" target="_blank">nightly</a></li>
  <li><a href="https://crates.io/crates/cargo-contract" target="_blank">cargo contract</a></li>
</ul>

This project was developed using the [Intellij Community](https://www.jetbrains.com/idea/download/#section=linux) with the [Rust plugin](https://www.jetbrains.com/rust/).

<hr>

This repository is tracking Substrate's
[`polkadot-v0.9.37`](https://github.com/paritytech/substrate/tree/polkadot-v0.9.37) branch.

The dev-node-substrate is a simple Substrate blockchain which is configured to include the Substrate module for [smart contract](https://use.ink/how-it-works) development using [ink! v4.0](https://github.com/paritytech/ink/releases/tag/v4.0.0).

Note: the consensus from [aura](https://docs.substrate.io/reference/glossary/#authority-round-aura)  & grandpa[(GHOST-based Recursive ANcestor Deriving Prefix Agreement)](https://wiki.polkadot.network/docs/learn-consensus#finality-gadget-grandpa) was changed to manual-seal([sp_consensus](https://docs.rs/sp-consensus/latest/sp_consensus/)/[sc_consensus](https://docs.rs/sc-consensus/latest/sc_consensus/)) where blocks are authored at every transaction.

<hr>

[ink! CLI version](https://use.ink/getting-started/setup#ink-cli).
```bash
cargo contract --version
```

![image](https://user-images.githubusercontent.com/76512851/231824713-4cf9311c-800d-49a0-a5a8-ef244e0031c7.png)


The directory will be assigned with a Rust toolchain with [rustup override](https://rust-lang.github.io/rustup/overrides.html#directory-overrides).

```bash
rustup show
```

![image](https://user-images.githubusercontent.com/76512851/230036769-8f8cddee-17b8-4c39-808a-7d26e068f11e.png)

Note:The nightly-2023-02-09 is set by the [rust-toolchain.toml](https://github.com/gcp-development/dev-node-substrate/blob/main/rust-toolchain.toml) file.

Test the outer node.
```bash
cargo check -p node --release
```

Test the runtime node.
```bash
cargo check -p node-runtime --release
```

Build the Substrate Smart Contracts Node.
```bash
cargo build --release
```

Run the Substrate Smart Contracts Node.
```bash
./target/release/dev-node-substrate --dev
```

![image](https://user-images.githubusercontent.com/76512851/230036266-13f97ce3-8d37-4e3d-adca-c969aa46dd59.png)

<hr>

Interact with our Substrate Smart Contracts Node using the Contracts UI:

[Contracts-UI](https://contracts-ui.substrate.io/?rpc=ws://127.0.0.1:9944)
 
![image](https://user-images.githubusercontent.com/76512851/230034898-3afb6aa8-fb0c-4e6d-b14b-e5274730deb1.png)

[Polkadot/Substrate Portal](https://polkadot.js.org/apps/#/explorer)

![image](https://user-images.githubusercontent.com/76512851/230035721-c4936f8a-e025-48a3-8ce9-a3069f8b3c24.png)

References:<br/>
[ink!](https://use.ink/)<br/>
[Smart Contracts](https://wiki.polkadot.network/docs/build-smart-contracts)<br/>
