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

---
#Sistemas_Operacionais/Conceitos 
O encerramento do processo ocorre quando o processo completa sua tarefa ou o usuário o fecha voluntariamente, como clicando no "X" no Windows.**Qual tipo de término se caracteriza ?**::Término normal voluntário.

O encerramento do processo ocorre quando o processo detecta um erro fatal, como tentar abrir um arquivo inexistente no Linux, resultando na finalização do processo. **Qual tipo de término se caracteriza ?**::Término por erro voluntário.

O encerramento do processo ocorre quando um programa com autoridade finaliza um processo, como com o comando `kill` no Linux ou "Finalizar Processo" no Windows, geralmente quando o programa não responde. **Qual tipo de término se caracteriza ?**:: Cancelamento por outro processo involuntário.


