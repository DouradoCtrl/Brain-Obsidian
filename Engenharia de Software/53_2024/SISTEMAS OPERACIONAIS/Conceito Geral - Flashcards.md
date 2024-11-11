#Sistemas_Operacionais/Conceitos
O que é **MMU** ?:: É a unidade de gerenciamento de memória (Memory Management Unit). Ele é responsável por converter o endereço lógico em endereço físico.

O que é um endereço lógico ?::É um endereço virtual que os programa e o sistema entendem e utilizam para acessar a mamória.

O que é um endereço físico ?::É a localização do endereço da memória ram.

O que é fragmentação ?::São buracos vazios na memória RAM. Esses buracos não podem ser utilizados

O que é fragmentação interna ?
??
Quando  um espaço total de um bloco de alocação de memória não é usado por completo.
![[fraginterna.png]]
- Acontece ema alocação contígua

O que é fragmentação externa ?
??
Ocorre quando existem espaços disponíveis na memória em pequenos intervalos não contíguos. 

O que é alocação contínua ?
??
É uma estratégia de alocação que armazena cada arquivo em bloco contíguos (lado a lado)

Qual a vantagem de uma alocação contígua ?
??
Acesso ao dados são rápidos, pois os mesmo estão lado a lado

Qual a desvantagem de uma alocação contígua ?
??
Está sujeito a fragmentação externa e interna.

O que é alocação por segmentos ?
??
É uma estratégia de alocação na qual os segmentos são alocados separadamente na memória. Cada partição se torna uma coleção de segmentos variados.
![[alocacaoPorSegmentos.png]]

Qual a vantagem  da alocação por segmento?
??
Vantagem no redimensionamento de cada segmento pois a alocação de memória se adéqua ao tamanho do segmento.

Qual a desvantagem da alocação externa ?
??
Está sujeita a fragmentação externa.

O que é uma alocação paginada ?
??
É uma estratégia de alocação que divide o endereço lógico em páginas e o endereço físico em blocos (quadros). Cada página é alocado em um determinado quadro. 
![[alocacaoPaginada.png]]

Qual a vantagem de uma alocação paginada ?
??
Permite que o endereçamento físico (memória RAM) seja utilizada de maneira não contígua, evitando a fragmentação externa.

Qual a desvantagem de uma alocação paginada ?
??
Pode gerar Overhead de Gerenciamento de memória.

Para que serve a memória virtual ?::A **memória virtual** utiliza armazenamento externo, como o disco rígido, como extensão da RAM para permitir a execução de mais processos e melhorar o desempenho.

O que é alocação contígua em disco rígido ?::Armazena arquivos em blocos contíguos. Tem um ganho em velocidade de acesso dos arquivos mas está sujeito a fragmentação externa.

O que é alocação encadeada em disco rígido ?::Utiliza um ponteiro para indicar qual é o próximo bloco, desta forma usando todos os blocos e solucionado o problema de fragmentação. Os arquivos são armazenados de forma não contígua espalhadas em disco.

Qual a desvantagem da alocação encadeada em disco rígido ?::Se os blocos ficarem muito espelhados haverá perca de desempenho, pois o braço de leitura do disco irá fazer um esforço maior.
A **FAT** (Tabela de Alocação de Arquivos) armazena informações sobre blocos de arquivos, mas pode causar perda de desempenho em discos grandes devido ao tamanho da tabela.

O que é alocação indexada em disco rígido ?::A **alocação indexada** usa i-nodes para associar arquivos a suas estruturas de dados, reduzindo o espaço e a necessidade de tabelas constantes, sendo comum em sistemas Unix e Linux.
![[alocacaoIndexada.png]]

O encerramento do processo ocorre quando o processo completa sua tarefa ou o usuário o fecha voluntariamente, como clicando no "X" no Windows.**Qual tipo de término se caracteriza ?**::Término normal voluntário.

O encerramento do processo ocorre quando o processo detecta um erro fatal, como tentar abrir um arquivo inexistente no Linux, resultando na finalização do processo. **Qual tipo de término se caracteriza ?**::Término por erro voluntário.

O encerramento do processo ocorre quando um programa com autoridade finaliza um processo, como com o comando `kill` no Linux ou "Finalizar Processo" no Windows, geralmente quando o programa não responde. **Qual tipo de término se caracteriza ?**:: Cancelamento por outro processo involuntário.

