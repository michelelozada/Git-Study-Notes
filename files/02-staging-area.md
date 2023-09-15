> **Inicializando um repositório Git e adicionando arquivos a staging area**  
> Repositório: Git: Versionamento básico  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

#### :pushpin: Inicializando um repositório Git  

Estando na pasta desejada, deve ser indicado ao Git que este será o diretório local a ser usado para o versionamento do projeto  
```sh

$ git init 
```

&nbsp;
     
#### :pushpin: Adicionando arquivos não rastreados a staging area  
◦ Adicionando um arquivo específico (por nome)  
```sh

$ git add nome-do-arquivo
```

&nbsp;

◦ Adicionando todos os arquivos de uma só vez  
```sh

$ git add .
```

&nbsp;

◦ Adicionando todos os arquivos de um diretório, de acordo com a sua extensão  
```sh

$ git add *.py
$ git add *.js
```

&nbsp;

#### :pushpin: Exibindo arquivos que estão na staging area, mas que ainda não foram commitados  
```sh

$ git diff --staged
```

&nbsp;

#### :pushpin: Retirando um arquivo específico da staging area  
```sh

$ git rm --cached nome-do-arquivo
```

&nbsp;

<div align="center">
<a href="https://github.com/michelelozada/Git-Versionamento-Basico">[Voltar à tela inicial do repositório]</a>
</div>