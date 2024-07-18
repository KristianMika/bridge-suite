# Getting Started

This project can be tested using a Vagrant configuration provided in [bridge-box](https://github.com/KristianMika/bridge-suite/tree/main/bridge-box). The configuration creates a ubuntu machine and install all the tools.

## Requirements

1. Install [Vagrant](https://www.vagrantup.com/downloads.html) and [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

2. Install Ansible community plugins.

    ```bash
    ansible-galaxy collection install community.general community.docker
    ```

## Usage

- Start the machine

    ```bash
    vagrant up
    ```

- Turn off the machine

    ```bash
    vagrant halt
    ```

- Resume the suspended machine

    ```bash
    vagrant resume
    ```

- Destroy the setup

    ```bash
    vagrant destroy
    ```

### Using SSH/SFTP

```bash
vagrant ssh-config > vagrant-ssh-config.txt
ssh -F vagrant-ssh-config.txt bridge-box
```

## Testing

### MeeSign Setup

- upon the server launch, MeeSign server should be already running
- there are 2 folders present on the desktop `meesign_client_*`
- to run MeeSign client applications, navigate to these directories and run the binary present in the folders. You can select the `localhost` server, or the `meesign.crocs.fi.muni.cz` server (works only from within the FI network)
- to use multiple clients, you can simply replicate the directories (just make sure to delete the client state - the `app` directory)

### Cryptoki Bridge Setup

- using the start menu, search for `bridge-controller` and run it
  - _NOTE: controller certificate is in `~/Desktop/meesign-server/keys/meesign-ca-cert.pem`_
- the controller can be used to launch the interfaces
  - _NOTE: WebAuthn and U2F must be tested using the provided chrome browser_
- an icon will appear in the trace menu. To display the window, right-click on the icon and select `Show`
- alternativelly, you can test the interfaces individually: softfido binary is located in `/usr/bin/softfido`, and cryptoki-bridge is located in `/usr/lib/libcryptoki-bridge.so`. Be sure to read the documentaion on how to use the interfaces.