Este estado é atribuído ao processo quando uma das quatro ações de criação de processo ocorre. **Qual é o tipo de estado ?**:: **Novo (new)**

É atribuído pelo sistema operacional quando instruções estão sendo executadas. **Qual é o tipo de estado ?**::**Em execução (running)**

O encerramento do processo ocorre quando um processo aguarda uma resposta externa (dispositivo de E/S), como uma impressora desligada, permanecendo em espera até que a resposta seja recebida.**Qual é o tipo de estado ?**::**Em espera: (waiting)**

O processo está em espera para ser atribuído a um processador quando, por exemplo, a calculadora do Windows é aberta e permanece sem realizar cálculos até que seja escalada para execução.**Qual é o tipo de estado ?**::**Pronto (ready)**

O processo terminou sua execução mediante a ocorrência de alguma das quatro situações de término de processo.**Qual é o tipo de estado ?**::**Concluído (terminated)**

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

O que é o algoritmo "Primeiro a Chegar, Primeiro a Ser Servido" e qual é sua principal desvantagem? Ele é preemptivo ou não preemptivo?
??
**Primeiro a Chegar, Primeiro a Ser Servido (FCFS)**: O processo que chega primeiro na fila é o primeiro a ser processado. A principal desvantagem é a possibilidade de um processo maior atrasar o início de processos menores que chegam posteriormente, resultando em longos tempos de espera para esses processos. Este algoritmo é **não preemptivo**, ou seja, um processo em execução não pode ser interrompido até ser concluído ou bloqueado.

O que é o algoritmo "Tarefa Mais Curta Primeiro" (SJF) e qual é sua principal restrição? 
??
**Tarefa Mais Curta Primeiro (SJF)**: Prioriza a execução da tarefa mais curta entre as disponíveis. Sua principal restrição é que todas as tarefas devem estar simultaneamente disponíveis para serem usadas pela CPU.

O que é o algoritmo "Próximo de Menor Tempo Restante" e qual é a sua principal característica em comparação ao algoritmo "Tarefa Mais Curta Primeiro" (SJF)?
??
**Próximo de Menor Tempo Restante**: Semelhante ao SJF, mas é uma versão **preemptiva**, onde o escalonador seleciona o processo com o menor tempo restante para finalizar, com base no tempo máximo fixado para a execução.

O que é o algoritmo "Chaveamento Circular" (Round-Robin) e como ele difere do FCFS? Ele é preemptivo ou não preemptivo?
??
**Chaveamento Circular (Round-Robin)**: É semelhante ao FCFS, mas **preemptivo**, onde cada processo recebe um tempo fixo chamado quantum para execução. Quando o quantum termina, a CPU é alternada para o próximo processo na fila, permitindo que todos sejam atendidos de forma equitativa.

O que é o algoritmo de escalonamento por prioridade e como ele difere do chaveamento circular?
??
**Escalonamento por Prioridade**: Diferente do **chaveamento circular**, onde todos os processos têm o mesmo tratamento, o escalonamento por prioridade atribui diferentes níveis de importância aos processos, permitindo que o sistema operacional escolha executar processos mais importantes primeiro.

O que é um deadlock e quais são as estratégias para preveni-lo?
??
Deadlock ocorre quando dois ou mais processos ficam bloqueados, esperando um pelo outro para liberar recursos. Para preveni-lo, pode-se:
1. **Evitar Exclusão Mútua**: Use recursos apenas se necessário e minimize o número de processos que podem requisitá-los.
2. **Evitar Posse e Espera**: Assegure que um processo não mantenha recursos enquanto espera por outros, ou garanta que todos os recursos necessários sejam alocados de uma vez.
3. **Evitar Inexistência de Preempção**: Permita a retirada de recursos de um processo se necessário para outros.
4. **Evitar Espera Circular**: Imponha uma ordem para requisitar recursos, evitando ciclos de espera.

O que são dispositivos de entrada/saída de blocos? 
??
Dispositivos de blocos armazenam dados em blocos de tamanho fixo, como discos rígidos e Pen Drives.

O que são dispositivos de entrada/saída de caractere?  
??
Dispositivos de caractere enviam ou recebem dados em fluxo contínuo de caracteres, sem estrutura de blocos, como teclados e mouses.

Segundo Tanenbaum (2010, p. 203), quais são as duas categorias de dispositivos de entrada/saída?::Dispositivos de blocos e dispositivos de caractere.

