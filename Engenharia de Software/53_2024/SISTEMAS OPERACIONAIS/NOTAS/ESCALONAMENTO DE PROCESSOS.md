> Um algoritmo que decide qual processo deve utilizar o processador

**Quatro situações de escalonamento:**
1. Processo foi encerrado
2. Novo processo: decidir entre pai e filho;
3. Bloqueado por E/S
4. Interrupção de E/S

**Preempção:** Cada processo tem um tempo máximo de execução. (quantums)
- Sai da fila, volta pra CPU, fica um tempo, vai pra fila, outro processo volta pra CPU, fica um tempo, volta pra fila....
- Dessa forma permitindo o revezamento
- **Para o usuário é paralelismo, mas na máquina é sequencial**

**Tipo de algoritmos de escalomanto:**
- Preemptivos: processo executa até um tempo máximo
- Não-preemptivos: processo executa até que seja bloqueado ou que encerre.

**Objetivo:**
- **Justiça:** quantums adequados;
- **Eficiência:** CPU 100% ocupada.
- **Tempo de reposta:** Demora pequena;
- **Turnaround:** Tempo pequeno desde a criação do processo e o término
- **Throughput:** Quanto mais processos executando melhor (alta vazão)
  
**Técnica do escalonamento de processos**
1. [[FIRST COME, FIRST SERVED]]

# Questões Conceituais
#Sistemas_Operacionais/Conceitos 
Quais são as quatro situações em que o escalonamento de processos é necessário, conforme definido por Tanenbaum?
??
1. Quando um processo é encerrado.
2. Quando um novo processo é criado e é necessário decidir entre executar o processo pai ou o processo filho.
3. Quando um processo é bloqueado por um dispositivo de entrada/saída.
4. Quando ocorre uma interrupção de entrada/saída.
exemplo:
- **Encerramento de Processo**: Fechar um programa clicando no X no Windows libera o processo e permite escalonar outros.
- **Novo Processo**: Decidir entre atualizar uma base de dados ou iniciar um novo programa.
- **Bloqueio por E/S**: Bloquear processos enquanto um CD está sendo gravado.
- **Interrupção de E/S**: Priorizar a impressão após clicar no botão IMPRIMIR e retornar ao texto depois da conclusão.
  
Quais são as características dos algoritmos de escalonamento preemptivo e não preemptivo?
??
- **Preemptivo**: O processo é executado por um tempo máximo fixado e pode ser interrompido.
- **Não Preemptivo**: O processo é executado até que seja bloqueado ou termine, sem interrupções.
  
O que é o algoritmo "Primeiro a Chegar, Primeiro a Ser Servido" e qual é sua principal desvantagem? Ele é preemptivo ou não preemptivo?
??
**Primeiro a Chegar, Primeiro a Ser Servido (FCFS)**: O processo que chega primeiro na fila é o primeiro a ser processado. A principal desvantagem é a possibilidade de um processo maior atrasar o início de processos menores que chegam posteriormente, resultando em longos tempos de espera para esses processos. Este algoritmo é **não preemptivo**, ou seja, um processo em execução não pode ser interrompido até ser concluído ou bloqueado.

O que é o algoritmo "Tarefa Mais Curta Primeiro" (SJF) e qual é sua principal restrição? 
??
**Tarefa Mais Curta Primeiro (SJF)**: Prioriza a execução da tarefa mais curta entre as disponíveis. Sua principal restrição é que todas as tarefas devem estar simultaneamente disponíveis para serem usadas pela CPU.

O que é o algoritmo "Próximo de Menor Tempo Restante" e qual é a sua principal característica em comparação ao algoritmo "Tarefa Mais Curta Primeiro" (SJF)?
??
**Próximo de Menor Tempo Restante**: Semelhante ao SJF, mas é uma versão **preemptiva**, onde o escalonador seleciona o processo com o menor tempo restante para finalizar, com base no tempo máximo fixado para a execução.

O que é o algoritmo "Chaveamento Circular" (Round-Robin) e como ele difere do FCFS? Ele é preemptivo ou não preemptivo?
??
**Chaveamento Circular (Round-Robin)**: É semelhante ao FCFS, mas **preemptivo**, onde cada processo recebe um tempo fixo chamado quantum para execução. Quando o quantum termina, a CPU é alternada para o próximo processo na fila, permitindo que todos sejam atendidos de forma equitativa.

O que é o algoritmo de escalonamento por prioridade e como ele difere do chaveamento circular?
??
**Escalonamento por Prioridade**: Diferente do **chaveamento circular**, onde todos os processos têm o mesmo tratamento, o escalonamento por prioridade atribui diferentes níveis de importância aos processos, permitindo que o sistema operacional escolha executar processos mais importantes primeiro.

