I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/139/challenge.zip)

Hints:
- Version control can help you recover files if you change or lose them!
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)
- You can 'checkout' commits to see the files inside them

Solución
Con el uso de git, podemos observar los commits pasados con git log
```
commit 144fdc44b09058d7ea7f224121dfa5babadddbb9 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:25 2024 +0000

    remove sensitive info

commit 7d3aa557ff7ba7d116badaf5307761efb3622249
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:25 2024 +0000

    create flag
```
Podemos ahora ir al primer commit con git checkout y el id del commit:
```
DiegoR09-picoctf@webshell:~/CommitmentIssues/drop-in$ git checkout 7d3aa557ff7ba7d116badaf5307761efb3622249
Previous HEAD position was 144fdc4 remove sensitive info
HEAD is now at 7d3aa55 create flag
```
Finalmente ahora si podemos observar la flag en el archivo
```
DiegoR09-picoctf@webshell:~/CommitmentIssues/drop-in$ cat message.txt 
picoCTF{s@n1t1z3_be3dd3da}
```