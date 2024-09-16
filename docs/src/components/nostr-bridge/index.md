# Nostr Bridge

[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/KristianMika/nostr-bridge)

!!! note "Note"

    Nostr Bridge is currently in the development stage and can not be used for Nostr event signing as MeeSign doesn't support a [BIP-340](https://github.com/bitcoin/bips/blob/master/bip-0340.mediawiki) compatible Schnorr signature protocol yet.

Nostr Bridge is a browser extension that facilitates storage and usage of Nostr user secret key (nsec). The extension interconnects a Nostr client and a threshold platform (MeeSign). The extension works by implementing a `window.nostr` object that is specified in [NIP-07](https://github.com/nostr-protocol/nips/blob/master/07.md).

Visit the [Nostr event signing](../../use%20cases/nostr.md) page for a demo.
