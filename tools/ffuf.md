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



Basic Usage

```text
ffuf -w wordlist.txt -u http://127.0.0.1:8000/api/FUZZ/6 -o output.txt -replay-proxy http://127.0.0.1:8080
```

Basic Usage With a Cookie

```text
ffuf -w wordlist.txt -u http://127.0.0.1:8000/api/FUZZ/6 -o output.txt -replay-proxy http://127.0.0.1:8080 -b "laravel_session=eyJpdiI6Ii8wQU11dTVlUkg2alRHUXBIVzlGSnc9PSIsInZhbHVlIjoiOWs3YllJWTdqNC9xa1pMeFRvMFh0OE1vRFpaWm9GSzFkRktVZS9yUHBDM0lIazZ4K0NsbndxWVIxQ05VZWhqZUZaR0RGQWlFdmdDc24yWllYRklGSXI5STd2b05Pam4yRXIwV1BUWkZhUnFLNUFzOWsycmRHcnlxS0FqRWNsSnEiLCJtYWMiOiI3ZTliMmM2YzIxOTExNDE0NmVjYTYyMGI4Nzg4YzJiYjNmNjVkNDI1YzEyODYwMzY5YzczNzY3NTUwZDk0OGYzIn0%3D;"        
```

Adding a delay

```text
ffuf -w wordlist.txt -u http://127.0.0.1:8000/api/FUZZ/6 -o output.txt -replay-proxy http://127.0.0.1:8080 –p 1 –t 3
```

Adding a delay \(new method\)

```text
ffuf -w wordlist.txt -u http://127.0.0.1:8000/api/FUZZ/6 -o output.txt -replay-proxy http://127.0.0.1:8080 –rate 100
```

Fuzzing 2 values

```text
ffuf -w wordlist.txt:FUZZ -w actions-lowercase.txt:ME -u http://127.0.0.1:8000/api/FUZZ/ME -o output.txt -replay-proxy http://127.0.0.1:8080 
```

Simple Filter

```text
ffuf -w wordlist.txt:FUZZ -w actions-lowercase.txt:ME -u http://127.0.0.1:8000/api/FUZZ/ME -o output.txt -replay-proxy http://127.0.0.1:8080 -fw 1
```

Simple Matcher

```text
ffuf -w wordlist.txt:FUZZ -w actions-lowercase.txt:ME -u http://127.0.0.1:8000/api/FUZZ/ME -o output.txt -replay-proxy http://127.0.0.1:8080 -mc 302
```

Custom Filters

```text
ffuf -w wordlist.txt:FUZZ -w numbers.txt:ME -u http://127.0.0.1:8000/api/FUZZ/ME -o output.txt -replay-proxy http://127.0.0.1:8080 -fr "not found"
```

Fuzzing Post Data

```text
ffuf -w wordlist.txt -X POST -d "email=df%40fd.com&issue=dsafd&information=FUZZ" -u http://127.0.0.1:8000/vulnerability -replay-proxy http://127.0.0.1:8080
```

 Fuzzing Parameters \(POST\)

```text
ffuf -w wordlist.txt -X POST -d "email=df%40fd.com&issue=dsafd&FUZZ=test" -u http://127.0.0.1:8000/vulnerability -replay-proxy http://127.0.0.1:8080
```

Fuzzing Parameters \(GET\)

```text
ffuf -w wordlist.txt -u http://127.0.0.1:8000/contact/submit?FUZZ=d%40d.com&issue=df -o output.txt -replay-proxy http://127.0.0.1:8080 
```

Fuzzing JSON Post Data

```text
ffuf -w wordlist.txt -X "PUT" -u http://127.0.0.1:8000/api/users/6 -H "Content-Type: application/json" -d "{'FUZZ':'test'}" -o output.txt -replay-proxy http://127.0.0.1:8080
```

