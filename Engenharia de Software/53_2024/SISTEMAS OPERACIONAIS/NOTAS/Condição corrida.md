> Quando há uma falha na comunicação e dois processos ou mais processos precisam utilizar do mesmo recurso ao mesmo tempo.
> 
> Ex:  Dois processos tentando acessar um mesmo arquivo.

Todo processo precisa de um espaço em memória durante a sua execução e um pedaço dessa memória é compartilhado entre outros processos. Esse  compartilhamento é chamado de **_região crítica_**.

- **Memória de processos:**
	- Porção alocada para execução
	- Desta porção, um espaço é compartilhado.
## Como evitar ?

Utilizando o princípio da **exclusão mutua**, essa técnica consiste em impossibilitar o processo de acessar uma variável ou arquivo compartilhado na **[[Região Crítica|região crítica]]** ao qual já esteja sendo utilizado por outro processo.

Sim, a **[[exclusão mútua]]** é um dos principais mecanismos usados para proteger a **região crítica**.