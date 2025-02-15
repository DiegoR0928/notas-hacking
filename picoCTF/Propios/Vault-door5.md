In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/d31ce4356bdfd15d33a9af7e35ab4d0a/VaultDoor5.java)

Hints: 
- You may find an encoder/decoder tool helpful, such as https://encoding.tools/
- Read the wikipedia articles on URL encoding and base 64 encoding to understand how they work and what the results look like.

Solución
Al ver el código de java, me doy cuenta de que la flag que le pasas la compara con una cadena en base64 y URL_Encodeada, por lo que con cyberchef se puede sacar:
```
input: JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVmJTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2JTM0JTVmJTY1JTMzJTMxJTM1JTMyJTYyJTY2JTM0'

Recipe: From Base64 -> URL Decode

Output:c0nv3rt1ng_fr0m_ba5e_64_e3152bf4

Flag:
picoCTF{c0nv3rt1ng_fr0m_ba5e_64_e3152bf4}
```