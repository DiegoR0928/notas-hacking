Unzip this archive and find the file named 'uber-secret.txt'

Solución
Primero extraer los archivos del zip con:
```
DiegoR09-picoctf@webshell:~$ unzip files.zip 
```
Una vez descomprimido, usé grep para buscar dentro de varias carpetas y todos sus archivos con la flag -r de grep dentro de la carpeta de files:
```
DiegoR09-picoctf@webshell:~$ grep -r "picoCTF" files

Resultado:
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}
```