# GNU-Netcat cheatsheet
| Comando o Flag | Descripción |
|----------------|-------------|
| `nc <host> <port>` | Conexión a `<host>:<port>` |
| `nc -l -p <port>` | Escucha en el puerto `<port>` |
| `nc -nlvp <port>` | Escucha de todo tipo de conexiones |
| `-u` | UDP |
| `-v` | Verbose |
| `-n` | Sin resolución DNS |
| `-w <num>` | Tiempo de espera |
| `-i <num>` | Intervalo de tiempo |
| `nc -e /bin/sh` | Ejecuta una shell después de la conexión |
| `nc -c <command>` | Ejecuta un comando después de la conexión (al cerrar)|
| `-k` | Acepta múltiples conexiones |
