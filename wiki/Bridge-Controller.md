[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KristianMika/bridge-controller)

Bridge Controller is the central application that provides means to customize and configure other services (emulated interfaces), using a GUI.

## Installation

### Debian-Based Distributions

1. [Setup the MPC Bridge repository](Debian-Repository.md)
2. Install the cryptoki-bridge package

```bash
sudo apt-get install bridge-controller
```

- Alternatively, an AppImage can be found in the [releases page](https://github.com/KristianMika/bridge-controller/releases).

### Other Distributions

Navigate to the [releases page](https://github.com/KristianMika/bridge-controller/releases) and install the built package.

## Usage

Upon installation, the application is available in the desktop menu tray.

## Development

Folder _.devcontainer_ contains a configuration for an environment with all the build dependencies. To learn how to use it, please refer to the provided tutorial locaten in the [Development](Development.md) page.

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
