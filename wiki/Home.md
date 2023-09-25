This project aims to provide a tool that interconnects common cryptographic interfaces, e.g., [PKCS#11](https://docs.oasis-open.org/pkcs11/pkcs11-base/v3.0/csprd01/pkcs11-base-v3.0-csprd01.html), or FIDO2, with threshold platforms, e.g., [MeeSign](https://meesign.crocs.fi.muni.cz/). Such interconnection results in highly customizable threshold authentication in originally intended single-party authentication environments.

## Components

The MPC Bridge consists of multiple components:

- [Bridge Controller](./components/Bridge-Controller.md) ([GitHub](https://github.com/KristianMika/bridge-controller))
- [Cryptoki Bridge](./components/Cryptoki-Bridge.md) ([GitHub](https://github.com/KristianMika/cryptoki-bridge))
- [FIDO2 Bridge](./components/Fido2-Bridge.md) (tbd)
- [Web eID Bridge](./components/Web-eID-Bridge.md) (tbd)
