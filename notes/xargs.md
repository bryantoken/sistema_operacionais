saída de comando que é argumento de outro
```
ls | xargs cp -r ./dir
```
### diferença entre uso com xargs (funciona como forEach)
Com xgars
```
ls | xargs cat
```
Sem xargs
```
ls | cat
```
