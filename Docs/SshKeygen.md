To generate key pair, type the following command at the prompt then press enter.
```
ssh-keygen -b 4096
```
On linux, the public key can be copied via the following command:
```
cat id_rsa.pub
```

By default the operating system will pick the private key stored at .ssh in its home user directory to login via the command:
```
ssh remote_user@remote_ip
```

To use a file from a different directory:
```
ssh -i /path_to_private_key/id_dsa remote_user@remote_ip
```