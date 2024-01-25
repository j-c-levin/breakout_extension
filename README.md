build command: 
```
cargo build --release --target wasm32-unknown-unknown

wasm-bindgen --no-typescript --target web \
--out-dir ./out/ \
--out-name "breakout_extension" \
./target/wasm32-unknown-unknown/release/breakout_extension.wasm
```

then for further optimisations
```
wasm-opt -Oz -o out/output.wasm out/breakout_extension_bg.wasm
```