### encontra todos dicionários US do sistema salvando no arquivo f1 e salvando erros em /dev/null
```
find / -name '*US.dic' 1> f1 2>/dev/null
```
### descartando os erros e sorteando e saindo com tee no terminal e no f2
```
find / -name '*US.dic' 2>/dev/null | sort | tee f2
```

vá para [[Process substitution]]
