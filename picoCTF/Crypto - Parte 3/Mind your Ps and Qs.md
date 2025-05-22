In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values)

Hints:
Bits are expensive, I used only a little bit over 100 to save money

# Solucion
Descargamos el archivo:
```
┌──(diego㉿Tallin)-[~/pico/Crypto-parte3/MindurPSandQs]
└─$ cat values      
Decrypt my super sick RSA:
c: 843044897663847841476319711639772861390329326681532977209935413827620909782846667
n: 1422450808944701344261903748621562998784243662042303391362692043823716783771691667
e: 65537  
```
Primero factorizamos en la herramienta de FactorDB el numero de n y asi obtener p y q
```
p = 2159947535959146091116171018558446546179
q = 658558036833541874645521278345168572231473
```
Podemos comprobarlo al multiplicar p x q y debe de dar n
```
>>> p = 2159947535959146091116171018558446546179
>>> q = 658558036833541874645521278345168572231473
>>> p * q
1422450808944701344261903748621562998784243662042303391362692043823716783771691667
```

Despues podemos usar formulas de RSA para descifrar el mensaje
```
>>> tn = (p -1) * (q-1)

>>> d = pow(e, -1, tn)
>>> m = pow(c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639555294957886055592061
>>> bytes. fromhex(hex(m)[2:])
b'picoCTF{sma11_N_n0_g0od_00264570}'
```