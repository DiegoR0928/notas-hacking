How about trying to match a regular expression The website is running [here](http://saturn.picoctf.net:64626/).

Hints:
Access the webpage and try to match the regular expression associated with the text field
# Solución
Ver en el código de la página, podemos ver el regex con el que se verifica la contraseña:
```
// ^p.....F!?
```
Podemos ver que el regex significan las siguientes cosas:
- tiene que iniciar con una p
- Debe de acabar con F
- los puntos pueden ser cualquier caracter
Por lo tanto podemos intentar acceder con 
```
picoCTF
```
asi podemos ver la flag
```
picoCTF{succ3ssfully_matchtheregex_08c310c6}
```