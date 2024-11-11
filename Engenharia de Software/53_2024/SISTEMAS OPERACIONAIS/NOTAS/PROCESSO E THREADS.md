1. [[CRIAÇÃO DO PROCESSO]]
2. [[TÉRMINO DO PROCESSO]]
3. [[ESTADO DO PROCESSO]]
4. [[PROCESSOS]]
5. [[THREADS]]

> Um processo pode ser considerado um **programa em execução.** 

**É UM PROGRAMA EM EXECUÇÃO**

- **_batch_**
	Somente utilizada em sistemas de grande porte. O sistema operacional irá executar o processo até finalizá-lo para daí começar a executar outro processo. Contudo é inviável para computadores pessoais devido o tempo de espera para usar um programa por vez.

**Estrutura de um processo de memória**

![[Pasted image 20240904205635.png]]

**Seção de Texto**: Código fonte; PC; Conteúdo dos registradores
**Seção de dados**: Variáveis globais
**Seção de Heap**: Alocação dinâmica de memória
**Seção de Pilha**: Parâmetros da função; Variáveis locais e endereços de retorno


#Sistemas_Operacionais/Conceitos 
Sobre Processo: O que é `Seção de texto`?::Área que contém o código do programa. Também inclui o contador do programa e o conteúdo dos registradores do processador.

Sobre Processo: O que é `Seção de dados` ?::Área que contém as variáveis globais.

Sobre Processo: O que é `Heap`?:: representa o espaço para alocação dinâmica de memória durante a execução do processo.

Sobre Processo: O que é `Pilha`?::  Contém os dados temporários (como parâmetros de função, endereços de retorno e variáveis locais).