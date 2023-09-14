> **Trabalhando com o repositório remoto**  
> Repositório: Git: Versionamento básico  
> GitHub: @michelelozada  
&nbsp;
     
&nbsp;
### Enviando as modificações para o repositório remoto  

◦ Criando um repositório remoto:
```sh

$ git remote add origin colar-link-aqui
```

◦ O link acima é o endereço do repositório criado previamente no GitHub  
◦ `origin` é o nome default do repositório; se desejar, pode ser alterado  

&nbsp; 

◦ Listando os repositórios remotos atualmente conectados ao repositório local:  
```sh

$ git remote -v
```

&nbsp;

◦ Enviando os arquivos ou alterações para o repositório remoto:  
```sh

$ git push origin master  
```

&nbsp;

### Criando uma cópia de um repositório remoto para a máquina local
```sh

$ git clone colar-link-do-repositorio-aqui  
```
:bulb: O link acima é o endereço do repositório a ser copiado do GitHub  

&nbsp;
  
### Atualizando o repositório local com base nas modificações do repositório remoto
```sh

$ git pull origin master
```

&nbsp;  

<div align="center">
<a href="https://github.com/michelelozada/Git-Versionamento-Basico">[Voltar à tela inicial do repositório]</a>
</div>