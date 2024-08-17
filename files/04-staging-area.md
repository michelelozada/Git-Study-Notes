> **Inicializando um repositório Git e adicionando arquivos a staging area**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

### Inicializando um repositório Git  
*Estando na pasta desejada, deve ser indicado ao Git que este será o diretório local a ser usado para o versionamento do projeto.*  
&nbsp;

```bash

$ git init 
```

&nbsp;
     
### Adicionando arquivos não rastreados a staging area  
*Ao executar o comando `git add`, o Git analisa o estado atual do(s) arquivo(s) no diretório e adiciona todas as modificações (adições, modificações e exclusões) na staging area. Isso significa que estas mudanças passam a estar preparadas para serem incluídas no próximo commit.*

&nbsp;

↳ Adicionando um arquivo específico (por nome)  
```bash

$ git add nome-do-arquivo
```
&nbsp;

↳ Adicionando todos os arquivos de um diretório, de acordo com a sua extensão  
```bash

$ git add *.py
$ git add *.js
```
&nbsp;

↳ Adicionando todos os arquivos de uma só vez  
```bash

$ git add .
```

&nbsp;

### Exibindo arquivos que estão na staging area, mas que ainda não foram commitados  

```bash

$ git diff --staged
```

&nbsp;

### Retirando um arquivo específico da staging area  

```bash

$ git rm --cached nome-do-arquivo
```

&nbsp;

<div align="center">
<a href="https://github.com/michelelozada/Git-Study-Notes">[Voltar à tela inicial do repositório]</a>
</div>