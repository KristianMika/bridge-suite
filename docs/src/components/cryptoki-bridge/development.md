# Development

Folder _.devcontainer_ contains a configuration for an environment with all the build dependencies. To learn how to use it, please refer to the provided tutorial locaten in the [Development](development.md) page.

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
