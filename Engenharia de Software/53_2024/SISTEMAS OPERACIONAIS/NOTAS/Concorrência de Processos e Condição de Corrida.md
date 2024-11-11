### Concorrência de Processos

**Concorrência de processos** refere-se ao **coexistência de múltiplos processos ou threads** em execução ao mesmo tempo. Isso é comum em sistemas multitarefa e multiprocessadores, onde diferentes partes do código podem ser executadas simultaneamente. A concorrência permite que programas realizem múltiplas tarefas de forma eficiente e responsiva.

### Condição de Corrida

**Condição de corrida** é um **problema específico** que ocorre dentro da concorrência quando **múltiplas threads ou processos acessam e manipulam dados compartilhados** ao mesmo tempo, sem a devida sincronização. Isso pode levar a **resultados inesperados ou incorretos** devido à interleaving não controlada das operações.

### Diferença

- **Concorrência de Processos**:
    
    - É uma característica desejável e útil de sistemas que permite a execução simultânea de várias tarefas.
    - Envolve a execução paralela de múltiplos processos ou threads.
- **Condição de Corrida**:
    
    - É um problema que pode surgir na concorrência quando a sincronização adequada não é usada.
    - Refere-se a uma situação onde o comportamento de um programa depende da ordem não controlada de execução das threads ou processos, resultando em erros ou comportamentos incorretos.

### Exemplo:

- **Concorrência**: Em um sistema que executa um servidor web, várias threads podem processar pedidos de diferentes usuários simultaneamente. Isso é desejável e ajuda a melhorar o desempenho e a capacidade de resposta do servidor.
    
- **Condição de Corrida**: Imagine que duas threads estão tentando atualizar a mesma variável global ao mesmo tempo. Se uma thread lê a variável antes da outra atualizar, e ambas escrevem valores diferentes, o resultado final pode ser incorreto. Esse é um exemplo de condição de corrida.

### Resumo

- **Concorrência de processos** é a execução simultânea de múltiplas tarefas.
- **Condição de corrida** é um problema que pode ocorrer quando várias threads/processos acessam recursos compartilhados sem sincronização adequada.