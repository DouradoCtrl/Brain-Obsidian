1. [[SOFTWARE DE ENTRADA E SAÍDA]]
2. [[THIN CLIENTS]]
### Dispositivos de Entrada/Saída (E/S)
São aqueles que interagem com o sistema, como mouse, teclado, monitor, disco rígido e relógio do sistema.

### Classificação de dispositivos de E/S (Tanenbaum, 2010)
- **De blocos**: Armazenam dados em blocos de tamanho fixo, como discos rígidos e pen drives.
- **De caractere**: Enviam/recebem um fluxo contínuo de dados, como teclado e mouse.
- Outros dispositivos, como o relógio do sistema, geram interrupções programadas.

### Comunicação e Interrupções
- Dispositivos se conectam à placa-mãe por barramentos, que interligam com o processador e memória.
- Dois controladores, **ponte norte** (alta velocidade, acessa RAM e processador) e **ponte sul** (média/baixa velocidade, USB e PCI), gerenciam essa comunicação.
- **IRQ (Interrupt Request)**: Cada dispositivo que solicita interrupção ao processador é identificado por um número único.
![[hierarquiaES.png]]
# Questões Conceituais
---
#Sistemas_Operacionais/Conceitos 

O que são dispositivos de entrada/saída de blocos? 
??
Dispositivos de blocos armazenam dados em blocos de tamanho fixo, como discos rígidos e Pen Drives.

O que são dispositivos de entrada/saída de caractere?  
??
Dispositivos de caractere enviam ou recebem dados em fluxo contínuo de caracteres, sem estrutura de blocos, como teclados e mouses.

Segundo Tanenbaum (2010, p. 203), quais são as duas categorias de dispositivos de entrada/saída?::Dispositivos de blocos e dispositivos de caractere.

O que são barramentos ?
??
Barramentos são sistemas de comunicação que conectam os componentes de um computador, como processador, memória e dispositivos de entrada/saída. Eles transportam dados, endereços e sinais de controle, permitindo a troca de informações entre esses elementos.
![[Pasted image 20240918193611.png]]

Cite alguns exemplo de barramentos ?::PCI-e, SATA, PS/2, PCI, AGP, ISA, etc.

Qual a diferença de barramento ponte norte e ponte sul ?::Os barramento de ponte norte são aqueles que necessitam de uma taxa de transferência mais alta, como: Processador, RAM, GPU, Monitor. Os barramento de ponte sul, dispositivos de taxa de transferência mais lenta, como: HD, USB, Teclado, Mouse, IDE.

Como é feita essa interação com um processador e os dispositivos de entrada e saída ?::São realizados por meio de interrupções.

Qual é a importância do timer ?
??
- Manter data/hora
- Definir o `quantum` do escalonamento preemptivo.
- Controle de controle de consumo de energia.
- Thins Clients  (terminais burros)

O que são controladores em um sistema de computador ?::Controladores são componentes que gerenciam a comunicação entre o processador e dispositivos, como memória, armazenamento e periféricos, garantindo a troca eficiente de dados.

