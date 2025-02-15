Unzip this archive and find the flag.
- [Download zip file](https://artifacts.picoctf.net/c/505/big-zip-files.zip)

Hints:
	Can grep be instructed to look at every file in a directory and its subdirectories?

Solución
Primero descomprimir el zip:
```
DiegoR09-picoctf@webshell:~$ unzip big-zip-files.zip
```
Después usar la flag -r para el comando grep para buscar dentro de todos los directiorios y los archivos la flag:
```
DiegoR09-picoctf@webshell:~$ grep -r "picoCTF" big-zip-files

Resultado:
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
```
Ahi encontramos la flag