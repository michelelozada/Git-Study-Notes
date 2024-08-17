> **Fluxo de trabalho no Git**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

## Visão geral do fluxo de trabalho no Git
 Área | Descrição
 ---| ---
Working Tree       | Onde são feitas as modificações nos arquivos
Staging Area       | Onde são preparadas as mudanças para o commit
Local Repository   | Onde são registradas as mudanças
Repositório remoto | Para onde são enviadas/recebidas as mudanças

&nbsp;  

Essas quatro áreas formam um fluxo de trabalho que permite ao Git gerenciar e controlar o versionamento de arquivos de forma eficiente.

&nbsp;  

### • Working Tree (aka Working Directory ou Diretório de Trabalho)
*Diretório onde são criados e editados os arquivos do projeto*

&nbsp;  

É o diretório real no sistema, onde os arquivos do projeto são criados, editados e modificados. Essas modificações são apenas locais. 

&nbsp;  

> As alterações dos arquivos que serão adicionadas ao próximo commit são adicionadas a staging area (ou index) através do comando `git add <arquivo>` - com isso as mudanças saem da working tree para a staging area.

&nbsp;  

### • Staging Area (aka Index)
*Área intermediária para preparação das mudanças antes do commit*

&nbsp;  

A staging area é um espaço temporário onde as alterações do arquivo são armazenadas antes de serem confirmadas, através de um commit.

&nbsp; 

> Após esta etapa, você pode confirmar as mudanças com um commit, através do comando `git commit -m "<mensagem>"` - com isso as mudanças saem da staging area para o local repository. 

&nbsp; 

### • Local Repository (aka Repositório Local)
*Local onde o Git armazena o histórico de commits e os metadados do repositório* 

&nbsp; 

Depois da execução do comando `git commit`, as mudanças preparadas na staging area são registradas aqui, criando um novo commit armazenado no repositório local. Esse commit possui um snapshot das mundanças, uma mensagem descritiva, além de metadados como a data e hora do commit, o autor e um código (hash) único identificador. 

&nbsp;  

O local repository está localizado no diretório .git dentro do diretório do projeto. Esta estrutura interna oculta dentro do diretório do projeto contém todas as informações necessárias para controlar as versões dos arquivos. 
&nbsp;

> A partir daqui, é possível enviar (push) as alterações do repositório local para um repositório remoto ou obter (pull) alterações de um repositório remoto para o repositório local, através dos comandos `git push` e `git pull`, respectivamente.

&nbsp;

### • Remote Repository
*Repositório Git hospedado em servidor remoto, para compartilhar e sincronizar alterações com outros colaboradores* 

&nbsp; 

É uma versão do repositório Git que fica hospedada em um servidor remoto (como no GitHub, GitLab, Bitbucket, entre outros). Esse repositório serve como um ponto central que pode ser acessado e compartilhado entre mais usuários/colaboradores. 

&nbsp;

<div align="center">
<a href="https://github.com/michelelozada/Git-Study-Notes">[Voltar à tela inicial do repositório]</a>
</div>