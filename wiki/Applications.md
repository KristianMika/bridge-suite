## OpenSSH Authentication

### Minimal Requirements

1. [Cryptoki Bridge](Cryptoki-Bridge.md) (but the whole MPC Bridge setup is recommended)
2. [MeeSign Server](https://meesign.crocs.fi.muni.cz/)
3. [MeeSign Clients](https://meesign.crocs.fi.muni.cz/)

### Tutorial

The following tutorial assumes you have created an authentication group on the MeeSign server. If not, please follow the [MeeSign Server](https://meesign.crocs.fi.muni.cz/) documentation.

1. Get the available group public keys in the OpenSSH format.

```bash
ssh-keygen -D <meesign_cryptoki_path.so> -e
```

2. Select the key corresponding to your target group and store it in a file

```bash
echo 'ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBBdg292CUPY0xjjLziR6wkHlPP0yKRF8DYjxMllkphQozXth+Eo12t5vuia8GELe3OFECEeb+Ou34yYL07I2afQ= test-auth-group' > id_ecdsa.pub
```

3. Authorize logins using the acquired public key on a remote server

```bash
ssh-copy-id -f -i id_ecdsa.pub <user@server>
```

4. Authenticate using meesign

```bash
ssh -I <meesign_cryptoki_path.so> <user@server>
```

5. (Optional) Configure the ssh meesign entry by customizing and appending the following entry to `~/.ssh/config`.

```txt
Host <entry_host_name>
    HostName <hostname>
    User <user>
    PKCS11Provider <meesign_cryptoki_path.so>
```

6. (Optional) Authenticate using the meesign ssh entry

```bash
ssh <entry_host_name> # e.g., ssh my_server_via_meesign
```