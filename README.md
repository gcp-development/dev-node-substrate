It's assumed that these software are installed and running:

<ul>
  <li><a href="https://www.rust-lang.org/tools/install" target="_blank">Rust</a></li>
  <li><a href="https://rust-lang.github.io/rustup/installation/index.html#installing-nightly" target="_blank">nightly</a></li>
  <li><a href="https://crates.io/crates/cargo-contract" target="_blank">cargo contract</a></li>
</ul>

<hr>

This repository is tracking Substrate's
[`polkadot-v0.9.37`](https://github.com/paritytech/substrate/tree/polkadot-v0.9.37) branch.

The dev-node-substrate is a simple Substrate blockchain which is configured to include the Substrate module for [smart contract](https://use.ink/how-it-works) development using [ink! v4.0](https://github.com/paritytech/ink/releases/tag/v4.0.0).

Note: the consensus from [aura](https://docs.substrate.io/reference/glossary/#authority-round-aura)  & grandpa[(GHOST-based Recursive ANcestor Deriving Prefix Agreement)](https://wiki.polkadot.network/docs/learn-consensus#finality-gadget-grandpa) was changed to manual-seal([sp_consensus](https://docs.rs/sp-consensus/latest/sp_consensus/)/[sc_consensus](https://docs.rs/sc-consensus/latest/sc_consensus/)) where blocks are authored at every transaction.

<hr>

ink! CLI version.
```bash
cargo contract --version
```

The directory will be assigned with a Rust toolchain with [rustup override](https://rust-lang.github.io/rustup/overrides.html#directory-overrides).

```bash
rustup show
```

![image](https://user-images.githubusercontent.com/76512851/230028584-f8af7919-7b64-4316-93c3-eceddc60095f.png)

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
Interact with our Substrate Smart Contracts Node using the Contracts UI:

[Contracts-UI](https://contracts-ui.substrate.io/?rpc=ws://127.0.0.1:9944)
 
![image](https://user-images.githubusercontent.com/76512851/199269077-e29144e7-e288-41c0-be51-9060bc16aebd.png)

[Polkadot/Substrate Portal](https://polkadot.js.org/apps/#/explorer)

![image](https://user-images.githubusercontent.com/76512851/201645371-283412c9-86a4-470d-8f80-dcd2dbd50cb8.png)


References:<br/>
[Substrate Stack Exchange](https://substrate.stackexchange.com/)<br/>
[Smart Contracts](https://wiki.polkadot.network/docs/build-smart-contracts)<br/>

