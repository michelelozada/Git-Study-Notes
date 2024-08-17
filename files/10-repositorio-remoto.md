> **Trabalhando com o repositório remoto**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;

&nbsp;  

### Enviando as modificações para o repositório remoto  

↳ Estabelecendo vínculo entre repositório local e o repositório remoto:
```bash

$ git remote add origin <URL_do_repositório_remoto> 
```
```bash

# Exemplo Github 
git remote add origin git@github.com:nomedousuario/nome-do-repositorio.git
```

>`origin` é o nome default do repositório remoto; se desejar, pode ser alterado*    
> A URL acima é o endereço do repositório criado previamente no GitHub*    

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

> O comando `git push --set-upstream origin master` define a branch upstream para a branch local master, fazendo com que essa passe a rastrear a branch master no repositório remoto origin. Além disso, há o envio das alterações da branch local (master) para o repositório remoto (origin). Após executar este comando, a branch local master estará configurada para sincronizar automaticamente com a branch master no repositório remoto origin, facilitando o uso de `git push` e `git pull` no futuro sem precisar especificar novamente a branch remota explicitamente.


Ou:
```bash

# Para o caso de uma branch local
git push --set-upstream origin nome_da_branch
```

&nbsp;

> Quando é criada uma nova branch local, ela existe apenas no repositório local até que seja feito um push para o repositório remoto (`git push origin <nome-da-branch-local>`) <- este comando, portanto, estabelece uma conexão entre a branch local e a branch remota.
  
&nbsp;  

> Branch de tracking = é uma branch local configurada para acompanhar uma branch remota específica. Ou seja, a branch local passa a 'trackear' a branch remota. Para obter uma lista das branchs locais e quais delas estão acompanhando branches remotas, maostrando também a diferença entre elas, use `git branch -vv`

&nbsp;  

### Criando uma cópia de um repositório remoto na máquina local
```bash

$ git clone <URL-do-repositorio-aqui>
```
```bash

# Exemplo Github 
$ git clone https://github.com/nomedousuario/nome-do-repositorio.git
```

&nbsp;

> O comando `git clone` não apenas copia o conteúdo do repositório, mas também configura automaticamente um repositório remoto chamado origin (no repositório local), que aponta para o repositório onde o clone foi feito (= para o URL do repositório de onde o clone foi feito). Isso facilita a execução de comandos como `git fetch`, `git pull` e `git push` para sincronizar as alterações entre o repositório local e repositório remoto.
> Portanto, ao clonar um repositório, as branches remotas são automaticamente configuradas para serem seguidas por branches locais com o mesmo nome. 

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