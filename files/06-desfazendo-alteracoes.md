> **Desfazendo alterações**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

### Retornando o arquivo para antes da edição (antes dele ter sido adicionado a staging area)
```bash

$ git checkout nome-do-arquivo
```

&nbsp;

### Retirando um arquivo da gravação (depois dele ter sido adicionado a staging area) 
```bash

$ git reset HEAD nome-do-arquivo
```

&nbsp;

### Desfazendo o último commit da gravação   
```bash

$ git reset HEAD~1   
```

&nbsp;

### Removendo um arquivo do repositório  
```bash

$ git rm nome-do-arquivo
``` 
↳ *Seguido a isso, deve ser feito o commit para consolidação da exclusão*

&nbsp;

<div align="center">
<a href="https://github.com/michelelozada/Git-Study-Notes">[Voltar à tela inicial do repositório]</a>
</div>