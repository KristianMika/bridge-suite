Softfido is a tool that emulates a FIDO2 token that boths supports WebAuthn, and U2F. It was [originally](https://github.com/ellerh/softfido) developed by [Helmut Eller](https://github.com/ellerh).

## Installation

### Debian-Based Distributions

1. Install a Debian package containing the vhci-hcd kernel module suitable for your kernel version

```bash
sudo apt-get install linux-modules-extra-$(uname -r)
```

2. Set up the MPC Bridge [repository](Debian-Repository.md) (or use the [release page](https://github.com/KristianMika/softfido/releases))
3. Install the softfido Debian package

```bash
sudo apt-get install softfido
```

4. Be sure to reboot your machine
