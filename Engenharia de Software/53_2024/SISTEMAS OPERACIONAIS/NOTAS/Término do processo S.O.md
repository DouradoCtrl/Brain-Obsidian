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