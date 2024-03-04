<h1>Nmap cheatsheet</h1>
<table>
  <thead>
    <tr>
      <th>Flag</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>-v</code>, <code>-vv</code>, <code>-vvv</code></td>
      <td>verbose</td>
    </tr>
    <tr>
      <td><code>-sS</code></td>
      <td>Escaneo TCP</td>
    </tr>
    <tr>
      <td><code>-sU</code></td>
      <td>Escaneo UDP</td>
    </tr>
    <tr>
      <td><code>-sn</code></td>
      <td>Escaneo sin enviar paquetes</td>
    </tr>
    <tr>
      <td><code>-sP</code></td>
      <td>Descubrimiento de hosts</td>
    </tr>
    <tr>
      <td><code>-Pn</code></td>
      <td>Ping scanning</td>
    </tr>
    <tr>
      <td><code>-p-</code></td>
      <td>Escanear todos los puertos</td>
    </tr>
    <tr>
      <td><code>-sV</code></td>
      <td>Servicios y versiones</td>
    </tr>
    <tr>
      <td><code>-sC</code></td>
      <td>Escaneo con scripts de seguridad</td>
    </tr>
    <tr>
      <td><code>-sCV</code></td>
      <td>Escaneo completo</td>
    </tr>
    <tr>
      <td><code>-O</code></td>
      <td>Adivinar OS</td>
    </tr>
    <tr>
      <td><code>-A</code></td>
      <td>OS y servicios</td>
    </tr>
    <tr>
      <td><code>-T1</code></td>
      <td>Escaneo lento</td>
    </tr>
    <tr>
      <td><code>-T5</code></td>
      <td>Escaneo rápido</td>
    </tr>
    <tr>
      <td><code>--script vuln</code></td>
      <td>Script para buscar vulnerabilidades</td>
    </tr>
    <tr>
      <td><code>--min-rate 1000</code></td>
      <td></td>
    </tr>
    <tr>
      <td><code>--max-rate 1000</code></td>
      <td></td>
    </tr>
  </tbody>
</table>


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
