# git
Curso sobre git

### cria um diretório para ser versionado
```
mkdir rep
cd rep/
nano t.py
```
### Inicia repositório
```
git init
```

### Verifica estado de cada arquivo
```
git status
```

### Adiciona arquivo para ser versionado
```
git add t.py 
```

### Mostra que agora o arquivo está sendo versionado

```
git status
```

### Retirando o versionamento do arquivo

```git rm --cached t.py
  git status
```

```
git commit -m "novo programa python"
```

```
git push localhost:~/rep
```

### cria uma branch master no repositório

```
git push --set-upstream localhost:~/rep master
```

```
nano t.py 
git status
git add t.py
git commit -m "nova mensagem no programa"
git push
```

### nó remoto:

```
mkdir ~/rep-local
cd ~/rep-local/
git clone localhost:~/rep .
```
