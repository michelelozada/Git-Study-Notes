<div align="center">
	<img src="./assets/git.png">
	<h1>Comandos Git: Versionamento básico</h1>
</div>
&nbsp;
     
&nbsp;       
**1. Configurações iniciais**  
Configurando a identidade do usuário
```
$ git config --global user.name "nome do desenvolverdor aqui"
$ git config --global user.name "email do desenvolvedor aqui"
```

Transformando uma pasta em um repositório Git:
```
$ git init 
```

Adicionando um arquivo ao repositório:
```
$ git add nome-do-arquivo
```
&nbsp;
&nbsp;       
**2. Modificando e gravando arquivos** 
Realizando alteração no repositório
```
$ git commit -m  "inclua breve descrição da atualização aqui"
```
Para exibir aquivos rastreados e atualizações realizadas 
```
$ git status
```
Visualizando o histórico de commits
```
$ git log  
```
```
$ git log p  <- auxilia com mais informações sobre os commits
```
&nbsp;
&nbsp;       
**3. Branches**    
Criando uma nova branch
```
$ git checkout -b nome-da-nova-branch
```

Listando todas as branches existentes *(branch atual estará destacada em verde)*
```
$ git branch     
```

Redirecionando para outra branch do repositório
```
$ git checkout nome-da-branch
```

Voltando para a branch master
```
$ git checkout master    
```
&nbsp;
&nbsp;       
**4. Enviando as modificações**  
Criando repositório remoto 
```
$ git remote add origin colar-link-aqui   <- este link é o endereço do repositório no GitHub
```

Subindo modificações locais para o repositório remoto 
```
$ git push  
```
&nbsp;
&nbsp;     