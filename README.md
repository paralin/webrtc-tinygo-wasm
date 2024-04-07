# Pion WebRTC with TinyGo and WebAssembly

Make sure `tinygo` and a compatible `go` version is installed.
Then try to build [`webrtc/data-channels/jsfiddle/main.go`](./webrtc/data-channels/jsfiddle/main.go):

```
$ make
```

## TinyGo Installation

We need the dev version of TinyGo.

```
git clone https://github.com/tinygo-org/tinygo
cd tinygo

# version as of 2024-04-07
git checkout 90b0bf646c271157f97aa59ffb2efec7eee4d2ec
git submodule update --init --recursive

# download llvm source
make llvm-source

# see: https://tinygo.org/docs/guides/build/manual-llvm/
make llvm-build

# build wasi-libc
make wasi-libc

# build tinygo
make

# add to your PATH
export PATH=$PATH:$(pwd)/build
```
