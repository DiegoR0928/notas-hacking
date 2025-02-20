My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/179/challenge.zip)

Hints:
- `git branch -a` will let you see available branches
- How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
- Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim

Solución
Primero podemos ver con el comando de git branch -a las ramas que existen:
```
DiegoR09-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ git branch -a 

Resultado: 
  feature/part-1
  feature/part-2
  feature/part-3
* main
```
Entonces podemos cambiar a la rama de la parte uno con el comando 
```
DiegoR09-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ git checkout feature/part-1    
Switched to branch 'feature/part-1'
```
Y aqui podemos ver el archivo y la primera parte de la flag
```
DiegoR09-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ vim flag.py 

print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')
```
Despues podemos ir a la segunda rama y repetir el procedimiento
```
DiegoR09-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ git checkout feature/part-2 --f
Switched to branch 'feature/part-2'

DiegoR09-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ vim flag.py 

print("Printing the flag...")
print("m@k3s_th3_dr3@m_", end='')
```
Finalmente vamos a la tercera y hacemos lo mismo
```
DiegoR09-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ git checkout feature/part-3 --f
Switched to branch 'feature/part-3'

DiegoR09-picoctf@webshell:~/CollaborativeDevelopment/drop-in$ vim flag.py

print("Printing the flag...")
print("w0rk_798f9981}")
```

Flag: 
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_798f9981}