Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:17781/](http://mercury.picoctf.net:17781/)

Solución
Hacer un curl a la página de manera repetitiva e ir iterando por los diferentes nombres de las galletas hasta encontrar la flag haciendo uso tambien de curl
```
diego@Tallin:/mnt/c/Users/Diego$ for i in {0..30}; do curl http://mercury.picoctf.net:17781/check -H "Cookie: name=$i" | grep "picoCTF"; done   

<p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}</code></p> 
```
