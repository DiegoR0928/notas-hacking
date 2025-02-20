How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 50321`

Solución
Al conectarse tenemos estos dos números en binario:
```
Binary Number 1: 01000100
Binary Number 2: 11000010
```
Primero nos pide un desplazamiento a la izquierda:
```
Question 1/6:
Operation 1: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 1001000
Incorrect. Try again
Enter the binary result: 10001000
Correct!
```
Después hacer una operación de AND que hice con python 
```
Question 2/6:
Operation 2: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1000000
Correct!
```
```python
>>> print(bin(a&b))
0b1000000
```
Después nos pide hacer una operación de suma que hice con python
```
Question 3/6:
Operation 3: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100000110
Correct!
```
```python
>>> print(bin(a+b))
0b100000110
```
Después hacer una operación con | que hice con python
```
Question 4/6:
Operation 4: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11000110
Correct!
```
```python
>>> print(bin(a|b))
0b11000110
```
Después hacer un desplazamiento a la derecha
```
Question 5/6:
Operation 5: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 0
Incorrect. Try again
Enter the binary result: 01100001
Correct!
```
Después hacer una operación de * que hice con python
```
Question 6/6:
Operation 6: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11001110001000
Correct!
```
```python
>>> print(bin(a*b))
0b11001110001000
```
Finalmente nos pide pasar este último resultado a hexadecimal y lo realicé con python
```
Enter the results of the last operation in hexadecimal: 3388

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_1367e2c6}
```
```python
>>> print(hex(int(bin(a*b),2)))
0x3388
```