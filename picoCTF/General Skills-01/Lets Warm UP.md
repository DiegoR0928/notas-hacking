If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

Hint:
	Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag

Solucion 1
con Python 
```
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x70)
'p'

Flag:
picoCTF{p}
```

Solucion 2
Usando cyberchef
```
Input: 0x70
Recipe: From Hex
Output: p

https://cyberchef.org/#recipe=From_Hex('Auto')&input=MHg3MA
```