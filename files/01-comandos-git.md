> **Comandos Git, uma referência rápida**    
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

### git add
Utilizado para adicionar modificações dos arquivos na staging area, preparando-as para o commit.

&nbsp;   

### git branch
Utilizado para criar, listar ou excluir branches no repositório Git atual.

&nbsp; 

### git checkout 
No contexto de branches -> utilizado para alternar entre diferentes branches: altera o HEAD (= o ponteiro atual do Git).
&nbsp; 

No contexto de commits -> utilizado para restaurar arquivos no diretório de trabalho para o estado de um commit específico.

&nbsp; 

### git clone 
Utilizado para copiar um repositório Git remoto para a máquina local.

&nbsp;   

### git commit
Utilizado para gravar as modificações (adicições, modificações e exclusões) feitas nos arquivos adicionados na staging area, criando assim um novo commit no repositório.

&nbsp;   

### git config
Utilizado para definir a identidade do usuário, como nome e email e para setar outras configurações globais e locais do repositório.

&nbsp;   

#### git diff 
Utilizado para exibir as diferenças entre o working directory e a staging area ou entre a staging area e o último commit.

&nbsp;   

#### git fetch
Utlizado para baixar todas as atualizações de um repositório remoto para um repositório local, atualizando o histórico local e as referências de branches, *mas sem aplicar essas mudanças ao  diretório de trabalho nem a branch atual*. Ideal para revisões de  alterações, antes da decisão delas serem mescladas/integradas ao código local.

&nbsp;  

### git init 
Utilizado para inicializar um novo repositório Git em um diretório específico.

&nbsp;   

### git pull
Utilizado para obter as alterações do repositório remoto (ou seja, um `git fetch`) e mesclá-las automaticamente com o repositório local (ou seja, um `git merge`), atualizando-o com as últimas modificações.

&nbsp;   

### git push 
Utilizado para enviar alterações locais para um repositório remoto.

&nbsp;   

### git remote
Utilizado para gerenciar repositórios remotos configurados para o repositório local

&nbsp;   

### git show 
Utilizado para exibir informações detalhadas sobre um commit específico: alterações feitas nos arquivos, autor, data e mensagem do commit.

&nbsp;  

### git status
Utilizado para verificar o estado atual de um repositório local, mostrando quais arquivos foram modificados, adicionados ou removidos em comparação com o último commit.

&nbsp;   

### git switch
Utilizado para alternar entre branches existentes no repositório Git.

&nbsp;   

## Flags 
Uma flag é uma letra ou palavra precedida por um traço (-) ou dois traços (--). Neste contexto, elas são usadas para alterar o comportamento de certos comandos Git.

&nbsp;   

Flag  | Funcionalidade
:---  | :---
-b    | Criação de uma nova branch 
-m    | Inclusão de mensagens diretamente na linha de comando
-v    | (de *verbose*) Fornecer infomações mais detalhadas

&nbsp;   

## Referências consultadas: 
- [Fluxo do GitHub](https://docs.github.com/pt/get-started/using-github/github-flow) em GitHub Docs
- [Os 12 principais comandos do Git que toda pessoa desenvolvedora deve conhecer](https://www.linkedin.com/pulse/os-12-principais-comandos-do-git-que-toda-pessoa-desenvolvedora-6p3we/?trackingId=mQZazTfsp%2FLX1UcV1ru8Cg%3D%3D) por GitHub Brasil 

&nbsp; 

<div align="center">
<a href="https://github.com/michelelozada/Git-Notas-de-Estudo">[Voltar à tela inicial do repositório]</a>
</div>