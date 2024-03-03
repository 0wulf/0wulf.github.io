## Ping Scanning
Ping scan for scanning up hosts. Not always reliable as not all devices are responding to ping messages for security reasons. Devices as printers are indeed configured to not respond to ping messages, but a more relevant target could be also configured like that.
```$ sudo nmap -sn <ip>/<mask>```
> Here i dont actually know if i need the super user privileges, but i know that nmap requires a lot those privileges for working as intended

## Crafted
```
# nmap -p- -sS -sC -sV --open --min-rate=5000 -vvv -n -Pn <ip> -oN <out file>
```
`--min-rate=5000` solo en entornos seguros
`--script vuln` busca vulnerabilidades
