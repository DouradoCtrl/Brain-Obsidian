#Sistemas_Operacionais/Livros 

# Unidade 1

O que são sistema operacionais ?
??
É o principal software de um dispositivo computacional. Podemos definir um SO de acordo com suas funcionalidades: é um gerenciador de recursos e ao mesmo tempo uma camada de abstração.

Descreva pelo menos dois sistemas operacionais, o nome dos SO e suas particularidades.
??
Microsoft Windows: sistema operacional proprietário; Atualmente da supor- te aos sistemas de arquivos FAT32 e/ou NTFS (Windows 10); É propriedade da Microsoft e opera sob uma licença paga; O fundador da Microsoft é Bill Gates. Linux: baseado em Unix; Primeira versão por Linus Torvalds em 1991; É open scource e opera sob a licença GNU CPL; Possui um kernel não comercializável; Várias distribuições.

O Android pertence unicamente ao Google? Pesquise pelo menos três membros da OHA que você conheça.
??
HTC, Dell, Motorola, Intel, Qualcomm, Samsung, etc.

# Unidade 2

Diferencie processos de threads.
??
![[Pasted image 20240918222058.png]]

Como um processo pode ser iniciado? E como pode ser finalizado?
??
Criação: Início do Sistema; Requisição de um usuário; Criação de um processo por outro processo; Tarefas em lote. Destruição: Término normal voluntário; Término por erro voluntário; Erro fatal involuntário; Cancelamento por outro pro- cesso involuntário.

O escalonamento do tipo chaveamento-circular (round-robin) utiliza a unidade quantum. Defina o que é um quantum
??
Quantum é o tempo reservado a um processo para que ele seja executado no processador. O quantum é considerado em escalonadores preemptivos como o Round-robin.

O que são semáforos e qual a sua utilidade para os sistemas operacionais?
??
Semáforos são uma técnica de exclusão mútua, implementados por meio e uma variável especial e protegida (abstrata) que pode ser acessada mediante às ope- rações WAIT e SIGNAL(). Servem para coordenar o acesso a algum recurso de uso exclusivo.

Para que ocorra um impasse, quatro situações devem ocorrer. Descreva duas delas.
??
Deve haver exclusão mútua; Deve haver posse e espera; Inexistência de preemp- ção; Deve haver espera circular.

# Unidade 3

Diferencie memórias primárias das memórias secundárias.
??
As memórias primárias são aquelas às quais o processador tem acesso direto. São memórias voláteis e seu custo financeiro é alto, assim como seu consumo de energia. Possuem capacidade de armazenamento reduzida quando comparadas aos dispositivos de memória secundária. As memórias secundárias são aquelas com as quais o processador se comunica através de operações de Entrada/Saída. São dispositivos não voláteis e permitem armazenamento persistente e em mas- sa. Possuem baixo consumo energético e custo financeiro quando comparadas às memórias primárias.

Diferencie fragmentação externa e fragmentação interna.
??
A fragmentação externa são lacunas de memória subutilizadas que se encon- tram fora de qualquer endereçamento de memória reservado a um processo; A fragmentação interna são lacunas de memória subutilizadas que se encontram dentro de um endereçamento reservado a um processo.

Diferencie quadro e página. Estas definições referem-se à estratégia de alocação paginada?
??
Tais conceitos se referem, sim, à alocação de memória paginada. Um quadro é o endereçamento físico, reservado a um processo. A página é o endereçamento lógico de um processo.

Quando vamos instalar um sistema operacional em um disco rígido é comum ser solicitada a formatação do disco antes da instalação propriamente dita. Por que isto é necessário?
??
A formatação padroniza a forma com a qual os setores do disco rígido serão ope- rados. Além disto, a formatação irá fornecer um sistema de arquivos.

Referencie os sistemas de arquivos NTFS, EXT3 e FAT com seus sistemas operacionais.
??
NTFS e FAT: Windows; EXT3: Linux.

# Unidade 4

O que são chipsets? Descreva sobre a função de dois chipsets estudados na gerência de entrada/saída.
??
São controladoras de dispositivos físicos. A ponte norte trabalha com dispositi- vos de alta velocidade. A ponte sul trabalha com dispositivos de média a baixa velocidade.

O que são temporizadores e quais as suas funções?
??
Um temporizador, relógio ou clock é um dispositivo que conta ciclos de clock (ticks de relógio). É a partir desse dispositivo que a máquina é capaz de sincro- nizar seu funcionamento. Além disso, os timers são úteis no escalonamento de processos e monitoramento de consumo de energia.

Podemos afirmar que todos os sistemas operacionais nativamente se comunicam com todos os dispositivos de entrada/saída existentes? O que é utilizado para esta comunicação?
??
Não. Os sistemas operacionais precisam dos device drivers para se comunicar com os dispositivos. Alguns SOs como o Windows e o Linux facilitam a instalação dos drivers. Todavia, os drivers não vêm com todos os SOs de maneira nativa.

Diferencie um sistema operacional protegido de um sistema operacional seguro.
??
Um sistema operacional protegido é aquele que implementa soluções internas para garantir integridade, disponibilidade e confidencialidade de dados. Um sistema operacional seguro está mundo de recursos externos para garantir integridade, disponibilidade e confidencialidade de dados.

Diferencie ataque de ameaça.
??
Uma ameaça é uma vulnerabilidade que ainda não foi explorada por algum agente malicioso. Um ataque é a efetiva utilização da vulnerabilidade para perturbar a integridade, disponibilidade e confidencialidade dos dados.

Diferencie vírus de worm (verme).
??
Virus é uma espécie de malware que tenta se multiplicar dentro da máquina infectada. O worm é um tipo de malware que tenta se multiplicar em várias máquinas, geralmente através de conexões de rede local.

# Unidade 5

Para garantir a performance dos arquivos multimídia, alguns parâmetros devem ser observados. Descreva os quatro parâmetros.
??
Alta vazão, baixa demora, baixa tremulação e alta confiabilidade.

Qual a diferença dos arquivos estudados na unidade III (gerenciamento de arquivos) e os arquivos estudados nesta unidade?
??
Os arquivos estudados na Unidade III eram generalistas e, de modo geral, não aportavam mais de uma mídia em um único arquivo. Os arquivos multimídia, da Unidade V possuem diversas mídias inseridas no mesmo arquivo, sendo que é preciso que haja sincronismo entre a exibição das várias mídias. Outra característica dos arquivos multimídia é que, geralmente, tais arquivos podem ter tamanhos muito grandes quando comparados a outros arquivos.

O que é uma máquina virtual?
??
É uma espécie de duplicata de uma máquina real. É um programa de computador que emula as funções de um hardware ou sistema operacional via software.

Para que serve a partição SWAP? Faça um paralelo com o que já foi estudado em outras unidades.
??
A partição SWAP é o espaço reservado, em disco, para que o SO possa estender a memória RAM de maneira virtual. Essencialmente, esse é o mesmo tema tratado na Unidade III, quando se fala em Memória Virtual e algoritmos de swapping.