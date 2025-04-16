Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.

Hints:
- How did pictures from the moon landing get sent back to Earth?
- What is the CMU mascot?, that might help select a RX option

# Solución
Una vez teniendo en audio en formato wav. Podemos descargar una herramienta para decodificar una imagen a partir del audio. Usando SSTV. Decodificamos:
```
└─$ sstv -d message.wav -o resultado.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...                                [####################################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
```
Y obtenemos la imagen de donde podemos sacar la flag
![[Pasted image 20250415171541.png]]
Flag:
```
picoCTF{beep_boop_im_in_space}
```