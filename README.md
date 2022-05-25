<div align="center">
	<img src="./assets/git.png">
	<h1>Comandos Git: Versionamento básico</h1>
</div>
&nbsp;
     
&nbsp;       
**1. Configurações iniciais**  
Configurando a identidade do usuário
```
$ git config --global user.name "nomeDoDesenvolverdorAqui"
$ git config --global user.name "emailDoDesenvolvedorAqui"
```

Transformando uma pasta em um repositório Git:
```
$ git init 
```

Adicionando um arquivo ao repositório:
```
$ git add nomeDoArquivoAqui
```
&nbsp;
&nbsp;       
**2. Modificando e gravando arquivos** 
Realizando alteração no repositório
```
$ git commit -m  "incluaBreveDescricaoDaAtualizacaoAqui"
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
$ git log p  <- auxilia com mais informações
```
&nbsp;
&nbsp;       
**3. Branches** 
Criando uma nova branch
```
$ git checkout -b nomeDaNovaBranchAqui
```

Listando todas as branches existentes **(branch atual está destacada em verde)**
```
$ git branch     
```

Redirecionando para outra branch do repositório
```
$ git checkout nomeDaOutraBranchAqui
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
$ git remote add origin colarLinkAqui   <- este link é o endereço do repositório no GitHub
```

Subindo modificações locais para o repositório remoto 
```
$ git push  
```
&nbsp;
&nbsp;     