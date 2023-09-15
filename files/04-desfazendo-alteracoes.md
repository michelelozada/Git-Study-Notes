> **Desfazendo alterações**    
> Repositório: Git: Versionamento básico  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

**Retornando o arquivo para antes da edição (antes dele ter sido adicionado a staging area)**  
```sh

$ git checkout nome-do-arquivo
```

&nbsp;

**Retirando um arquivo da gravação (depois dele ter sido adicionado a staging area)** 
```sh

$ git reset HEAD nome-do-arquivo
```

&nbsp;

**Desfazendo o último commit da gravação**   
```sh

$ git reset HEAD~1   
```

&nbsp;

**Removendo um arquivo do repositório**  
```sh

$ git rm nome-do-arquivo

// seguido a isso, deve ser feito o commit para consolidação da exclusão
``` 
&nbsp;

<div align="center">
<a href="https://github.com/michelelozada/Git-Versionamento-Basico">[Voltar à tela inicial do repositório]</a>
</div>