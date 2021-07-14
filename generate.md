# Generate

## Generate password hash

### One way

```text
openssl passwd -1 -salt [salt] [password]

openssl passwd -1 -salt mysalt Raviraj@1234
```

### second way

```text
mkpasswd -m sha-512 newpasswordhere
```

scp file.txt user@10.10.117.88:/home/user

