<div align="center">
	<img src="./assets/git.png">
	<h1>Git: Versionamento básico</h1>
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
1. &nbsp;&nbsp;[Comandos encadeados](#Comandos-encadeados)
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
Apagando nome e e-mail setados
```sh
$ git config --global --unset user.name
$ git config --global --unset user.email
```
Listar todas as configurações 
```sh
$ git config --list
```
[Voltar ao índice](#Índice)
&nbsp;
&nbsp;   
### Inicializando um repositório Git 
```sh
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
# para exibir informações e alterações do commit
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
# para retornar o log resumido de cada commit em uma única linha
$ git log --pretty=oneline
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

Altera o nome da branch principal de master (padrão do Git Bash) para main
```sh
$ git branch -M main
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
Listando os repositórios remotos atualmente conectados ao repositório local
```sh
$ git remote -v
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
$ git pull origin master
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
&nbsp;  
**:bulb: Dica:** O site **[gitignore.io](https://www.toptal.com/developers/gitignore/)** gera o conteúdo necessário para arquivos .gitignore, de acordo com a linguagem e com a IDE utilizadas (p. ex.: Java + Eclipse, Python + PyCharm, etc.).    
&nbsp;  
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
### Comandos encadeados  
Para isso, os comandos devem ser concatenados com `&&`, sendo que o comando subsequente só será executado se o anterior for executado sem problemas.  
```sh
$ git add . && git commit -m "Consertada formatação do texto" && git push origin main
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
| Comando | Função
| :---    | :---
| cd      | Seguido ao nome do diretório, acessa-o
| cd ..   | Retrocede um nível de diretório
| cd /    | Acessa o diretório raiz
| ls      | Lista o conteúdo do diretório em que o usuário está no momento *(exceto os arquivos ocultos)*   
| ls -a   | Lista o conteúdo do diretório em que o usuário está no momento *(inclusive os arquivos ocultos)*    
| mkdir   | Cria um diretório   
| touch   | Cria um arquivo vazio  
| mv      | Move um arquivo e/ou diretório
| cat     | Exibe o conteúdo de um arquivo no terminal  
| pwd     | Informa o diretório em que o usuário está no momento   
| clear   | Limpa a tela do terminal  
| exit    | Fecha o terminal

[Voltar ao índice](#Índice)
&nbsp;
     
&nbsp;  
### Utilizando o editor de texto Vim:
| Comando | Função
| :---    | :---
| vim *nome-do-arquivo*  | Abre arquivo
| i                      | Entra no modo insert  
| ESC                    | Sai do modo insert  
| :w                     | Salva o arquivo  
| :w *novo-arquivo*      | Salva novo nome para arquivo
| :q                     | Sai do editor  
| :wq                    | Salva o conteúdo e sai do editor  

[Voltar ao índice](#Índice)
&nbsp;
     
&nbsp;     
<div align="center">

 <details>
 <summary><strong>Clique aqui para ver as referências consultadas para criação deste repositório</strong></summary>

  &nbsp;
  &nbsp;   
  [A Visual Git Reference](https://marklodato.github.io/visual-git-guide/index-en.html)
  [Curso de Git (por Fábio dos Reis)](https://www.youtube.com/playlist?list=PLucm8g_ezqNq0dOgug6paAkH0AQSJPlIe)  
  [Git - Documentation](http://git-scm.com/docs)  
  [Git e GitHub para Iniciantes (por Willian Justen)](https://www.youtube.com/playlist?list=PLlAbYrWSYTiPA2iEiQ2PF_A9j__C4hi0A)  
  [GitHub Docs](https://docs.github.com/en/get-started/getting-started-with-git)  
  
  **Sites para treinar conceitos de Git**      
  [Learn Git Branching](https://learngitbranching.js.org/?locale=pt_BR)  
  [Visualizing Git](https://git-school.github.io/visualizing-git/)    
 </details>

&nbsp;  
[Voltar ao topo](https://github.com/michelelozada/Git-Versionamento-Basico#git-versionamento-básico)

</div>