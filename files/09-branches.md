> **Branches**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;   

> Cada branch é uma linha de desenvolvimento separada que permite que se trabalhe em funcionalidades específicas do projeto sem interferir diretamente no código principal.

&nbsp;   

> Quando um repositório Git é iniciado e o primeiro commit feito sem a criação explícita de uma nova branch, o Git considera que se trabalhando na branch padrão, que tradicionalmente é chamada de master. Isso significa que todos os commits iniciais são registrados nessa branch principal.

&nbsp;   

> Você pode criar várias branches a partir do repositório principal para trabalhar em diferentes funcionalidades ou correções, e eventualmente mesclar essas branches de volta ao repositório principal.

&nbsp;   

> Branch Local: É a ramificação do seu código que está armazenada no repositório local. 
> Branch Remota: É a versão da branch que está armazenada no repositório remoto (origin). 
> Cada branch local pode ter uma branch correspondente no repositório remoto, que é usada para sincronizar suas mudanças com outros colaboradores.

### Criando uma branch local

↳ *Criando uma branch*
```bash

$ git branch nome-da-nova-branch  
```

&nbsp;  

↳ *Criando e acessando uma branch*
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