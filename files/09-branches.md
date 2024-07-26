> **Branches**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;   
### Criando uma branch 

↳ *Criando uma branch local*
```bash

$ git branch nome-da-nova-branch  
```

&nbsp;  

↳ *Criando uma branch local e acessando ela*
```bash

$ git checkout -b nome-da-nova-branch  
```

&nbsp;  

### Acessando uma branch

```bash

$ git checkout nome-da-branch
```

&nbsp;  

↳ *Voltando para a branch master*

```bash

$ git checkout master  
```

&nbsp;  

### Listando todas as branches existentes no repositório
*Caso haja mais de uma, a branch em trabalho estará destacada em verde ou com asterisco*  

```bash

$ git branch     # lista as branches locais    
$ git branch -r  # lista as branches do repositório remoto  
$ git branch -a  # lista as branches locais e remotas 
$ git branch -v  # lista as branches com os logs de commits realizados
```

&nbsp;  

### Alterando o nome da branch principal de master (padrão do Git Bash) para main
```bash

$ git branch -m main
``` 

&nbsp;  

### Mesclando branches
```bash

$ git merge nome-da-branch-a-ser-mesclada    
``` 

&nbsp; 

### Listando as branches que já foram mescladas na branch atual

```bash

git branch --merged
```

&nbsp;

↳ Para listar quais branches não foram mescladas na atual 
```bash

git branch --no-merged 
``` 

&nbsp; 

### Excluindo uma branch

↳ *Excluindo uma branch local*
```bash

$ git branch -d nome-da-branch 
```

&nbsp; 

↳ *Excluindo uma branch remota*
```bash

$ git push origin --delete nome-branch  
``` 

&nbsp; 

<div align="center">
<a href="https://github.com/michelelozada/Git-Study-Notes">[Voltar à tela inicial do repositório]</a>
</div>