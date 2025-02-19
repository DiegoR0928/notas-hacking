Using a Secure Shell (SSH) is going to be pretty important.

Additional details will be available after launching your challenge instance.

Hints:
- [https://linux.die.net/man/1/ssh](https://linux.die.net/man/1/ssh)
- You can try logging in 'as' someone with `<user>`@titan.picoctf.net
- How could you specify the port?
- Remember, passwords are hidden when typed into the shell

Solución
Nos conectamos con ssh y obtenemos la flag:
```
DiegoR09-picoctf@webshell:~$ ssh ctf-player@titan.picoctf.net -p 50648 
The authenticity of host '[titan.picoctf.net]:50648 ([3.139.174.234]:50648)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Warning: Permanently added '[titan.picoctf.net]:50648' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_3e293eea}
```