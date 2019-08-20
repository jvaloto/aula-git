> Projeto para aprendizado de comandos do Git integrando com o GitHub

:paperclip: Precisa baixar e instalar o [git](https://git-scm.com/downloads)

# Configuração do usuário
```
# configurar nome do usuário
$ git config --global user.name "User Name"
```

```
# configurar email do usuário
$ git config --global user.email "email@test.com"
```

# Inicializar um repositório
```
# inicializar um repositório
$ git init
```


# Exibir o estado atual dos arquivos
```
# exibir o repositório neste momento
$ git status
```

# Commit
```
# adicionar arquivos no commit
$ git add nome_arquivo
```

```
# commit das alterações no GitHub
$ git commit -m "mensagem do commit"
```


# Log
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


# Diff
```
# exibir as diferenças entre os arquivos antes de realizar o commit
$ git diff
```

```
# exibe apenas os nomes dos arquivos que possuem diferença
$ git diff --name-only
```

# Checkout
```
# checkout do arquivo conforme versão no git
$ git checkout nome_arquivo
```


# Reset

Voltar históricos que não precisam ser mais comitados. Utilizar quando ainda o commit não foi para o servidor

```
# retorna o commit da hash e já adiciona no commit
$ git reset --soft hash
```

```
# retorna o commit mas sem adicionar no commit novamente
$git reset --mixed hash
```

```
# retorna o arquivo conforme o histórico do hash
$ git reset --hard hash
```

# Adicionar um repositório remoto
```
# adiciona 
$ git remote add origin ssh/https
```

```
# define pela primeira vez para onde vai e de onde vem
$ git push -u origin master
```

# Clonar um repositório
```
# parametro opcional de nome diferente do que esta no git
$ git clone ssh/https [novo-nome]
```


# Fork

Você pode copiar o repositório para a sua conta, realizar as alterações e depois enviar um pull request para o respoitório original.

Se for utilizar git clone, ele apenas serve para quando o projeto for seu, assim você pode enviar os commits diretos para seu repositório.

Clicar no projeto desejado e clicar em "Fork"

# Branch

- Modificar os arquivos sem alterar o branch maser (principal) sem as alterações
- Gerenciamento de forma fácil (criar/apagar)
- Multiplas pessoas trabalhando em várias branchs diferentes
- Evita conflitos, os commits são realizados apenas no final

```
# exibir as branchs existents e qual você está no momento
$ git branch
```

```
# criar uma branch e já entrar nela
$ git checkout -b nome_branch
```

```
# entrar na branch
$ git checkout nome_branch
```

```
# excluir uma branch
$ git branch -D nome_branch
```

```
# apagar uma branch no github
$ git push origin :nome_branch
```

# Merge e Rebase
- Merge: precisa de um commit extra para organizar as bases, tem o histórico de todos os commits já feitos (mais utilizado para pull requests)
- Rebase: ele organiza os commits em linha, não possui o histórico dos commits entre as branches (tentar utilizar sempre que possível)

```
# fazer merge entre as branchs
# deve estar na branch que irá receber o merge
$ git merge nome_branch
```

# Git ignore

Utilizado para definir quais arquivos NÃO serão enviados para o servidor.

Criar um arquivo chamado **.gitignore**

É possível definir quais os arquivos ou utilizar suas extenções:

- arquivo.json
- *.json

# Git stash

Utilizado para "guardar" o state atual das modificações sem comitar, fica em status de WIP "Work In Progress"

```
# cria um estado atual
$ git stash
```

```
# retorna o estado anterior
$ git stash apply
```

```
# lista todos os stash
$ git stash list
```

```
# limpa a lista de stash
$ git stash clear
```

# Alias

Utilizado para não precisar digitar o comando inteiro todas as vezes, por exemplo, utilizar "git s" para "git status"

```
# configrar um alias
$ git config --global alias.palavra_chave comando_executar
```

# Tags

Deixar marcado versões estáveis, é possível baixar o source completo pela tag

```
# cria uma tag com mensagem
$ git tag -a 1.0.0 -m "Mensagem da tag"
```

```
# commit nas tags
$ git push origin master --tags
```

```
# listar todas as tags
$ git tag
```

```
# apagar uma tag local
$ git tag -d nome_tag
```

```
# apagar uma tag no github
$ git push origin :nome_tag
```

# Revert

Utilizado quando é necessário voltar um commit sem perde o histórico do que já tinha sido comitado, diferente do **git reset** 

```
# revertendo a partir de um log
$ git revert hash_log
```