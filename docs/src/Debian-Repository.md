# Debian Repository

This project uses a packagecloud Debian repository to distribute the MPC Bridge packages. The repository is located at [packagecloud.io/kristian_mika/mpc-bridge](https://packagecloud.io/kristian_mika/mpc-bridge).

## Setup

1. Add the repository GPG key

    ```bash
    curl -fsSL https://packagecloud.io/kristian_mika/mpc-bridge/gpgkey | gpg --dearmor > /etc/apt/keyrings/kristian_mika_mpc-bridge-archive-keyring.gpg
    ```

2. Add the Debian repository

    ```bash
    cat <<EOT >> /etc/apt/sources.list.d/kristian_mika_mpc-bridge.list
    deb [signed-by=/etc/apt/keyrings/kristian_mika_mpc-bridge-archive-keyring.gpg] https://packagecloud.io/kristian_mika/mpc-bridge/ubuntu trusty main
    deb-src [signed-by=/etc/apt/keyrings/kristian_mika_mpc-bridge-archive-keyring.gpg] https://packagecloud.io/kristian_mika/mpc-bridge/ubuntu trusty main
    EOT
    ```

3. (Alternatively, at your own risk) Run the following script provided by packagecloud as a quick substitude for the previous steps.

    ```bash
    curl -s https://packagecloud.io/install/repositories/kristian_mika/mpc-bridge/script.deb.sh?any=true | sudo bash
    ```

4. Update APT caches and install

    ```bash
    sudo apt-get update && sudo apt-get install <mpc bridge component>
    ```

5. (Alternatively) You can also download the packages from the release page, or the packagecloud repository page using your browser.
