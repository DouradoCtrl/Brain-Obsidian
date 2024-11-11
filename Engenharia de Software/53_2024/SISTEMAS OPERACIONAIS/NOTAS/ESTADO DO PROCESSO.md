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

![[Pasted image 20240904192901.png]]

---
#Sistemas_Operacionais/Conceitos 
Este estado é atribuído ao processo quando uma das quatro ações de criação de processo ocorre. **Qual é o tipo de estado ?**:: **Novo (new)**

É atribuído pelo sistema operacional quando instruções estão sendo executadas. **Qual é o tipo de estado ?**::**Em execução (running)**

O encerramento do processo ocorre quando um processo aguarda uma resposta externa (dispositivo de E/S), como uma impressora desligada, permanecendo em espera até que a resposta seja recebida.**Qual é o tipo de estado ?**::**Em espera: (waiting)**

O processo está em espera para ser atribuído a um processador quando, por exemplo, a calculadora do Windows é aberta e permanece sem realizar cálculos até que seja escalada para execução.**Qual é o tipo de estado ?**::**Pronto (ready)**

O processo terminou sua execução mediante a ocorrência de alguma das quatro situações de término de processo.**Qual é o tipo de estado ?**::**Concluído (terminated)**

