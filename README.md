# git

Demonstrações de comandos git

## Controlando Versionamento

### cria um diretório para ser versionado
```
mkdir rep
cd rep/
nano t.py
nano z.py
```
### Inicia repositório
```
git init
```

### Verifica estado dos arquivos do repositório
```
git status
```

### Adiciona arquivo para ser versionado
```
git add t.py 
git add z.py 
```

### Mostra que agora o arquivo está sendo versionado
```
git status
```

### Retirando o versionamento do arquivo
```
git rm --cached t.py
git status
```

### Obtendo cópia de um repositório remoto:
```
mkdir ~/rep-local
cd ~/rep-local/
git clone localhost:~/rep .
git status
```

## Gerenciando alterações

### cria uma branch master no repositório
```
git push --set-upstream localhost:~/rep master
```

### Adiciona um arquivo para ser versionado
```
nano t.py
git add t.py 
```

### Prepara arquivos para gerar uma nova versão no repositório
```
git commit -m "novo programa python"
```

### Confirma nova versão
```
git push 
```

### Verifica lista da últimas alterações feitas no repositório
```
git log 
```

## Gerenciando Branches


```
nano t.py 
git status
git add t.py
git commit -m "nova mensagem no programa"
git push
```


