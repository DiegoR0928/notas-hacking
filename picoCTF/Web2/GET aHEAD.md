Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:34561/

Hints:
- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses

Solución
Hacer un curl a la página y usar la opción -I para que nos muestre los headers de la página y ahi ver la flag
```
diego@Tallin:/mnt/c/Users/Diego$ curl -I http://mercury.picoctf.net:34561/                                      HTTP/1.1 200 OK                                                                                                 flag: picoCTF{r3j3ct_th3_du4l1ty_8f878508}                                                                      Content-type: text/html; charset=UTF-8        
```