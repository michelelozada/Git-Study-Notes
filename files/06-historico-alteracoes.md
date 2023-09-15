> **Examinando o histórico de alterações**  
> Repositório: Git: Versionamento básico  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

**Visualizando o histórico das alterações realizadas até o momento:**  
```sh

$ git log   
```

&nbsp;

**Visualizando o histórico das alterações realizadas apenas em um arquivo específico:**  
```sh

$ git log nome-do-arquivo  
```

&nbsp;

**Para informações das alterações do último commit realizado:**  
```sh

$ git show
```

&nbsp;

**Para informações das alterações de um arquivo específico:**  
```sh

$ git show hash-do-commit  
```

&nbsp;

**Para exibir informações e alterações do commit:**  
```sh

$ git log -p  
```

&nbsp;

**No exemplo abaixo, para retornar apenas os dois últimos commits:**   
```sh

$ git log -p -2  
```

&nbsp;

**Para retornar estatísticas sobre os commits realizados:**  
```sh

$ git log --stat -2  
```

&nbsp;

**Para retornar o log resumido de cada commit em uma única linha:**  
```sh

$ git log --pretty=oneline
```

&nbsp;

**Neste exemplo, para retornar o log dos commits realizados nos 2 últimos dias:**  
```sh

$ git log --since=2.days 
```

&nbsp; 

<div align="center">
<a href="https://github.com/michelelozada/Git-Versionamento-Basico">[Voltar à tela inicial do repositório]</a>
</div>