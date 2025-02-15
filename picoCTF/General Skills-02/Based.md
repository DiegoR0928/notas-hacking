To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.

Hints:
	- I hear python can convert things.
	- It might help to have multiple windows open

Solución
Con cyberchef, primero binario:
```
Input: 01101101 01100001 01110000

Recipe: From Binary

Output: map
```
Después de octal:
```
Input: 143 157 155 160 165 164 145 162

Recipe: From Octal

Output: computer
```
Finalmente de Hexadecimal
```
Input: 74657374

Recipe: From Hex

Output: test
```
Resultado:
```
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}
```