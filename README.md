<div align="center">
	<img src="./assets/git.png">
	<h1>Comandos Git: Versionamento básico</h1>
</div>
&nbsp;
     
&nbsp;       
**1. Configurações iniciais**  
Configurando a identidade do usuário que realizará o versionamento:
```sh
$ git config --global user.name "nome do desenvolverdor aqui"
$ git config --global user.name "email do desenvolvedor aqui"
```
&nbsp;
&nbsp;   
**2. Indicando o repositório que será versionado**  
Inicializando um repositório Git:
```sh
# Criando um diretório
mkdir nome-do-diretorio
# Acessando o diretório
cd nome-do-diretorio/   
# Indicando ao Git que este será o diretório usado para versionamento do projeto
$ git init 
```
&nbsp;
&nbsp;       
**3. Modificando e gravando arquivos**   
Adicionando um arquivo para ser gravado:
```sh
$ git add nome-do-arquivo
```
Realizando a gravação de alteração no projeto junto com uma mensagem de log:
```sh
$ git commit -m  "inclua breve descrição da atualização aqui"
```
Alterando mensagem enviada de commit:
```sh
$ git commit --amend -m  "inclua a nova descrição da atualização aqui"
```
&nbsp;
&nbsp;   
**4. Desfazendo alterações**   
Retirando um arquivo da gravação  
```sh
$ git reset HEAD nome-do-arquivo
```
Retirando um commit (o último) da gravação  
```sh
# aqui é desfeito o último commit
$ git reset HEAD~1   
```
&nbsp;
&nbsp;   
**5. Examinando situações**   
Para exibir aquivos rastreados e/ou atualizações realizadas:
```sh
$ git status
```
Visualizando o histórico das alterações:
```sh
# para listar todo o histórico  
$ git log   
```
```sh
# para auxiliar com mais informações sobre os commits
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
&nbsp;
&nbsp;       
**6. Branches**  
Criando um novo branch:
```sh
$ git branch nome-do-novo-branch
```
Criando e sendo redirecionado para um novo branch:
```sh
$ git checkout -b nome-do-novo-branch
```

Listando todos os branches existentes: *(branch em trabalho estará destacado em verde, caso haja mais de um)*
```sh
$ git branch     
```
```sh
# para listar os branches com seus respectivos logs de commits realizados
$ git branch -v   
```

Redirecionando para outro branch do repositório:
```sh
$ git checkout nome-do-outro-branch
```

Voltando para o branch master:
```sh
$ git checkout master    
``` 
&nbsp;
&nbsp;       
**7. Enviando as modificações**    
Criando um repositório remoto:
```sh
$ git remote add origin colar-link-aqui
# o link cima é o endereço do repositório criado no GitHub
```

Subindo modificações locais para o repositório remoto:
```sh
$ git push origin master  
# irá abrir janela de autenticação do GitHub
```
&nbsp;
&nbsp;     
**8. Baixando arquivos para uma máquina local com Git**
```sh
$ git clone colar-link-aqui  
# o link acima é o endereço do repositório a ser copiado do GitHub
```