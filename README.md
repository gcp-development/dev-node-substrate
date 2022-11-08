This repository is tracking Substrate's
[`polkadot-v0.9.31`](https://github.com/paritytech/substrate/tree/polkadot-v0.9.31) branch.

This repository is unsuitable for a production deployment, it was developed to be a Substrate Smart Contracts Node to support [Substrate Smart Contracts](https://use.ink/how-it-works) PoCs. The [crate](https://paritytech.github.io/substrate/master/pallet_contracts/index.html) [pallet-contracts](https://github.com/paritytech/substrate/tree/polkadot-v0.9.31/frame/contracts) for [WebAssembly](https://wiki.polkadot.network/docs/learn-wasm) [smart contracts](https://wiki.polkadot.network/docs/build-smart-contracts#smart-contract-environments-are-still-maturing) is configured for this Substrate Smart Contracts Node. <br/>
Note: the consensus from [aura](https://docs.substrate.io/reference/glossary/#authority-round-aura)  & grandpa[(GHOST-based Recursive ANcestor Deriving Prefix Agreement)](https://wiki.polkadot.network/docs/learn-consensus#finality-gadget-grandpa) was changed to manual-seal([sp_consensus](https://docs.rs/sp-consensus/latest/sp_consensus/)/[sc_consensus](https://docs.rs/sc-consensus/latest/sc_consensus/)) where blocks are authored at every transaction.

It's assumed that Rust is [configured and running](https://docs.substrate.io/install/).

```bash
rustup show
```
<img src="https://user-images.githubusercontent.com/76512851/199425508-587354a7-fd4a-49c6-9627-5bdcee3418c6.png" width="500" height="350">

```bash
rustup +nightly show
```
<img src="https://user-images.githubusercontent.com/76512851/199425772-8113e761-2728-40ae-8d78-68e38750a97b.png" width="650" height="400">

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

References:<br/>
[Substrate Stack Exchange](https://substrate.stackexchange.com/)<br/>
[Smart Contracts](https://wiki.polkadot.network/docs/build-smart-contracts)<br/>

