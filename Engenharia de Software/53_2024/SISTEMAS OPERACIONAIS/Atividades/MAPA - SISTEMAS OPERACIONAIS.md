**(1) PRIMEIRA ETAPA: Análise da Situação Problema**  
   
A Importância do Estudo de Programas, Processos e Threads em Sistemas Operacionais  
No âmago dos sistemas operacionais, residem conceitos fundamentais que garantem a execução fluida e eficiente de programas: programas, processos e threads. Dominá-los é crucial para desvendar os mecanismos internos que transformam linhas de código em ações tangíveis e experiências digitais.  
Estudar esses elementos permite aos desenvolvedores entenderem como os sistemas operacionais dão vida aos programas. Eles desvendam como os recursos do computador são alocados e gerenciados, garantindo que cada programa funcione de forma isolada e eficiente, mesmo quando diversos estão em execução simultânea.  
Dominar os conceitos de programas, processos e threads em sistemas operacionais não se limita apenas à criação de software. É uma jornada para desvendar os segredos do funcionamento interno dos computadores, capacitando analistas e desenvolvedores a construir sistemas robustos, eficientes e escaláveis que moldam o mundo digital em que vivemos.

Fonte: Elaborado pelo Professor, 2024

  
**(2) SEGUNDA ETAPA: Realização da atividade**  
   
**Objetivo:**  
- Compreender os conceitos fundamentais de programas, processos e threads em sistemas operacionais.  
- Diferenciar os termos com base em suas características e funcionalidades.  
- Analisar as diferenças entre threads de usuário e threads de kernel em termos de implementação e gerenciamento.  
   
**Tarefas:**  
Com base no material da disciplina, nas referências bibliográficas e pesquisa em outras fontes, elabore um relatório com a estrutura a seguir, respondendo cada um dos questionamentos.  
   
**1. Definição e Diferenciação:**  
**- Programa:** Descrever o que é um programa, sua natureza e função.  
**- Processo:** Apresentar a definição de processo, seus componentes principais e características.  
**- Thread:** Conceituar thread, destacando suas características, diferenças em relação a processos e relevância na programação.  
**- Quadro Comparativo:** Elaborar um quadro comparativo resumindo as principais diferenças entre programa, processo e thread. Pesquise sobre as seguintes características: natureza, granularidade, uso de recursos, criação/destruição, isolamento e concorrência.  
**2. Implementação de Threads:**  
**- Threads de Usuário:** Explique o que são threads de usuário, como são implementadas e gerenciadas pelo programador.  
**- Threads de núcleo:** Descrever threads de kernel (núcleo), detalhando seu funcionamento e gerenciamento pelo sistema operacional.  
**- Comparação:** Comparar e contrastar threads de usuário e threads de kernel, considerando aspectos como:  
-> Localização da tabela de processos e threads;  
-> Mecanismos de troca de contexto;  
-> Sincronização entre threads;  
-> Gerenciamento de prioridades; e  
-> Vantagens e desvantagens de cada tipo de thread.

# Definição e diferenciação
---
**Programa:** Um programa é uma aplicação que possui toda a lógica de algoritmos necessária para ele funcionar e executar determinada tarefa. Vale ressaltar que um programa é construído com base em alguma linguagem de programação adequado aquela finalidade seja: Java, C#, Python e entre outros.

**Processo:** Um processo é basicamente um programa em execução, ele utiliza de recursos como tempo de CPU, memória, arquivos e dispositivos de entrada e saída para executar a tarefa requisitada. O processo pode ser instanciado tanto pelo usuário ao solicitar a execução de um programa ou em segundo plano para o funcionamento do sistema operacional ou também instanciado por um outro programa. Um programa é independente e possui seu próprio espaço de memória, diferentemente dos threads, ele é mais pesado e isolado. Os processos competem por recursos. 

Vale ressaltar que um processo possui estados de funcionamento como: Novo, em execução, em espera e pronto. Esses estados podem mudar à medida que o processo recebe respostas do sistema operacional e se comunica com o usuário, incluindo interações com dispositivos de entrada e saída.

Um processo possui uma estrutura composta por: Texto, dados, heap e pilha. Os campos heap e pilha são alocados dinâmicamente, visto que, a depender da demanda de execução, ele irá consumir mais ou menos da memória primária.

