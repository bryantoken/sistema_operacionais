```
sort <(cat /etc/group /etc/passwd)
```

Se trata da entrada de um comando como se fosse um arquivo de saída

### diferença entre arquivos sorteando o primeiro sem alterar o arquivo ou ter de criar outro
```
diff -y <(sort f1) f2
```
