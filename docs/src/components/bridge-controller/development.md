# Development

The repository contains a prepared devcontainer environment that can be used for a simple and secure development setup. Refer to the provided [tutorial](../../devcontainer.md) on how to use it.

!!! warning "Warning"

    Please, note, this setup has some limitations. For example, you can upload files only from the `devcontainer-shared-files` directory that is located in the repo root and can be accessed from within the container at `/home/dev/shared-files` (can be changed in devcontainer.json under mounts.

## Build Requirements

- [tauri prerequisites](https://tauri.app/v1/guides/getting-started/prerequisites/)
- [npm, Node.js](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [rust](https://www.rust-lang.org/tools/install)
- [protocol buffer compiler](https://grpc.io/docs/protoc-installation/)

!!! info "Info"
    All build requirements are already installed in the provided devcontainer environment

## Development Build

- Launch a development server. The setup watches all files and reflects the changes on the fly

    ```bash
    npm run tauri dev
    ```

## Production Build

- Create a production build

    ```bash
    npm run tauri build
    ```