A depender do sistema operacional e do tipo máquina ao qual o programa está sendo executado, haverá um ordem de prioridade de processo a serem processados. Dependerá da máquina e do sistema operacional se o processo será executado de forma preemptiva,  como em sistemas batch, ou utilizando de escalonamento de processos, como em computadores pessoais.

Como citado a acima os processo competem por recursos dessa forma, os mesmo estão sujeitos a empecilhos em sua execução como condições de corridas ou impasses. O sistema operacional que será responsável por executar esses processos e evitando esses tipos de problemas assim e também lidando com a fragmentação de memória.

**Thread:** Threads são partes de um processo, são considerados como "mini processos" ele permite que sejam executadas várias operações em simultâneo. Um processo pode conter diversos threads mas um thread possui um processo apenas. A maior de diferença entre threads e processos é que os threads compartilham recursos, ou seja: tempo de CPU, memória, arquivos e dispositivos de entrada e saída. Diferentemente dos processos que competem por recursos constantemente em tempo de execução.

Devido aos threads conseguirem acessar os mesmo endereços de memória, compartilhando dados e códigos as suas atividades podem reduzir o tempo de execução de um processo.

**Quadro comparativo:**

| Termo                  | **Significado**                                            |
| ---------------------- | ---------------------------------------------------------- |
| **Natureza**           | Característica fundamental ou essência de algo.            |
| **Granularidade**      | Nível de detalhe ou divisão de uma unidade de trabalho.    |
| **Uso de Recursos**    | Como e quanto um componente consome recursos do sistema.   |
| **Criação/Destruição** | Processo de iniciar ou finalizar a existência de algo.     |
| **Isolamento**         | Grau em que uma unidade é separada de outras unidades.     |
| **Concorrência**       | Capacidade de executar múltiplas operações ao mesmo tempo. |

| Características                   | Programa                                                                                       | Processo                                                                         | Thread                                                                                                               |
| --------------------------------- | ---------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Natureza**                      | Entidade passiva, contendo uma lista de instruções (linguagem de programação) em disco rígido. | Entidade ativa, contendo instruções de código de máquina                         | Compartilham de recursos entre si no mesmo endereço alocado pelo processo.                                           |
| **Granularidade**                 | Conjunto de intruções.                                                                         | Execução do programa em uma pedaço de memória alocado.                           | Execução dentro de um processo em uma memória já alocada compartilhando recuros.                                     |
| **Uso de recursos**               | Utiliza-se do armazenamento secundário.                                                        | Utiliza-se da memória principal, alocação de memória.                            | Utiliza-se da memória principal mas compartilham recursos entre si, sem necessidade alocação de memória para threads |
| **Criação/Destruição (Overhead)** | Executado na memória secundária até ser convertido em um processo.                             | Maior sobrecarga, pois competem por recursos.                                    | Menor sobrecarga, compartilham do mesmo endereço.                                                                    |
| **Isolamento**                    | Não tem isolamento.                                                                            | Processos são isolados na memória.                                               | Thread compartilham recursos de um processo. (mesmo espaço de memória)                                               |
| **Concorrência**                  | Apenas a execução de um programa.                                                              | Podem executar múltiplas operações mas precisam estar presente no escalonamento. | Diversas, podem ser executas paralelamente e compartilhar recursos.                                                  |

# Implementação de Threads
---
**2. Implementação de Threads:**  
**- Threads de Usuário:** Explique o que são threads de usuário, como são implementadas e gerenciadas pelo programador.  
**- Threads de núcleo:** Descrever threads de kernel (núcleo), detalhando seu funcionamento e gerenciamento pelo sistema operacional.  
**- Comparação:** Comparar e contrastar threads de usuário e threads de kernel, 

**Threads de usuário:** Threads de Usuário são threads criadas e escalonadas sem o conhecimento do kernel, ou seja é uma camada acima de kernel com menos permissões entretanto, desenvolvedores utilizam de bibliotecas em suas aplicações para que seja possível criar e manipular threads de usuário. Dessa forma proporciona maior velocidade na execução do programa e mais otimização no sistema aplicado. Um desvantagem desse tipo de thread é que caso ela acesse uma funcionalidade ao qual não tem permissão destinada ao acesso do kernel por exemplo, a thread bloqueia todo o programa, encerrando seu funcionamento. Uma linguagem de programação que é referência em velocidade de compilação e utiliza de thread de usuário em aplicações é a linguagem RUST.

