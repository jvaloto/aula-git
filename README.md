Precisa baixar e instalar o [git](https://git-scm.com/downloads)

#### Config
```
# configurar nome do usuário
$ git config --global user.name "User Name"
```

```
# configurar email do usuário
$ git config --global user.email "email@test.com"
```

#### Inicializar um repositório
```
# inicializar um repositório
$ git init
```


#### Exibir o estado atual dos arquivos
```
# exibir o repositório neste momento
$ git status
```

#### Commit
```
# adicionar arquivos no commit
$ git add nome_arquivo
```

```
# commit das alterações no GitHub
$ git commit -m "mensagem do commit"
```


#### Log
```
# exibe os commits realizados
$ git log
```

```
# exibe os commits com um pouco mais de detalhes
$ git log --decorate
```

```
# exibe os commits filtrando pelo autor
$ git log --author="Nome do usuario"
```

```
# exibe os commits por autor com mensagem
$ git shortlog
```

```
# exibe a quantidade de commit por autor
$ git shortlog -sn
```

```
# exibe os commits com uma forma gráfica
$ git log --graph
```

```
# exibe os componentes do commit
$ git show hash_log
```


#### Diff
```
# exibir as diferenças entre os arquivos antes de realizar o commit
$ git diff
```

```
# exibe apenas os nomes dos arquivos que possuem diferença
$ git diff --name-only
```