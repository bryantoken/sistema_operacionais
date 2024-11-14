### contar número de usuários
```
wc -l /etc/passwd
```
### contar dicionário com maior número de linhas
```
wc -l /usr/share/hunspell/*.dic | sort -nr | head -2 | tail -1
```
