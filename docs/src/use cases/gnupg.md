# GnuPG (GPG) Signing

## Minimal Requirements

1. [Cryptoki Bridge](../components/cryptoki-bridge/index.md) (but the whole MPC Bridge setup is recommended)
2. [MeeSign Server](https://meesign.crocs.fi.muni.cz/)
3. [MeeSign Clients](https://meesign.crocs.fi.muni.cz/)

## Tool Support

The main option for interconnecting PKCS#11 tokens with GPG is [gnupg-pkcs11-scd](https://github.com/alonbl/gnupg-pkcs11-scd), which unfortunatelly doesn't support ECDSA keys ([GitHub Issue](https://github.com/alonbl/gnupg-pkcs11-scd/issues/17#issuecomment-1244026970)). There is a [proprietary solution](https://docs.digicert.com/en/software-trust-manager/tools/cryptographic-libraries-and-frameworks/gpg-smart-card-daemon.html) provided by DigiCert, though.
_Disclaimer: I haven't tested the tool_
