# Usage

Cryptoki Bridge is a shared library that can be loaded into any application that supports PKCS#11. On Debian-based distributions, the library is installed in `/usr/lib/libcryptoki_bridge.so`.

## Configuration

1. [Bridge Controller](../bridge-controller/index.md)
2. ENV Variables
      - _COMMUNICATOR_HOSTNAME_ - sets the meesign hostname, e.g., `meesign.crocs.fi.muni.cz` (required)
      - _COMMUNICATOR_CERTIFICATE_PATH_ - provides the library with the path to the CA certificate (required)
      - _GROUP_ID_ - sets the signing group (optional). If not set, all groups present on the communicator are available.

## Applications

- [OpenSSH Authentication](../../applications/openssh.md)
