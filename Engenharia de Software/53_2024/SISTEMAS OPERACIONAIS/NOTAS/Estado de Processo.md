> A técnica de troca de estados foi pensada para entregar o Status da execução do programa.

- **New:**
	Esse estado é atribuído ao processo quando uma das quatro ações de criação de processo ocorre.
- **Runnig:**
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