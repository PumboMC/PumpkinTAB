# Building

Use the Rust 1.100.0 toolchain and WASIp3 target pinned in `rust-toolchain.toml`.

```sh
cargo fetch --locked
cargo fmt --check
cargo clippy --locked --offline --all-targets -- -D warnings
cargo test --locked --offline
cargo build --locked --offline --release --target wasm32-wasip3
```

Install `target/wasm32-wasip3/release/pumpkin_tab.wasm` on a Pumpkin runtime
that supports WASIp3 and matches the pinned plugin WIT.
