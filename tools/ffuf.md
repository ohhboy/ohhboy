# FFUF

## FFUF

Discover Web Content

```text
ffuf -u https://FUZZ.HOST/ -w ~/payloads/SecLists/Discovery/Web-Content/common.txt -p 1 -t 10
```

Post Request Fuzzing with proxy to Burp

```text
ffuf -w ~/temp/fuc_wordlist.txt -X POST -d "cmd=FUZZ.js" -u http://jewel.uploadvulns.thm/admin/ -fc 401
```



