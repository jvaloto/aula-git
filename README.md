Precisa baixar e instalar o [git](https://git-scm.com/downloads)



```
// configurar nome do usuário
$ git config --global user.name "User Name"
```


```
// configurar email do usuário
$ git config --global user.email "email@test.com"
```


> Inicializar um repositório
```
$ git init
```


> Exibir o repositório neste momento
```
$ git status
```


> Adicionar arquivos no commit
```
$ git add nome_arquivo
```


> Commit das alterações no GitHub
```
$ git commit -m "mensagem do commit"
```


> Exibe os commits realizados
```
$ git log
```


> Exibe os commits com um pouco mais de detalhes
```
$ git log --decorate
```

> Exibe os commits filtrando pelo autor
```
$ git log --author="Nome do usuario"
```

> Exibe os commits por autor com mensagem
```
$ git shortlog
```

> Exibe a quantidade de commit por autor
```
$ git shortlog -sn
```

> Exibe os commits com uma forma gráfica
```
$ git log --graph
```

> Exibe os componentes do commit
```
$ git show hash_log
```