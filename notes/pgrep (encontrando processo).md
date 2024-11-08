-> serve para mostrar os processos rodando

com program substitution
```
cd /proc/$(pgrep firefox)
```

```
sudo cat cmdline
```

ver o tempo, e uso do cpu do processo
```
sudo cat oom_score
```
(tem limites por processo)

-> linux detecta processos que estão colocando a integridade do sistema em perigo, os processos são eliminados
-> no windows não tem

[[process substitution]]
[[Threads]]
