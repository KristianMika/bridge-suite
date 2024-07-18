[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KristianMika/bridge-controller)

Bridge Controller is the central application that provides means to customize and configure other services (emulated interfaces), using a GUI.

## Installation

### Windows

You can install the tool using either the **msi** or **exe** installer available at the [releases page](https://github.com/KristianMika/bridge-controller/releases).

### Debian-Based Distributions

1. [Setup the MPC Bridge repository](Debian-Repository.md)
2. Install the cryptoki-bridge package

```bash
sudo apt-get install bridge-controller
```

### Other Linux Distributions

You can either directly run or install the built **AppImage** [AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher). The **AppImage** is available at the the [releases page](https://github.com/KristianMika/bridge-controller/releases).

## Usage

Upon installation, the application is available in the desktop menu tray.

## Development

Folder _.devcontainer_ contains a configuration for an environment with all the build dependencies. To learn how to use it, please refer to the provided tutorial locaten in the [Development](Development.md) page.

Please, note, this setup has some limitations. For example, you can upload files only from the `devcontainer-shared-files` directory that is located in the repo root and can be accessed from within the container at `/home/dev/shared-files` (can be changed in devcontainer.json under mounts.

### Build Requirements

_(Already installed in the devcontainer)_

- [tauri prerequisites](https://tauri.app/v1/guides/getting-started/prerequisites/)
- [npm, Node.js](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [rust](https://www.rust-lang.org/tools/install)
- [protocol buffer compiler](https://grpc.io/docs/protoc-installation/)

### Development Build

- Launch a development server. The setup watches all files and reflects the changes on the fly
  ```bash
  npm run tauri dev
  ```

## Production Build

- Create a production build
  ```bash
  npm run tauri build
  ```
