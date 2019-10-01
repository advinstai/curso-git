# git

Demonstrações de comandos git

## Controlando Versionamento

### Cria um diretório para ser versionado
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

### Obtendo cópia de um repositório remoto
```
mkdir ~/rep-local
cd ~/rep-local/
git clone localhost:~/rep .
git status
```

## Gerenciando Alterações

### Cria uma branch master no repositório
```
git push --set-upstream localhost:~/rep master
```

### Adiciona um arquivo para ser versionado
```
nano t.py
git add t.py 
```

### Salva o snapshot no histórico do projeto e conclui o processo de controle de alterações. Qualquer coisa que tenha sido definida pelo git add para ser versionada torna-se parte do snapshot

```
git commit -m "novo programa python"
```

### Atualiza o repositório remoto com quaisquer confirmações feitas localmente em um commit
```
git push 
```

### Verifica lista da últimas alterações feitas no repositório
```
git log 
```

## Gerenciando Branches

### Criando uma Branch
```
git branch my-branch
```

## Mudando de Branch
```
git checkout my-branch
```

## Alterando um arquivo em uma branch
```
cat z.py
```

## Volta para a Branch principal
```
git checkout master
```

## Versão do arquivo na branch principal
```
cat z.py
```

```
nano t.py 
git status
git add t.py
git commit -m "nova mensagem no programa"
git push
```


