1. [[PROCESSOS]]
2. [[ESCALONAMENTO DE PROCESSOS]]
3. [[IMPASSE E DEADLOCK]]\


**Processos precisam se comunicar um com os os outro**
- De forma estruturada e sem interrupção

**[[Condição corrida]]**
- Um processo depende do resultado do outro para poder continuar
- Exemplos:
	- Dois processo solicitando a abertura do mesmo arquivo
	- Disputa: Corrupção de dados
	  
- **Como evitar essas condições de disputas ?**
	- Utilizando a [[exclusão mútua]]

**Técnicas de exclusão mútua:** 

1. [[DESABILITAR INTERRUPÇÕES]]
2. [[VARIÁVEL DO TIPO TRAVA (LOCK)]]
3. [[CHAVEAMENTO OBRIGATÓRIO]]
4. [[SOLUÇÃO DE PETERSON]]
5. [[INSTRUÇÃO TSL]]
6. [[SEMÁFOROS E MUTEX]]
7. [[MONITORES]]

#Sistemas_Operacionais/Conceitos 
O que é uma **condição de corrida** ?::é um erro que ocorre quando dois ou mais processos ou threads acessam recursos compartilhados simultaneamente de maneira não controlada, levando a resultados imprevisíveis.

O que é uma **exclusão mútua** ?:: Técnica ao qual os processos são impedidos de acessar uma variável ou arquivo compartilhado na região crítica que já esteja em uso por outro processo.

O que é uma **região crítica** ?:: Pedaço de memória compartilhado entre processos.

Segundo Tanenbaum, o que define uma boa solução para exclusão mútua ?
??
- Dois processos nunca podem estar simultaneamente em suas regiões críticas. 
- Nada pode ser afirmado sobre a velocidade ou sobre o número de CPUs.
- Nenhum processo executando fora de sua região crítica pode bloquear outros processos.
- Nenhum processo deve esperar eternamente para entrar em sua região crítica.

O que é uma trava (lock) e quais são suas vantagens e desvantagens?
??
**Trava (lock)**: Uma variável binária usada para controlar o acesso a uma região crítica, onde um valor 0 indica que a região está disponível e valor 1 indica que está ocupada.
**Vantagens**:
- Simples de implementar.
- Facilita o controle exclusivo de acesso a recursos compartilhados.
**Desvantagens**:
- Pode levar a condições de corrida se a alteração do valor não for atômica.
- Não resolve problemas de espera ativa ou de desempenho se vários processos verificarem a trava simultaneamente.

O que significa desabilitar interrupções para controlar o acesso a uma região crítica e quais são suas limitações?
??
**Desabilitar interrupções**: Impede que outros processos usem a CPU ao desabilitar interrupções enquanto um processo está na região crítica e reabilita-as após a conclusão.
**Limitações**:
- Um processo do usuário poderia ter mais prioridade que um processo que o sistema operacional criou.
- Só é eficaz em sistemas com uma única CPU.

O que é chaveamento obrigatório e quais são suas vantagens e desvantagens?
??
**Chaveamento Obrigatório**: É uma técnica onde um processo realiza uma busca contínua (espera ociosa) para verificar se a região crítica está em uso, utilizando uma variável chamada spin lock (trava giratória).
**Vantagens**:
- Simples de implementar para controle de acesso.
**Desvantagens**:
- **Espera Ociosa**: Consome tempo de CPU desnecessariamente enquanto realiza a busca contínua.
- **Bloqueio Ineficiente**: Pode bloquear processos que não precisam da região crítica, reduzindo a eficiência geral.

O que é a solução de Peterson e como ela controla o acesso à região crítica?
??
**Solução de Peterson**: É um algoritmo para dois processos que controla o acesso à região crítica verificando se há outros processos interessados. O processo interessado entra em uma fila de espera e é executado na ordem de chegada, com o último interessado sendo processado por último.

O que é a instrução TSL e como ela contribui para o controle de exclusão mútua?
??
**Instrução TSL (Test and Set Lock)**: Introduzida no processador Intel 8088, é uma instrução de hardware que lê e atualiza uma variável de trava a cada ciclo de clock da CPU para garantir exclusão mútua. Embora eficaz, pode causar espera ociosa, onde o processo continua verificando a variável mesmo quando não há necessidade de acesso à região crítica. **sleep e wakeup**

O que são semáforos e mutex e como eles funcionam para controlar o acesso a recursos?
??
**Semáforos e Mutex**: Introduzidos em 1965, são técnicas para controle de acesso a recursos. Semáforos são variáveis protegidas acessadas por operações **WAIT()** e **SIGNAL()**, que garantem exclusão mútua e controle de acesso.
- **Semáforos Binários (Mutex)**: Variam entre 0 e 1, usados para garantir exclusão mútua.
- **Semáforos de Contagem**: Controlam o acesso a recursos, com um valor inicial igual ao número de recursos disponíveis, diminuindo com o uso e aumentando com a liberação.
> A operação WAIT() decrementa o valor, enquanto SIGNAL() o incrementa.

O que são monitores e qual é a sua função em relação ao uso de semáforos?
??
**Monitores**: Unidades básicas de sincronização de alto nível criadas para evitar erros de programação ao usar semáforos. Eles garantem o uso correto dos semáforos e são implementados em linguagens como Concurrent Pascal, C#, e Java.

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






