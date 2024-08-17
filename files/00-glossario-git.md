> **Glossário de termos relacionados ao Git**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

## Branch
É uma referência independente a um ponto específico no histórico do código-fonte de um repositório. Ela permite o desenvolvimento paralelo de funcionalidades ou correções sem interferir na branch principal (chamada de master ou main). Cada branch pode ter seu próprio conjunto de commits; e mudanças feitas em uma branch não afetam outras até que elas sejam mescladas.

&nbsp;   

## Changes
Como o nome diz, são consideradas alterações realizadas nos arquivos do diretório de trabalho (working directory).

&nbsp;   

## Clone
O ato de criar uma cópia local completa de um repositório Git existente, incluindo todos os arquivos, histórico de commits e branches. 
  
&nbsp;   

## Commit 
A gravação de alterações feitas no código-fonte de um projeto, que salva um ponto específico na sua 'história' do seu desenvolvimento, acompanhado de uma mensagem descritiva que resume as alterações realizadas. 

&nbsp;   

## Diff
Uma ferramenta/formato de saída que mostra as diferenças entre dois estados do código-fonte/arquivos, destacando adições, remoções e modificações específicas de linhas.

&nbsp;   

## Estado (do repositório)
Condição atual de arquivos, commits e referências (como as branches) dentro de um repositório Git em um determinado momento. Pode mudar conforme novos commits sejam adicionados ou branches sejam criadas.

&nbsp;   
  
## Fetch
Um comando Git que baixa todas as atualizações do repositório remoto para o repositório local, atualizando o histórico local e as referências de branches, *mas sem aplicar essas mudanças ao  diretório de trabalho nem a branch atual*. Ideal para revisões de  alterações, antes da decisão delas serem mescladas/integradas ao código local.

&nbsp;   
  
## Fork 
Uma cópia independente de um repositório Git criada dentro de uma conta no GitHub (ou outra plataforma), permitindo modificações sem afetar o repositório original.

&nbsp;   

## Git
Sistema de controle de versão distribuído, utilizado para o rastreamento de mudanças em arquivos durante o desenvolvimento de software e para colaboração em projetos de código aberto e entre equipes de desenvolvimento. Desenvolvido por Linus Torvalds :heart: em 2005.

&nbsp;   

## GitHub
Plataforma de hospedagem de código, que possibilita p controle de versão, colaboração em equipe, gerenciamento de projetos e funcionalidades como issues, pull requests e integração contínua.

&nbsp;   

## Hash
Um valor único de identificação gerado pelo Git para representar um commit, um arquivo ou um conjunto de dados dentro de um repositório. É uma sequência que identifica de maneira exclusiva conteúdo no Git.

&nbsp;  

## HEAD
É um ponteiro que aponta para o commit mais recente na branch branch atualmente selecionada no seu repositório Git e serve como ponto de partida para novas alterações.

&nbsp;   

## Issues
Funcionalidade do GitHub (e de outras plataformas de hospedagem de código) que permite ao usuário reportar problemas, sugerir melhorias ou discutir ideias relacionadas a um projeto específico.
  
&nbsp;   

## Merge 
Processo de combinar as alterações de uma branch em outra no Git. Isso une o histórico das duas branches e cria um novo commit que incorpora as modificações de ambas, de forma automática quando possível (às vezes pode ser necessário resolver conflitos manualmente).

&nbsp;   

## Origin 
No contexto do Git, é o apelido para o repositório remoto padrão

&nbsp;   


## Pull
*Trazer do remoto para o local*
&nbsp;   

Um comando Git que combina alterações do repositório remoto para o repositório local e atualiza automaticamente o branch local com as modificações mais recentes do repositório remoto.
 
&nbsp;   

## Pull request (PR)
*'Tenho uma contriubuição para você, você aceita?'*
&nbsp;   

É uma solicitação feita por um colaborador de um repositório Git para que as alterações feitas em sua branch sejam incorporadas à branch principal do repositório original. Após revisão, o mantenedor do repositório decide se aceita que estas alterações sejam mescladas.

&nbsp;   

## Push 
*Enviar local para o remoto*
&nbsp; 

Um comando Git que envia as alterações feitas no repositório local para o repositório remoto, atualizando a branch remota com as mudanças feitas localmente.

&nbsp;   

## Repositório
É um local onde todos os arquivos, histórico de versões e metadados de um projeto são armazenados e gerenciados, permitindo o controle de versão e a colaboração entre desenvolvedores. Você transforma um diretório específico em um repositório Git, quando você executa ali `git init`.

&nbsp;   

## Staging area    
Área intermediária no Git onde você prepara seus arquivos antes de confirmar as mudanças definitivamente com `git commit`.

&nbsp;   

## Tracking
Mecanismo que permite que branches locais acompanhem e sincronizem com branches remotas. Ou seja, que uma branch local "trackeie" uma branch remota. 

&nbsp;   

## Versionamento
Processo de rastrear e gerenciar as diferentes versões de um arquivo ou conjunto de arquivos ao longo do tempo. No contexto de controle de versão como Git, isso inclui registrar alterações, revisar históricos, controlar quem fez quais mudanças e revertê-las se necessário, facilitando o desenvolvimento colaborativo e a manutenção de projetos de software.

&nbsp; 

## Working directory (ou working tree)  
É o diretório no seu sistema de arquivos onde você edita e trabalha com os arquivos do projeto. É o estado dos arquivos que você vê e modifica diretamente no seu sistema de arquivos local, refletindo as modificações feitas desde o último commit.

&nbsp; 

## Referências consultadas: 
- [Fluxo do GitHub](https://docs.github.com/pt/get-started/using-github/github-flow) em GitHub Docs  
- [Os 12 principais comandos do Git que toda pessoa desenvolvedora deve conhecer](https://www.linkedin.com/pulse/os-12-principais-comandos-do-git-que-toda-pessoa-desenvolvedora-6p3we/?trackingId=mQZazTfsp%2FLX1UcV1ru8Cg%3D%3D) por GitHub Brasil 

&nbsp; 

<div align="center">
<a href="https://github.com/michelelozada/Git-Notas-de-Estudo">[Voltar à tela inicial do repositório]</a>
</div>