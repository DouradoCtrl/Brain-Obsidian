**Power ON -> Bios -> MBR(Master Boot Record)**

**Alocação contígua**
- Não há separação entre bloco de arquivo
- Armazenado de forma contígua
- Ganho no acesso dos arquivos
- Pesquisa mais rápida
- Sujeito a fragmentação externa

**Alocação encadeada**
- Acaba com a fragmentação
- Utiliza um ponteiro informando o próximo bloco
- Armazenado espalhado no disco
	- Muito espalhado = menos desempenho
- Muito tempo
	- Armazena em **FAT**
		- **FAT => Tabela de alocação de arquivos**
	- Desempenho ruim em discos grandes

**Alocação indexada**
- i-node -> associa cada arquivo em uma estrutura de dados nó-indice
	- Relaciona os atributo e endereços em disco dos bloco de arquivos

![[alocacaoIndexada.png]]

**Diferença entre encadeada e indexada**
- Indexada => não há necessidade de tabelas

> pois o i-node só precisa estar na memória quando o arquivo estiver aberto, com isso o espaço consumido é muito menor do que a tabela FAT, que irá armazenar todas as entradas todo o tempo. Essa estratégia é muito utilizada em sistemas operacionais Unix e seus descendentes, como Linux.


---
# Questões Conceituais
#Sistemas_Operacionais/Conceitos 
O que é alocação contígua em disco rígido ?::Armazena arquivos em blocos contíguos. Tem um ganho em velocidade de acesso dos arquivos mas está sujeito a fragmentação externa.

O que é alocação encadeada em disco rígido ?::Utiliza um ponteiro para indicar qual é o próximo bloco, desta forma usando todos os blocos e solucionado o problema de fragmentação. Os arquivos são armazenados de forma não contígua espalhadas em disco.

Qual a desvantagem da alocação encadeada em disco rígido ?::Se os blocos ficarem muito espelhados haverá perca de desempenho, pois o braço de leitura do disco irá fazer um esforço maior.
A **FAT** (Tabela de Alocação de Arquivos) armazena informações sobre blocos de arquivos, mas pode causar perda de desempenho em discos grandes devido ao tamanho da tabela.

O que é alocação indexada em disco rígido ?::A **alocação indexada** usa i-nodes para associar arquivos a suas estruturas de dados, reduzindo o espaço e a necessidade de tabelas constantes, sendo comum em sistemas Unix e Linux.
![[alocacaoIndexada.png]]


