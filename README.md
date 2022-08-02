<div align="center">
	<img src="./assets/git.png">
	<h1>Comandos Git: Versionamento básico</h1>
</div>
&nbsp;
     
&nbsp;       
### Índice
1. &nbsp;&nbsp;[Configurações básicas](#Configurações-básicas)
1. &nbsp;&nbsp;[Inicializando um repositório Git](#Inicializando-um-repositório-Git)
1. &nbsp;&nbsp;[Adicionando arquivos alterados e/ou não rastreados a staging area](#Adicionando-arquivos-alterados-eou-não-rastreados-a-staging-area)
1. &nbsp;&nbsp;[Efetuando o commit das alterações](#Efetuando-o-commit-das-alterações)
1. &nbsp;&nbsp;[Desfazendo alterações](#Desfazendo-alterações)
1. &nbsp;&nbsp;[Exibindo o estado de um arquivo no momento](#Exibindo-o-estado-de-um-arquivo-no-momento)
1. &nbsp;&nbsp;[Examinando o histórico de alterações](#Examinando-o-histórico-de-alterações)
1. &nbsp;&nbsp;[Comparando diferenças entre arquivos da working area e arquivos da staging area](#Comparando-diferenças-entre-arquivos-da-working-area-e-arquivos-da-staging-area)
1. &nbsp;&nbsp;[Branches](#Branches)
1. &nbsp;&nbsp;[Unindo as branches](#Unindo-as-branches)
1. &nbsp;&nbsp;[Remover um arquivo do repositório](#Remover-um-arquivo-do-repositório)
1. &nbsp;&nbsp;[Enviando as modificações para o repositório remoto](#Enviando-as-modificações-para-o-repositório-remoto)
1. &nbsp;&nbsp;[Criando uma cópia de um repositório remoto para a máquina local](#Criando-uma-cópia-de-um-repositório-remoto-para-a-máquina-local)
1. &nbsp;&nbsp;[Atualizando o repositório local com base nas modificações do repositório remoto](#Atualizando-o-repositório-local-com-base-nas-modificações-do-repositório-remoto)
1. &nbsp;&nbsp;[Criando um arquivo .gitignore](#Criando-um-arquivo-gitignore)
1. &nbsp;&nbsp;[Configurando atalhos para comandos Git](#Configurando-atalhos-para-comandos-Git)
1. &nbsp;&nbsp;[Obtendo ajuda com o Git](#Obtendo-ajuda-com-o-Git)
1. &nbsp;&nbsp;[Extra: Comandos úteis do Linux](#Extra-Comandos-úteis-do-Linux)
&nbsp;
     
&nbsp;    
### Configurações básicas
Configurando a identidade do usuário que realizará o versionamento:
```sh
$ git config --global user.name "nome do usuario aqui"
$ git config --global user.email "email do usuario aqui"
```
Consultando a identidade registrada:
```sh
$ git config user.name 
$ git config user.email 
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Inicializando um repositório Git 
```sh
# Criando um diretório para o projeto
$ mkdir nome-do-diretorio

# Acessando o diretório
$ cd nome-do-diretorio   

# Indicando ao Git que este será o diretório local usado para o versionamento do projeto
$ git init 
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;       
### Adicionando arquivos alterados e/ou não rastreados a staging area
```sh
# Adicionando um arquivo específico 
$ git add nome-do-arquivo
```
```sh
# Adicionando todos os arquivos de uma só vez
$ git add .
```
```sh
# Adicionando todos os arquivos de um diretório, de acordo com a sua extensão
$ git add *.py
$ git add *.js
```
```sh
# Para exibir arquivos que estão na staging area, mas que ainda não foram commitados
$ git diff --staged
```
```sh
# Para retirar um arquivo da staging area
$ git rm --cached nome-do-arquivo
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Efetuando o commit das alterações
Registrando as alterações do projeto:
```sh
$ git commit 
```
Registrando as alterações do projeto junto com uma mensagem breve que descreva as alterações:
```sh
$ git commit -m  "inclua a mensagem aqui"
```
Alterando a mensagem de commit:
```sh
$ git commit --amend -m  "inclua a nova descrição da alteração aqui"
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Desfazendo alterações
Retornando o arquivo para antes da edição (antes dele ter sido adicionado a staging area):  
```sh
$ git checkout nome-do-arquivo
```
&nbsp;
Retirando um arquivo da gravação (depois dele ter sido adicionado a staging area):  
```sh
$ git reset HEAD nome-do-arquivo
```
Desfazendo o último commit da gravação  
```sh
$ git reset HEAD~1   
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Exibindo o estado de um arquivo no momento
```sh
$ git status
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Examinando o histórico de alterações   
Visualizando o histórico das alterações realizadas até o momento:
```sh
$ git log   
```
Visualizando o histórico das alterações realizadas apenas em um arquivo específico:
```sh
$ git log nome-do-arquivo  
```
```sh
# para informações das alterações do último commit realizado
$ git show
```
```sh
# para informações das alterações de um arquivo específico
$ git show hash-do-commit  
```
```sh
# para auxiliar com maiores informações sobre os commits realizados 
$ git log -p  
```
```sh
# neste exemplo, para retornar apenas os dois últimos commits
$ git log -p -2  
```
```sh
# para retornar estatísticas sobre os commits realizados
$ git log --stat -2  
```
```sh
# para retornar o log resumido em uma única linha
$ git log --prety-oneline
```
```sh
# neste exemplo, para retornar o log dos commits realizados nos 2 últimos dias
$ git log --since=2.days 
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Comparando diferenças entre arquivos da working area e arquivos da staging area   
```sh
$ git diff
```
```sh
# para informações de um arquivo específico
$ git diff nome-do-arquivo
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;       
### Branches  
Criando uma branch local:
```sh
$ git branch nome-da-nova-branch
```

Acessando uma branch:
```sh
$ git checkout nome-da-branch
```

Criando e sendo redirecionado para uma nova branch:
```sh
$ git checkout -b nome-da-nova-branch
```

Listando todas as branches existentes no repositório: *(branch em trabalho estará destacada em verde, caso haja mais de uma)*
```sh
$ git branch     
```
```sh
# para listar as branches com seus respectivos logs de commits realizados
$ git branch -v   
```

Listando as branches existentes no repositório remoto:
```sh
$ git branch -r    
```

Redirecionando para outra branch do repositório:
```sh
$ git checkout nome-da-outra-branch
```

Voltando para a branch master:
```sh
$ git checkout master    
``` 

Deletando uma branch:
```sh
$ git branch -d nome-da-branch    
``` 
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;       
### Unindo as branches  
Fazendo o merge:
```sh
$ git merge nome-da-branch-a-ser-mesclada    
``` 
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;  
### Remover um arquivo do repositório  
```sh
$ git rm nome-do-arquivo
# além disso, deve ser feito o commit para consolidação da exclusão
``` 
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;  
### Enviando as modificações para o repositório remoto    
Criando um repositório remoto:
```sh
$ git remote add origin colar-link-aqui
# o link acima é o endereço do repositório criado no GitHub
# 'origin' é o nome default do repositório; se desejar, pode ser alterado
```

Enviando os arquivos ou alterações para o repositório remoto:
```sh
$ git push origin master  
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;     
### Criando uma cópia de um repositório remoto para a máquina local
```sh
$ git clone colar-link-do-repositorio-aqui  
# o link acima é o endereço do repositório a ser copiado do GitHub
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Atualizando o repositório local com base nas modificações do repositório remoto
```sh
$ git pull
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Criando um arquivo .gitignore  
```sh
# Se o arquivo for criado pelo terminal:
$ touch .gitignore

# Após criado, incluir ali quais arquivos, pastas ou extensões (ex: *.txt) não se deseja que sejam 'trackeados'.
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Configurando atalhos para comandos Git 
```sh
# o alias pode ser de livre escolha
$ git config --global alias.st status
$ git config --global alias.ci commit
$ git config --global alias.br branch

# depois disso, os comandos assumem os aliases recém-atribuídos
$ git st
$ git ci
$ git br
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Obtendo ajuda com o Git
```
$ git help
```
```
# Caso seja escrito o nome do comando, logo após o git help, abrirá no navegador página do manual com explicações a respeito
$ git help fetch
$ git help diff
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp; 
### Extra: Comandos úteis do Linux  
```
cd - acessar um diretório      
cd.. - sair do diretório  
ls - listar o conteúdo do diretório em que o usuário está no momento (exceto arquivos ocultos)   
ls -a - listar o conteúdo do diretório em que o usuário está no momento (inclusive arquivos ocultos)    
mkdir - criar um diretório   
pwd - informar o diretório em que o usuário está no momento   
touch - para criar um arquivo vazio  
cat - seguido ao nome do arquivo, exibe o conteúdo do arquivo no terminal  
clear - limpar a tela do terminal  
exit - fechar o terminal

# Utilizando o editor de texto Vim:
$ vim nome-do-arquivo - para criar, abrir ou editar um arquivo  
i - para entrar no modo insert  
ESC - para sair do modo insert  
:w - para salvar o arquivo  
:w novo-nome-do-arquivo - para salvar novo nome de arquivo  
:q - para sair do editor  
:wq - para salvar o conteúdo e sair do editor  
 ```
[Voltar ao índice](#Índice)
&nbsp;
     
&nbsp;     
#### :bookmark_tabs: Referências consultadas para criação deste repositório:  
  [Curso de Git (por Fábio dos Reis)](https://www.youtube.com/playlist?list=PLucm8g_ezqNq0dOgug6paAkH0AQSJPlIe)  
  [Git - Documentation](http://git-scm.com/docs)   
  [Git e GitHub para Iniciantes (por Willian Justen)](https://www.youtube.com/playlist?list=PLlAbYrWSYTiPA2iEiQ2PF_A9j__C4hi0A)    
  [GitHub Docs](https://docs.github.com/en/get-started/getting-started-with-git)    
  [Bitbucket Support](https://support.atlassian.com/bitbucket-cloud/docs/git-and-mercurial-commands/)