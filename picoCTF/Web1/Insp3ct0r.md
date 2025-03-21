Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/9670/` ([link](https://jupiter.challenges.picoctf.org/problem/9670/)) or http://jupiter.challenges.picoctf.org:9670

Hints:
- How do you inspect web code on a browser?
- There's 3 parts

Solución 
Ver el código de la página y entrar al código de HTML, ahí encontramos la primera parte 
```html
<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->
```

Entrar a la hoja de estilos y ver la segunda parte
```CSS
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */
```

Entrar a el archivo de javascript
```javascript
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?2e7b23e3} */
```
Flag
picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?2e7b23e3}