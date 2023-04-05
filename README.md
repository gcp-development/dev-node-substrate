It's assumed that these software are installed and running:

<ul>
  <li><a href="https://www.rust-lang.org/tools/install" target="_blank">Rust</a></li>
  <li><a href="https://rust-lang.github.io/rustup/installation/index.html#installing-nightly" target="_blank">nightly</a></li>
  <li><a href="https://crates.io/crates/cargo-contract" target="_blank">cargo contract</a></li>
</ul>
<hr>

This repository is tracking Substrate's
[`polkadot-v0.9.37`](https://github.com/paritytech/substrate/tree/polkadot-v0.9.37) branch.

The dev-node-substrate is a simple Substrate blockchain which is configured to include the Substrate module for smart contract developement using [ink!4.0](https://github.com/paritytech/ink/releases/tag/v4.0.0).

<hr>
This repository is unsuitable for a production deployment, it was developed to be a Substrate Smart Contracts Node to support [Substrate Smart Contracts](https://use.ink/how-it-works) PoCs. The [crate](https://paritytech.github.io/substrate/master/pallet_contracts/index.html) [pallet-contracts](https://github.com/paritytech/substrate/tree/polkadot-v0.9.31/frame/contracts) for [WebAssembly](https://wiki.polkadot.network/docs/learn-wasm) [smart contracts](https://wiki.polkadot.network/docs/build-smart-contracts#smart-contract-environments-are-still-maturing) is configured for this Substrate Smart Contracts Node. <br/>
Note: the consensus from [aura](https://docs.substrate.io/reference/glossary/#authority-round-aura)  & grandpa[(GHOST-based Recursive ANcestor Deriving Prefix Agreement)](https://wiki.polkadot.network/docs/learn-consensus#finality-gadget-grandpa) was changed to manual-seal([sp_consensus](https://docs.rs/sp-consensus/latest/sp_consensus/)/[sc_consensus](https://docs.rs/sc-consensus/latest/sc_consensus/)) where blocks are authored at every transaction.

It's assumed that Rust is [configured and running](https://docs.substrate.io/install/).

rustc version
```bash
rustup show
```
![image](https://user-images.githubusercontent.com/76512851/229990984-24d9834e-4a98-4eb2-b97d-578641fdcadd.png)

rustc +nightly version
```bash
rustup +nightly show
```
![image](https://user-images.githubusercontent.com/76512851/229991173-f393a3c7-478f-465a-bedb-b5f827aceddd.png)

ink! CLI version.
```bash
cargo contract --version
```
![image](https://user-images.githubusercontent.com/76512851/229992243-d014b1b6-7aa6-4150-b018-bb46795a7671.png)


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

