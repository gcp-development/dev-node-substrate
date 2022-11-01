This repository is tracking Substrate's
[`polkadot-v0.9.31`](https://github.com/paritytech/substrate/tree/polkadot-v0.9.31) branch.

This repository is unsuitable for a production deployment, it was developed to be a single node to support [Substrate Smart Contracts](https://use.ink/how-it-works) PoCs.

The [crate](https://paritytech.github.io/substrate/master/pallet_contracts/index.html) [pallet-contracts](https://github.com/paritytech/substrate/tree/polkadot-v0.9.31/frame/contracts) for [WebAssembly](https://wiki.polkadot.network/docs/learn-wasm) [smart contracts](https://wiki.polkadot.network/docs/build-smart-contracts#smart-contract-environments-are-still-maturing) were configured for this single node. 

```bash
cargo install contracts-node --git https://github.com/paritytech/substrate-contracts-node.git --tag v0.21.0 --force --locked
```
Note:Verify the tags in [here](https://github.com/paritytech/substrate-contracts-node/tags)

```bash
cargo build --release
```

References:

[StackExchange](https://substrate.stackexchange.com/)
[Smart Contracts](https://wiki.polkadot.network/docs/build-smart-contracts)
