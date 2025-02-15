Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/471/enc_flag).

Hints:
	Multiple decoding is always good.

Solución 1
Utilizando cyberchef para decodificar la flag de base 64 5 veces repetidas, la salida de una es la entrada de otra:
```
Input:
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVXbUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdWMlZzVWxaVmJFNW9UVVJDTlZaWE1XRlZRWEJYVFVkME5GWkVSbXRUCmJWWnlUbFpvVldGdGVFVlhibTkzVDFWT2JsQlVNRXNLCg==

Recipe: 
From Base64 -> From Base64 -> From Base64 -> From Base64 -> From Base64

Output: 
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
```

Solución 2
Meter la flag codificada en base 64 a un archivo y despues desde la misma bash decodificarla usando pipelines para decodificarla varias veces: 
```
DiegoR09-picoctf@webshell:~$ base64 --decode mensaje.txt | base64 --decode | base64 --decode | base64 --decode | base64 --decode | base64 --decode 

Resultado:
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
```