Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip)

Hints:
	After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...

Solución
Ir entrando a las carpetas hasta llegar al archivo binario, usar el comando strings para imprimir los caracteres que se pueden imprimir y filtrar con un grep el comienzo de la flag:
```
DiegoR09-picoctf@webshell:~/TabTabAtack/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ strings fang-of-haynekhtnamet | grep "picoCTF"

Resultado:
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}
```