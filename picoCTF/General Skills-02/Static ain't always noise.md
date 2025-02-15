Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static)? This [BASH script](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh) might help!

Solución
Primero para poder ejecutar el script de shell hay que darle permisos de ejecución:
```bash
DiegoR09-picoctf@webshell:~/Static$ chmod 755 ltdis.sh 
```
Después, ejecutar el script pasándole el archivo de static:
```
DiegoR09-picoctf@webshell:~/Static$ ./ltdis.sh static

Resultado:
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
```
Ver el contenido del archivo static.ltdis.strings.txt y hacer un grep para buscar la flag:
```bash
DiegoR09-picoctf@webshell:~/Static$ cat static.ltdis.strings.txt | grep "picoCTF"

Resultado:
   1020 picoCTF{d15a5m_t34s3r_98d35619}
```
