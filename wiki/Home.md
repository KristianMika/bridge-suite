This project aims to provide a tool that interconnects common cryptographic interfaces, e.g., [PKCS#11](https://docs.oasis-open.org/pkcs11/pkcs11-base/v3.0/csprd01/pkcs11-base-v3.0-csprd01.html), or FIDO2, with threshold platforms, e.g., [MeeSign](https://meesign.crocs.fi.muni.cz/). Such interconnection results in highly customizable threshold authentication in originally intended single-party authentication environments.

## Components

The MPC Bridge consists of multiple components:

- [Bridge Controller](Bridge-Controller.md) - GUI Application for interface management ([GitHub](https://github.com/KristianMika/bridge-controller))
- [Cryptoki Bridge](Cryptoki-Bridge.md) - PKCS#11 library implementation ([GitHub](https://github.com/KristianMika/cryptoki-bridge))
- [FIDO2 Bridge](Fido2-Bridge.md) - FIDO2 emulated token (tbd)
- [Web eID Bridge](Web-eID-Bridge.md) - Web eID emulated applet (tbd)

## How to test?

- The easiest way is to use the preconfigured Vagrant configuration located [here](DemoSetup.md)
- If you are interested in a specific component, please refer to the corresponding page for more information
