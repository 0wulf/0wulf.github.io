[Fuente](https://invertebr4do.github.io/tratamiento-de-tty/#)

---
nos conectamos con netcat a la escucha 
```
$ nc -nvlp <puerto>
```


y hacemos el tratamiento
```
$ script /dev/null -c bash
^Z para SIGSTOP a netcat
$ stty raw -echo; fg
$ reset xterm
```
> `$ htop` luego k `SIGSTOP` en caso que no funcione el ctrl+Z

exportamos variables de entorno
```
$ export TERM=xterm
$ export SHELL=bash
```

Vemos el tamaño de nuestra shell en una consola normal

```
$ ssty size
40 123
```

Y las seteamos en la reverse shell **(en mi caso 40 filas y 123 columnas)**

```
$ stty rows 40 columns 123
```
