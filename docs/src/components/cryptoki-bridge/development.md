# Development

The repository contains a prepared devcontainer environment that can be used for a simple and secure development setup. Refer to the provided [tutorial](../../devcontainer.md) on how to use it.

## Build Requirements

- [rust](https://www.rust-lang.org/tools/install)
- [protocol buffer compiler](https://grpc.io/docs/protoc-installation/)

!!! info "Info"
    All build requirements are already installed in the provided devcontainer environment

## Build

1. Update submodules

    ``` bash
    git submodule update --init --recursive
    ```

2. Build the library

    ```bash
    cargo build --release
    ```
