# Installation

The extension will be available in the Chrome store.

## Dev Installation

1. Install the extension

    - Chrome > Extensions > Enable _Developer mode_ (upper right corner) > Load unpacked (top left) > Select the _dist_ folder

2. Run the envoy proxy

    ```bash
    docker run -d -v "$(pwd)"/envoy.yaml:/etc/envoy/envoy.yaml:ro --network=host --name=envoy envoyproxy/envoy:v1.22.0
    ```