**Threads de Kernel:** São gerenciadas diretamente pelo sistema operacional (kernel). Elas têm acesso direto ao hardware da máquina, permitindo interações com registradores e interrupções. O kernel é por controlar essas threads. Elas podem se relacionar com diversas threads de usuário podendo ter de um-para-muito ou até mesmo muito-para-muitos em máquinas multithreading.

**Comparação:**

| Índices                                          | Threads de Usuário                                                                     | Threads de Kernel                                              |
| ------------------------------------------------ | -------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| **Localização da Tabela de Processos e Threads** | Administradas nível usuário (Programador).                                             | Administradas pelo kernel (sistema operacional).               |
| **Mecanismos de Troca de Contexto**              | Limitada não possui tanto acesso a nível do kernel                                     | Possui acesso total a máquina e ao hardware.                   |
| **Sincronização entre Threads**                  | Sincronizada pela biblioteca da linguagem de programação utilizada pelo desenvolvedor. | Sincronização efetuada pelo sistema operacional.               |
| **Gerenciamento de Prioridades**                 | Prioridades baixas, o sistema operacional se quer sabe das threadas.                   | O kernel gerencia a prioridade.                                |
| **Vantagens**                                    | Rápido para criar e excluir.                                                           | Maior acesso no hardware e funções do sistema operacional      |
| **Desvantagens**                                 | Menor acesso as funções de sistema operacional e hardware.                             | Existe um custo adicional na sua utilização, sendo mais lenta. |

# Referências
---
1. **NFO94.** O que é um processo em um sistema operacional. *DEV*. Disponível em: <https://dev.to/nfo94/o-que-e-um-processo-em-um-sistema-operacional-2769>. Acesso em: 13 set. 2024.

2. **GRANCURSOSONLINE.** Sistemas operacionais: gerenciamento de processos. *Blog Gran Cursos Online*. Disponível em: <https://blog.grancursosonline.com.br/sistemas-operacionais-gerenciamento-de-processos/>. Acesso em: 13 set. 2024.

3. **MICROSOFT.** Threads and threading. *Microsoft Learn*. Disponível em: <https://learn.microsoft.com/pt-br/dotnet/standard/threading/threads-and-threading>. Acesso em: 15 set. 2024.

4. **TAKE U FORWARD.** Difference between process, program, and thread: different types. *Take U Forward*. Disponível em: <https://takeuforward.org/operating-system/difference-between-process-program-and-thread-different-types/>. Acesso em: 15 set. 2024.

5. **BACKBLAZE.** What’s the diff? Programs, processes, and threads. *Backblaze Blog*. Disponível em: <https://www.backblaze.com/blog/whats-the-diff-programs-processes-and-threads/#:~:text=Computer%20processes%20are%20independent%20program,easier%20but%20requiring%20careful%20synchronization>. Acesso em: 15 set. 2024.

6. **IBM.** Processes, kernel threads, and user threads. *IBM Documentation*. Disponível em: <https://www.ibm.com/docs/en/aix/7.3?topic=processes-kernel-threads-user-threads>. Acesso em: 15 set. 2024.

7. Prof. Santiago - Programação e Ciência. Definição de Threads e Diferença entre Thread de Usuário e de Kernel - SISTEMAS DE COMPUTAÇÃO. Youtube, 21 de dez. 2021. Disponível em: <https://youtu.be/jFgTdn5Qu4w?si=SgkqwEx3nE93fr0G>. Acesso em: 15 set. 2024.

8. Código Fonte TV. Thread (entenda como sua aplicação funciona) // Dicionário do Programador. Youtube, 14 de set. de 2020. Disponível em: <https://youtu.be/xNBMNKjpJzM?si=UKQ_aG5gwxvKCTiw>. Acesso em: 15 set. 2024.

9. Prof. Paulo Vitor. Sistemas Operacionais - Threads. Youtube, 14 de nov. de 2020. Disponível em: <https://youtu.be/NRJo-TR28gs?si=8akzZXWDsFrdQwUb>. Acesso em: 15 set. 2024.
