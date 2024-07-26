> **Trabalhando com o repositório remoto**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;

&nbsp;  

### Enviando as modificações para o repositório remoto  

↳ Estabelecendo conexão com o repositório remoto: 
```bash

$ git remote add origin <URL_do_repositório_remoto> 
```

*◦ `origin` é o nome default do repositório remoto; se desejar, pode ser alterado*    
*◦ A URL acima é o endereço do repositório criado previamente no GitHub*    

&nbsp; 

↳ Listando os repositórios remotos atualmente conectados ao repositório local:  
```bash

$ git remote -v
```

&nbsp;

↳ Enviando os arquivos ou alterações para o repositório remoto:  
```bash

git push --set-upstream origin master
```
*◦ Após o reconhecimento da branch remota, nas próximas vezes bastará usar apenas o `git push`*  

&nbsp;

### Criando uma cópia de um repositório remoto na máquina local
```bash

$ git clone colar-link-do-repositorio-aqui  
```
*◦ O link acima é o endereço do repositório a ser copiado do GitHub*  

&nbsp;
  
### Atualizando o repositório local com base nas modificações do repositório remoto
↳ *Atualizando a branch local atual com mudanças da branch master do repositório remoto origin*
```bash

git pull origin master
```

&nbsp;

↳ *Atualizando a branch local atual com mudanças da branch remota que ela está configurada para rastrear*
```bash

git pull
```

&nbsp;  

<div align="center">
<a href="https://github.com/michelelozada/Git-Study-Notes">[Voltar à tela inicial do repositório]</a>
</div>