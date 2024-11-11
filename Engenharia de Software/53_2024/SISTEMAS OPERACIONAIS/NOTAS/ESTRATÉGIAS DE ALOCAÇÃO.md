> **O que é ?**
> A memória RAM utiliza dados do sistema operacional e de processos, logo é preciso armazena-lós para isso existem 3 principais estratégias.

1. [[ALOCAÇÃO CONTÍNUA]]
2. [[ALOCAÇÃO POR SEGMENTOS]]
3. [[ALOCAÇÃO PAGINADA]]

---
#Sistemas_Operacionais/Conceitos 
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





