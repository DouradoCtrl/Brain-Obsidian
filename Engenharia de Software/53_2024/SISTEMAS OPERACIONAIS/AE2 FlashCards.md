#Sistemas_Operacionais/Questões/AE2 
#### Observe o diagrama esquemático de integração entre componentes em um sistema computacional
![](https://sistemasead.unicesumar.edu.br/flex/amfphp/services/Portal/ImagemQuestionario2/QUE_222310_557840_1.png)
Fonte: o autor.
##### Há três papéis “humanos” apontados – usuário final, programador e projetista de sistema operacional. Todos eles são influenciados pelas decisões de projeto do sistema operacional, pois a depender de técnicas aplicadas no sistema operacional, a programação de utilitários e aplicativos será diferente. De mesma forma, o usuário terá uma percepção diferente do funcionamento geral, por direta influência das decisões de projeto.
###### Dado o contexto, qual é a influência da técnica de multiprogramação em um sistema operacional?
- Alternativa 1: Permite que vários programas sejam executados simultaneamente.
- Alternativa 2: Garante a segurança do sistema contra ameaças.
- Alternativa 3: Aloca recursos de memória de forma eficiente.
- Alternativa 4: Aumenta a velocidade do processador.
- Alternativa 5: Automatiza tarefas repetitivas.
??
- Alternativa 1: Permite que vários programas sejam executados simultaneamente.

---
#### Depois de criado, um processo começa a executar e faz seu trabalho. Contudo, nada é para sempre, nem mesmo os processos. Mais cedo ou mais tarde o novo processo terminará, normalmente em razão de alguma condições. 
Fonte: ​TANENBAUM, A. S. **Sistemas operacionais modernos.** 3. ed. São Paulo: Pearson Education, 2010.
##### Considerando o texto exposto, analise as alternativas a seguir sobre as descrições corretas para encerramento de processos, segundo Tanenbaum (2010): 
I. Término normal voluntário: ocorre quando o processo descobre a existência de um erro fatal, e com isto o estado de encerramento é acionado.
II. Término por erro voluntário: ocorre quando o processo cumpre com êxito a sua finalidade ou então quando o usuário solicita voluntariamente o encerramento do processo.
III. Erro fatal involuntário: ocorre durante a execução de um processo no momento que uma instrução ilegal ou não planejada/testada é executada.
IV. Cancelamento por outro processo involuntário: ocorre quando um processo é finalizado a partir de um determinado programa que possui autoridade para realizar esta finalização, com privilégio superior (super usuário ou administrador).  
###### É correto o que se afirma em: 
- Alternativa 1: I e III, apenas.
- Alternativa 2:III e IV, apenas.
- Alternativa 3: I, III e IV, apenas.
- Alternativa 4: II, III e IV, apenas.
- Alternativa 5: I, II, III e IV.
??
- Alternativa 2: III e IV, apenas.

---
#### No contexto de concorrência entre processos e uso de recursos críticos, Tanenbaum (2010, p. 71) define "que uma boa solução de exclusão mútua deve atender a alguns critérios".  
​Fonte: TANENBAUM, A. S. **Sistemas operacionais modernos**. 3. ed. São Paulo: Pearson Education, 2010.
#### Considerando esta informação, analise os seguintes critérios:  
I. Dois processos nunca podem estar simultaneamente em suas regiões críticas.  
II. Nada pode ser afirmado sobre a velocidade ou sobre o número de CPUs.  
III. Nenhum processo executando fora de sua região crítica pode bloquear outros processos.  
IV. Nenhum processo deve esperar eternamente para entrar em sua região crítica. 
###### É correto o que se afirma em:
- Alternativa 1: I e IV, apenas.
- Alternativa 2: I, II e III, apenas.
- Alternativa 3: I, III e IV, apenas.
- Alternativa 4: II, III e IV, apenas.
- Alternativa 5: I, II, III e IV.
??
- Alternativa 5: I, II, III e IV.

---
#### Em sistemas operacionais temos que apenas um processo pode usar o recurso por vez, ou seja, pelo menos um recurso deve ser mantido em modo não compartilhável. Se outro processo solicitar esse recurso, o processo solicitante deverá ser adiado até que o recurso seja liberado.  
###### Analise as alternativas abaixo e marque a condição descrita acima para evitar deadlock:
- Alternativa 1: Round Robin.
- Alternativa 2: Exclusão mútua
- Alternativa 3: Posse e espera.
- Alternativa 4: Espera circular.
- Alternativa 5: Inexistência de preempção.
??
- Alternativa 2: Exclusão mútua

---
#### O escalonador é responsável por decidir a ordem de execução dos processos prontos, ou seja, que escalona os processos. O escalonamento de processos é realizado por um algoritmo que visa tratar de forma eficiente e rápida os processos a serem tratados.  
###### Com relação ao algoritmo de escalonamento PRIMEIRO A CHEGAR, PRIMEIRO A SER SERVIDO (First Come First Serve – FCFS), assinale a alternativa que possui uma informação ERRADA:
- Alternativa 1: O algoritmo FCFS é preemptivo.
- Alternativa 2: O algoritmo FCFS possui como vantagens o fato de ser simples, fácil de entender e fácil de implementar.
- Alternativa 3: O processo que solicita primeiro a CPU é o primeiro a ser atendido. Isso significa que os processos são atendidos na ordem exata de sua chegada.
- Alternativa 4: Uma vez que um processo é selecionado, esse processo é executado até que seja finalizado ou seja bloqueado por uma E/S ou algum outro evento.
- Alternativa 5: Uma desvantagem do algoritmo FCFS é quando em uma fila existem dois processos de tamanhos distintos e o maior deles é processado primeiro. Dessa forma, o segundo processo ficará aguardando um bom tempo até que o primeiro processo seja finalizado.
??
- Alternativa 1: O algoritmo FCFS é preemptivo.

---
#### É possível descrever conceitualmente as funções do sistema operacional. Sabemos que ele tem as funções básicas. Pensando sobre isso, analise as sentenças a seguir:   
I. Gerencia o uso dos componentes (hardware) de um computador, garantindo sua disponibilidade e armazenamento correto de dados.  
II. Fornece uma camada de abstração para uso de outros softwares.  
III. Fornece uma interface de acesso para dispositivos com tecnologias distintas como USB e IDE.  
IV. Coordena as funções disponíveis para o usuário conforme o ambiente de trabalho atual, quer seja residencial ou mesmo profissional, filtrando pesquisas em ferramentas de busca na Web.  
V. Estabelece regras de funcionamento e operações para softwares comerciais e de entretenimento.  
###### É correto o que se afirma em: 
- Alternativa 1: I, II e III, apenas.
- Alternativa 2: I, III e V, apenas.
- Alternativa 3: II, III e IV, apenas.
- Alternativa 4: I, II, apenas.
- Alternativa 5: I e IIl, apenas.
??
- Alternativa 1: I, II e III, apenas.

---
#### Sabemos que um processo pode ser iniciado e terminado. O sistema operacional sabe se o processo está em execução ou não, por meio da técnica de troca de estados. Silberschatz (2011) define cinco tipos de estados para os processos:  
Fonte: SILBERSCHATZ, A. **Fundamentos de Sistemas Operacionais**. 8. ed. Rio de Janeiro: LTC, 2011.  
![](https://sistemasead.unicesumar.edu.br/flex/amfphp/services/Portal/ImagemQuestionario2/QUE_222310_555889_1.png)
Fonte: Silberschatz (2011, p. 58)
###### Entre os estados possíveis, a definição correta para o estado “Pronto” é
- Alternativa 1: que o processo está esperando ser atribuído a um processador.
- Alternativa 2: como o processo fica após ocorrer uma das quatro ações de criação.
- Alternativa 3: o estado atribuído pelo sistema operacional quando instruções estão sendo executadas.
- Alternativa 4: quando o processo precisa esperar por um recurso lento e/ou externo ao processador.
- Alternativa 5: quando o processo termina de executar seu código.
??
- Alternativa 1: que o processo está esperando ser atribuído a um processador.

---
#### Mecanismos de entrada e saída em hardware são controlados e se comunicam através dos recursos que um sistema operacional oferece. Esses recursos vão desde o que um usuário pode fazer durante a interação com um dispositivo desse tipo, até o que o dispositivo pode oferecer ao usuário.  
​VOLTZ, Wagner Mendes. Sistemas Operacionais. Maringá-PR: UniCesumar, 2018. 
###### Considerando o fragmento de texto acima, analise as afirmativas a seguir sobre a ideia de dispositivos de entrada e saída controlados pelo sistema operacional:   
I – A exibição de uma interface gráfica em um dispositivo de saída como o monitor depende do sistema operacional e não da resolução do monitor.  
II – Dentro da comunicação entre sistema operacional e dispositivos de entrada e saída, um componente essencial para essa comunicação se chama driver.  
III – Os barramentos são responsáveis pela comunicação física entre dispositivos de entrada e saída e a placa mãe que os gerencia em conjunto com o sistema operacional.  
###### É correto o que se afirma em: 
- Alternativa 1: I, apenas.
- Alternativa 2: II, apenas.
- Alternativa 3: I e III, apenas.
- Alternativa 4: II e III, apenas.
- Alternativa 5: I, II e III.
??
- Alternativa 5: I, II e III.

---
#### Um sistema operacional deve ser capaz de administrar a possibilidade de ocorrência de sistemas multiprogramados necessitarem e requisitarem um mesmo recurso simultaneamente. Existem técnicas para impedir que o recurso (arquivo em disco, impressora etc.) seja disponibilizado aos dois processos, pois isso pode ocasionar problemas mais simples, como uma impressão equivocada de conteúdos indesejados, ou travamento de todo o sistema se o recurso bloquear o mesmo enquanto está em uso.  
​VOLTZ, Wagner Mendes. Sistemas Operacionais. Maringá-PR: UniCesumar, 2018.
##### Considerando o texto acima, analise as afirmativas sobre a ideia de condição de corrida contendo opções de solução.  
I – Uma possibilidade é a de que interrupções sejam usadas para resolver o problema devido ao fato de duas interrupções não serem possíveis de ocorrerem ao mesmo tempo.  
II – O uso de uma trava determina que um processo que acessa um recurso indique que o recurso está ocupado através da mudança do valor de um bit indicativo de uso do recurso de 0 para 1.  
III – Há um método que, caso um processo necessite de um recurso, antes é verificado se o mesmo se encontra na chamada região crítica por outro processo estar requisitando-o também, e, caso esteja, ele é enfileirado e aguarda.
##### É correto o que se afirma em:
- Alternativa 1: I, apenas.
- Alternativa 2: II, apenas.
- Alternativa 3: III, apenas.
- Alternativa 4: II e III, apenas.
- Alternativa 5: I, II e III, apenas.
??
- Alternativa 4: II e III, apenas.

---
#### Possuir no seu computador uma CPU muito rápida, de pouco adiantaria se você não tiver uma quantidade considerável de memória para o bom funcionamento do conjunto, dado que a memória e a CPU trabalham em conjunto para garantir rapidez nos processos.    
##### Com relação aos tipos de memória, assinale a alternativa CORRETA:
- Alternativa 1: A memória RAM possui a característica de serem não-voláteis.
- Alternativa 2: Disco rígido, CD-ROM são alguns exemplos de memória secundária.
- Alternativa 3: Um disco rígido de 1 TB (terabyte) é mais caro que uma memória RAM de 1 TB.
- Alternativa 4: Memórias principais são maiores (em capacidade de armazenamento) do que as memórias secundárias.
- Alternativa 5: Memória secundária ou de massa são voláteis, além de mais rápidas se comparadas às memórias principais.
??
- Alternativa 2: Disco rígido, CD-ROM são alguns exemplos de memória secundária.

---