O que são thin clients?
??
Thin clients são computadores que não possuem disco rígido ou sistema operacional próprio. Eles se conectam a um servidor central para acessar aplicativos e dados, compartilhando processador, memória e disco rígido com o servidor. Isso permite melhor gerenciamento e economia de recursos, mas pode resultar em desempenho reduzido devido ao compartilhamento de recursos.

Quais são as quatro camadas do software de entrada/saída?
??
1. **Tratadores de Interrupção**: Garantem que o driver que iniciou a operação de entrada/saída seja bloqueado até sua conclusão.
2. **Drivers**: Código específico para controlar cada tipo de dispositivo de entrada/saída.
3. **Softwares de Entrada/Saída Independente do Dispositivo**: Fornecem funções comuns como armazenar no buffer e reportar erros.
4. **Softwares de Entrada/Saída do Espaço do Usuário**: Trabalham no nível do usuário, usando bibliotecas personalizadas para funções específicas.

O que são barramentos ?
??
Barramentos são sistemas de comunicação que conectam os componentes de um computador, como processador, memória e dispositivos de entrada/saída. Eles transportam dados, endereços e sinais de controle, permitindo a troca de informações entre esses elementos.

Cite alguns exemplo de barramentos ?::PCI-e, SATA, PS/2, PCI, AGP, ISA, etc.

Qual a diferença de barramento ponte norte e ponte sul ?::Os barramento de ponte norte são aqueles que necessitam de uma taxa de transferência mais alta, como: Processador, RAM, GPU, Monitor. Os barramento de ponte sul são dispositivos de taxa de transferência mais lenta, como: HD, USB, Teclado, Mouse, IDE.

Como é feita essa interação com um processador e os dispositivos de entrada e saída ?::São realizados por meio de interrupções.

Qual é a importância do timer ?
??
- Manter data/hora
- Definir o `quantum` do escalonamento preemptivo.
- Controle de controle de consumo de energia.
- Thins Clients  (terminais burros)

O que são controladores em um sistema de computador ?::Controladores são componentes que gerenciam a comunicação entre o processador e dispositivos, como memória, armazenamento e periféricos, garantindo a troca eficiente de dados.

O que são vírus ?:: É Software que se infiltra, se replica e infecta outros programas.

O que é um Worm ?:: Um malware que espalha-se pela rede sem infectar outros programas, buscando ameaças não corrigidas.

O que é um Cavalo de Troia ?:: Um malware que engana o usuário para permitir a entrada de outros malwares, como worms e rootkits.

O que é um Exploit ?::Detecta ameaças não corrigidas para iniciar ataques. Busca vulnerabilidades.

O que é um Packet Sniffer ?::Monitora a rede copiando pacotes de dados.

O que é um Keylogger ?::Malware que captura tudo o que é digitado.

O que é um RootKit ?::Um malware que oculta a presença de intrusos no sistema.

O que é um BackDoor ?::Um malware que abre portas para possibilitar o acesso contínuo e não autorizado.

**O que é proteção ?**
??
A proteção em um S.O fornece mecanismos para imposição das políticas de recursos, como: Leitura, gravação e escrita.
- Implementados pelo Sistema Operacional
- Controle de acesso a dados.
  
**O que é segurança ?**::Quando existem vulnerabilidades que podem ser exploradas, como: Softwares sem licença, patches de segurança, sistema operacional legado.

**O que é ataque ?**
??
É a exploração daquela vulnerabilidade.
- Confidencialidade (Várias pessoas possuem)
- Integridade (Arquivo modificado/Corrompido)
- Disponibilidade (youtube fora)

**O que é ameaça ?**
??
Quando existem vulnerabilidades que podem ser exploradas, como: Softwares sem licença, patches de segurança, sistema operacional legado.

**Sobre proteção e segurança defina: O que é interrupção ?**
??
É um ataque que visa impedir o acesso a determinado serviço. Serviços como DDOS que sobrecarregam servidores para retirar a sua disponibilidade na internet.

**Sobre proteção e segurança defina: O que é interceptação ?**
??
É um malware que quebra a confidencialidade do sistema operacional, acessando informações confidenciais sem modificar. (KeyLogger)

**Sobre proteção e segurança defina: O que modificação ?**
??
É um malware que procura modificar o sistema ou parte dele. (ransomware)

**Sobre proteção e segurança defina: O que fabricação ?**
??
É um malware que tem com objetivo criar informações falsas ou adicionar componentes maliciosos. Exemplo: Inserção de malware no sistema operacional. (Cavalo de troia)






