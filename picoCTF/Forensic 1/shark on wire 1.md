We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

Hints:
- Try using a tool like Wireshark
- What are streams?

# Solución
Con wireshark buscar las transmisiones que sean con UDP, seguir la transmisión y buscar la secuencia donde aparezca la flag:
```
picoCTF{StaT31355_636f6e6e}
```
