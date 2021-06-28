# Hashing Crypto

## Identify the Hash

### **HashID** 

Automated hash recognition tools \(Unreliable many formats\) [Hashid project](https://pypi.org/project/hashID/)

### **Hash Identifier** 

```text
hash-identifier
```

### **Online Hash Identifiers** 

[Hash Identifier](https://hashes.com/en/tools/hash_identifier)

## Crack the Hash

### **Find My Hash**

```text
findmyhash MD5 -h HASH_HERE
```

### **John The Ripper** 

#### Basic

```text
john --wordlist=/usr/share/wordlists/rockyou.txt hash_to_crack.txt
```

Format Specific

```text
john --format=raw-md5 --wordlist=/usr/share/wordlists/rockyou.txt hash\_to\_crack.txt
```

_Dealing with Standard hash type add RAW prefix in format_

Check Formats

```text
john --list=formats | grep SHA512
```

Cracking Shadow File \( Relevant lines from each file can be used\) and After unshadow, Use john with given format.

```text
unshadow local\_passwd local\_shadow > unshadowed.txt

john --wordlist=/app/payloads/rockyou.txt --format=sha512crypt unshadowed.txt
```

/app/payloads/rockyou.txt

#### Custom Rule

Custom rules are stored in `/etc/john/john.conf` or `/opt/john/john.conf`

```text
john --wordlist=path_to_wordlist --rule=rule_name path_to_hash_file
```

#### Zip2John

```text
Convert Zip to Hash File

zip2john [options] [zip file] > [output file]

Crack

john --wordlist=app/payloads/rockyou.txt zip\_hash.txt
```

_options is optional most of the times_

#### SSH2John

```text
Convert SSH to Hash File

ssh2john [options] [id_rsa file] > [output file]

Crack

john --wordlist=app/payloads/rockyou.txt ssh_hash.txt
```

