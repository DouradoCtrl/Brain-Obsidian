> Threads são uma maneira de permitir que um programa execute várias operações simultaneamente, dentro do mesmo processo. Elas são como "subprocessos" ou "caminhos de execução" que compartilham os mesmos recursos, como memória e arquivos, do processo principal, mas que podem ser executadas de forma independente e, em muitos casos, em paralelo.

>**Processo pode ter várias threads, mas uma thread só pode ter um processo**

- **A atividade de um processo é chamada de thread**

> Em sistemas de processamento em lote (_batch jobs_), é normal cada processo possuir só um thread, já que o processamento não envolve múltiplas atividades.Chamamos os processos desses computadores de _monothread_.
### O que é uma Thread?
Uma **thread** é a menor unidade de execução dentro de um processo, permitindo a execução de múltiplas tarefas simultaneamente no mesmo programa.

### Para que serve?
Threads são usadas para realizar multitarefas dentro de um programa, como manter uma interface responsiva ou processar várias operações ao mesmo tempo.

### Diferença entre Thread e Processo
- **Thread**: Compartilha memória e recursos com outras threads do mesmo processo, tem menos overhead e permite comunicação rápida entre si.
- **Processo**: É independente, com seu próprio espaço de memória; é mais pesado e isolado de outros processos.

> **Os processos competem por espaço (recursos), diferente das threads que compartilham recursos entre si**
