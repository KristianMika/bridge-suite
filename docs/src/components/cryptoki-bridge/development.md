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

## Debugging

### PKCS11-Spy

[PKCS #11 Spy](https://github.com/OpenSC/OpenSC/wiki/Using-OpenSC#pkcs-11-spy) is a spy library that is injected between a PKCS #11 consumer (application) and a PKCS #11 producer (library). The library logs all function invocations along with the supplied arguments. Envoked calls are delegated to the PKCS #11 producer. 

#### Installation

PKCS #11 Spy is part of the [OpenSC](https://github.com/OpenSC/OpenSC) project and is therefore distributed as part of the OpenSC release artifact. 

##### Debian-Based OS

``` bash
sudo apt-get install opensc
```

#### Usage

The spy is loaded as a regular PKCS #11 library. In addition, the following environment variables are used for customization:

- _PKCS11SPY_ - Specifies the PKCS #11 library that should receive delegated function invocations
- _PKCS11SPY_OUTPUT_ - Specifies log file that will contain function invocations.

#### Example

``` bash
PKCS11SPY="/usr/lib/libcryptoki_bridge.so" PKCS11SPY_OUTPUT="./cryptoki-bridge.log" ssh -I /usr/lib/x86_64-linux-gnu/pkcs11-spy.so username@localhost
```