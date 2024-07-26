> **Configurando atalhos para comandos Git**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;
### Alias
No contexto do Git, são abreviações ou nomes mais curtos e simples que podem ser criados para comandos Git, facilitando assim a utilização de comandos Git.

&nbsp;

↳ O alias pode ser definido por livre escolha (aqui, foi escolhido st, ci e br), seguindo esta sintaxe:
```bash

$ git config --global alias.st status
$ git config --global alias.ci commit
$ git config --global alias.br branch
```

&nbsp;

↳ Depois disso, os comandos assumem então estes aliases recém-atribuídos:
```bash

$ git st
$ git ci
$ git br
```

&nbsp; 

<div align="center">
<a href="https://github.com/michelelozada/Git-Study-Notes">[Voltar à tela inicial do repositório]</a>
</div>