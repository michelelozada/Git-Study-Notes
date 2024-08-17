> **Alterações no Git: examinando o histórico**  
> Repositório: Git - Notas de estudo  
> GitHub: @michelelozada
&nbsp;
     
&nbsp;  

### Visualizando o histórico das alterações realizadas até o momento
```bash

$ git log   
```

&nbsp;

### Visualizando o histórico das alterações realizadas apenas em um arquivo específico
```bash

$ git log nome-do-arquivo  
```

&nbsp;

### Para informações das alterações do último commit realizado
```bash

$ git show
```

&nbsp;

### Para informações das alterações de um arquivo específico
```bash

$ git show hash-do-commit  
```

&nbsp;

### Para exibir informações e alterações do commit
```bash

$ git log -p  
```

&nbsp;

### No exemplo abaixo, para retornar apenas os dois últimos commits
```bash

$ git log -p -2  
```

&nbsp;

### Para retornar estatísticas sobre os commits realizados
```bash

$ git log --stat -2  
```

&nbsp;

### Para retornar o log resumido de cada commit em uma única linha
```bash

$ git log --pretty=oneline
```

&nbsp;

### Neste exemplo, para retornar o log dos commits realizados nos 2 últimos dias
```bash

$ git log --since=2.days 
```

&nbsp; 

<div align="center">
<a href="https://github.com/michelelozada/Git-Study-Notes">[Voltar à tela inicial do repositório]</a>
</div>