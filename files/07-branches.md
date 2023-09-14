> **Branches**  
> Repositório: Git: Versionamento básico  
> GitHub: @michelelozada  
&nbsp;
     
&nbsp;  
### Branches  

◦ Criando uma branch local:
```sh

$ git branch nome-da-nova-branch
```

&nbsp;  

◦ Acessando uma branch:
```sh

$ git checkout nome-da-branch
```

&nbsp;  

◦ Criando e sendo redirecionado para uma nova branch:
```sh

$ git checkout -b nome-da-nova-branch
```

&nbsp;  

◦ Listando todas as branches existentes no repositório: *(branch em trabalho estará destacada em verde, caso haja mais de uma)*
```sh

$ git branch     
```

&nbsp;  

◦ Para listar as branches com seus respectivos logs de commits realizados:  
```sh

$ git branch -v   
```

&nbsp;  

◦ Listando as branches existentes no repositório remoto:
```sh

$ git branch -r    
```

&nbsp;  

◦ Redirecionando para outra branch do repositório:
```sh

$ git checkout nome-da-outra-branch
```

&nbsp;  
	
◦ Voltando para a branch master:
```sh

$ git checkout master    
``` 

&nbsp;  

◦ Alterando o nome da branch principal de master (padrão do Git Bash) para main
```sh

$ git branch -M main
``` 

&nbsp;  

◦ Deletando uma branch:
```sh

$ git branch -d nome-da-branch    
``` 

&nbsp;  
       
### Unindo as branches  
◦ Fazendo o merge:
```sh

$ git merge nome-da-branch-a-ser-mesclada    
``` 

&nbsp; 

<div align="center">
<a href="https://github.com/michelelozada/Git-Versionamento-Basico">[Voltar à tela inicial do repositório]</a>
</div>