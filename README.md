This repository is tracking Substrate's
[`polkadot-v0.9.31`](https://github.com/paritytech/substrate/tree/polkadot-v0.9.31) branch.

This repository is unsuitable for a production deployment, it was developed to be a Substrate Smart Contracts Node to support [Substrate Smart Contracts](https://use.ink/how-it-works) PoCs. The [crate](https://paritytech.github.io/substrate/master/pallet_contracts/index.html) [pallet-contracts](https://github.com/paritytech/substrate/tree/polkadot-v0.9.31/frame/contracts) for [WebAssembly](https://wiki.polkadot.network/docs/learn-wasm) [smart contracts](https://wiki.polkadot.network/docs/build-smart-contracts#smart-contract-environments-are-still-maturing) is configured for this Substrate Smart Contracts Node. 

It's assumed that Rust is [configured and running](https://docs.substrate.io/install/).

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
./target/release/node --dev
```
Interact with our Substrate Smart Contracts Node using the Contracts UI:

[Contracts-UI](https://contracts-ui.substrate.io/?rpc=ws://127.0.0.1:9944)
 
![image](https://user-images.githubusercontent.com/76512851/199269077-e29144e7-e288-41c0-be51-9060bc16aebd.png)

References:

[Substrate Stack Exchange](https://substrate.stackexchange.com/)

[Smart Contracts](https://wiki.polkadot.network/docs/build-smart-contracts)

