<div align="center">
	<img src="./assets/git.png">
	<h1>Comandos Git: Versionamento básico</h1>
</div>
&nbsp;
     
&nbsp;       
**1 - Configurações iniciais**    
Configurando a identidade do usuário
```
$ git config --global user.name "Nome do desenvolvedor aqui"
$ git config --global user.name "E-mail do desenvolvedor aqui"
```

Iniciando um repositório Git
```
$ git init 
```

Adicionando um arquivo ao repositório
```
$ git add *nome do arquivo aqui*
```
&nbsp;
&nbsp;       
**2. Commits**  
Adicionando um arquivo ao repositório
```
$ git commit -m  *inclua uma breve descrição da versão aqui*  
```
Visualizando o histórico de commits
```
$ git log  
```
&nbsp;
&nbsp;       
**3. Branches**    
Criando uma nova branch
```
$ git checkout -b *nome da nova branch aqui*
```

Listando todas as branches existentes no repositório do computador
```
$ git branch     
```

Redirecionando para outra branch do repositório
```
$ git checkout *nome da branch aqui*
```

Voltando para a branch master
```
$ git checkout master    
```
&nbsp;
&nbsp;       
**4. Outros comandos úteis**  
Subindo modificações ao repositório remoto
```
$ git push origin master 
```

Exibindo quais arquivos foram modificados desde o último commit
```
$ git status
```