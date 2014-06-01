git reset
=========
El comando reset saca un archivo del area de preparacion para el commit es decir 'git reset <path>' es lo contrario a 'git add <path>'.

el comando '--soft' no toca el archivo indice o el arbol de trabajo pero reajusta el head a <commit>

```
git reset <commit> --soft
```
Reajusta el archivo indice como el arbol

```
git reset <commit> --hard
```
el comando '~#' deshace la cantidad de commits indicados, el ejemplo mostrado deshace 3 commits

```
git reset HEAD~3 --hard
```

```
git reset HEAD~3 --soft
```