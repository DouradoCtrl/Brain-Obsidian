> Um processo pode ser considerado um **programa em execução.** Por exemplo: imagine que desejamos ler um livro em nosso computador (os chamados _e-books_). O livro somente poderá ser lido quando ele estiver em execução e para isto é necessário clicar duas vezes sobre ele para a sua abertura. Com isto, um processador de texto será aberto. A partir deste momento temos um processo em execução (no caso o processador de texto com o _e-book_ sendo exibido). E como ele entrou em execução?

**É UM PROGRAMA EM EXECUÇÃO**

- **_batch_**
	Somente utilizada em sistemas de grande porte. O sistema operacional irá executar o processo até finalizá-lo para daí começar a executar outro processo.

# Término do Processo
---
- **Término Normal Voluntário:**
	- Quando o processo é finalizado com êxito ou o usuário solicita
- **Término por erro voluntário:**
	- Quando o processo descobre a existência de um erro fatal. ("Não foi possível abrir esse arquivo").\
	- Um erro tratado com try-cat por exemplo.
- **Erro fatal involuntário:**
	- Quando uma instrução ilegal/não planejada ocorre. Um erro não tratado.
	- Encerramento abrupto do programa
	- Caso a exceção não tenha sido prevista durante o desenvolvimento do software, consideramos como término por erro fatal.
- **Cancelamento por outro processo involuntário:**
	- Ocorre quando um processo é finalizado a partir de um determinado programa que possui autoridade para realizar esta finalização.
	- Ex: Finalizar tarefa do windows no gerenciador de tarefas
	- Ex2: Comando Kill no terminal Linux

# Estado de processo
---
> A técnica de troca de estados foi pensada para entregar o Status da execução do programa.

- **New:**
	Esse estado é atribuído ao processo quando uma das quatro ações de criação de processo ocorre.
- **Running:**
	- Quando as instruções estão sendo executadas
	- Ex: Esperando abrir um programa/arquivo
- **Waiting:**
	- Quando um processo aguarda uma resposta externa
	- Ex: Dispositivo E/S
	- Ex: Solicitação de impressão mas a impressora está desligada (Aguardar inicialização)
- **Ready:**
	- Quando um programa está pronto para ser usado
	- Ex: Calculadora sem cálculo.
- **Terminated:**
	- Término do processo

# Condição de corrida
---
> Quando há uma falha na comunicação e dois processos ou mais processos precisam utilizar do mesmo recurso ao mesmo tempo.
> 
> Ex:  Dois processos tentando acessar um mesmo arquivo.

Todo processo precisa de um espaço em memória durante a sua execução e um pedaço dessa memória é compartilhado entre outros processos. Esse  compartilhamento é chamado de **_região crítica_**.

## Como evitar ?

Utilizando o princípio da **exclusão mutua**, essa técnica consiste em impossibilitar o processo de acessar uma variável ou arquivo compartilhado na **[[Região Crítica|região crítica]]** ao qual já esteja sendo utilizado por outro processo.

Sim, a **exclusão mútua** é um dos principais mecanismos usados para proteger a **região crítica**.

### O que é Exclusão Mútua?
**Exclusão mútua** significa garantir que apenas uma thread ou processo possa acessar a região crítica de cada vez. Isso evita que duas ou mais threads ou processos interfiram entre si ao tentar modificar um recurso compartilhado simultaneamente.

### Como Funciona?
Quando uma thread quer entrar na região crítica, ela precisa primeiro "trancar a porta" usando um mecanismo de exclusão mútua, como uma **trava (lock)**. Enquanto a thread está na região crítica, outras threads são bloqueadas de entrar até que a primeira termine e "destranque a porta", liberando o recurso para a próxima thread.

### Por que é Importante?
A exclusão mútua é fundamental para evitar erros como condições de corrida, onde o resultado do programa depende da ordem imprevisível de execução das threads. Ao garantir que apenas uma thread possa acessar a região crítica por vez, a exclusão mútua mantém a integridade dos dados e o comportamento correto do programa.
### Critérios exclusão mútua:
Segundo Tanenbaum (2010) a exclusão mútua eficiente devem respeitar o seguintes parâmetros.

- Dois processos nunca podem estar  simultaneamente em suas regiões críticas.
- Nada pode ser afirmado sobre a velocidade ou sobre o número de CPUs.
- Nenhum processo executando fora de sua região crítica pode bloquear outros processos.
- Nenhum processo deve esperar eternamente para entrar em sua região crítica.


