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

### Third way


