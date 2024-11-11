---

---
No contexto de sistemas operacionais, a gerência de dispositivos de entrada e saída (E/S) desempenha um papel crucial na interação entre o hardware e o software, proporcionando uma interface que permite a comunicação eficiente e segura entre os diferentes componentes do sistema. Considere os seguintes aspectos:

Fonte: Elaborado pelo Professor, 2024​

**1. Tipos de Dispositivos de E/S:** Explique as principais categorias de dispositivos de entrada e saída (como dispositivos de bloco e dispositivos de caractere) e forneça exemplos de cada tipo. Discuta como as características desses dispositivos influenciam a maneira como o sistema operacional gerencia suas operações.  

**2. Drivers de Dispositivos:** Descreva a função dos drivers de dispositivos no sistema operacional. Como esses drivers facilitam a comunicação entre o sistema operacional e os dispositivos de hardware? Quais são os desafios associados ao desenvolvimento e manutenção de drivers de dispositivos?  

**3. Interrupções e Polling:** Compare e contraste as técnicas de interrupção e polling usadas para gerenciar a comunicação entre o processador e os dispositivos de E/S. Quais são as vantagens e desvantagens de cada abordagem?  
  
Com base nos tópicos mencionados, elabore um texto que explore como um sistema operacional gerencia dispositivos de entrada e saída, destacando os principais desafios e as soluções comuns adotadas para lidar com esses desafios. Utilize exemplos práticos para ilustrar seus pontos e demonstre como a gerência eficaz de E/S pode impactar o desempenho e a estabilidade do sistema como um todo.  

_**Observação**: a entrega da atividade deve ser feita na caixa de texto a seguir. Atente-se, pois após a finalização da atividade, não será possível realizar alterações no texto. Verifique a sua resposta antes de finalizar.  
• Evite compartilhar sua resolução com colegas da turma. A expressão do aprendizado é pessoal e única de cada estudante. Preserve sua autoria e evite transtornos na replicação de sua resposta.  
• Não são permitidas correções parciais no decorrer do módulo, pois a interpretação da atividade também faz parte da avaliação.  
• Atenção ao prazo de entrega da atividade. Sugerimos que envie sua atividade antes do prazo final para evitar transtornos e lentidão nos servidores. Evite o envio de atividade em cima do prazo!_

# Entendimento
---
## Conceito:
### O que é gerência de dispositivos de entrada e saída ?

Função essencial do sistema operacional que envolve o controle, gerenciamento e coordenação dos dispositivos que interagem com o computador como: mouse, teclado, monitor, impressora, scanner, drivers etc...

#### Gerência de dispositivos de entrada e saída envolve tanto os componentes de hardware como os de software

##### Hardware:
###### Dispositivos:
Teclados, mouse, impressora, disco rígido, placa de vídeo etc

###### Controladores de dispositivos:
Controlador do dispositivos que é um pequeno circuito ou chip. Exemplo: A entrada de PCI express da placa mãe. Esse pequeno controlador é responsável por realizar as funções de entrada e saída.

##### Software:
###### Driver de dispositivos:
Programas de software que agem como intermediário entre o sistema operacional e o hardware. Traduz um comando do SO em comando entendível para o dispositivo de hardware específico executar, caso o SO não esteja com driver adequado ele não conseguirá se comunicar adequadamente com o dispositivo de hardware.

ex: nvdia dlls

##### Sistema operacional:
O SO gerencia o uso de dispositivos de E/S, cordenada acesso ao dipsositivos, gernecia interrupções, realiza operações de buffering.
#### Resumindo:

A gerência de dispositivos de E/S não é apenas física ou apenas lógica, mas uma combinação das duas. O hardware fornece os meios físicos para entrada e saída de dados, enquanto o software gerencia, controla e coordena essas operações para garantir que os dispositivos funcionem de forma eficiente e integrada ao sistema como um todo.

### Quais são as principais categorias de dispositivos de entrada e saída ?

#### O que é dispositivo de bloco ?

Dispositivos de hardware que a transferência dos é feita em forma de blocos. A comunição é feita por meio de blocos de dados como SSD, CD-ROM, flash drivers e qualquer outro dispositivo de armazenamento.

Esses utilizam operações de entrada e saída com buffer para otimizar o desempenho de transferência de dados.

Esse blocos são unidade de tamanho fixo. O tamanho varia de 512 bytes a 32 K bytes,  diferentemente dos dispositivos de de caracteres que processam os dados com um fluxo de bytes.  Normalmente armazenados em sistemas de arquivos, organizados em diretórios e arquivos.
#### O que é dispositivos de caractere ?

é aquele dispositivo que **sua comunicação feita através do envio e recebimento de um fluxo de caracteres**. (**Dispositivos interface serial**). 'as implementações desse tipo priorizam a eficiência da comunicação em vez do seu volume, neste sentido, é feita de forma não "bufferizada", sendo assim cada caracter é lido/escrito no dispositivo imediatamente'

**ex:**
	Teclados e mouse são exemplo de dispositivos de caractere, não precisa de buffers

Estes citados acima prioriza comunicação. Contudo existem dispositivos de caracteres que priorizam volume com a impressora, este por exemplo devido a quantidade grande de dados que é maior que sua velocidade de impressão (possui buffer de impressão)

**Dispositivo de caracteres:** É aquele que envia/recebe um fluxo de caracteres, sem considerar qualquer estrutura de blocos, eles não são endereçáveis e não dispõe de qualquer operação de posicionamento. Impressoras e mouses são exemplos desses dispositivos.

### O que é buffer ?
É uma área de memória temporária para armazenar dados enquanto ele estão sendo transferido entre dois locais, como entre dispositivo de entrada/saída e a memória principal do sistema.

O uso de buffers ajuda a coordenar a velocidade de transferência entre diferentes componentes de um sistema de computação, que podem operar em diferentes velocidades.
O que é drivers de dispositivos ? Qual a função deles no sistema operacional ?

### Como esses drivers facilitam a comunicação entre o sistema operacional e os dispositivos de hardware?

#### O que é um driver?
Um _driver_ é um componente de software que permite que o sistema operacional e um dispositivo se comuniquem. Intermediário entre o sistema operacional e o hardware.

#### Como facilitam ?
Os drivers traduzem os comandos do sistema operacional para o dispositivo de hardware, permitindo que o sistema operacional se comunique com o dispositivo conectado. Dessa forma, os drivers permitem que o hardware seja interpretado e gerenciado pelo sistema operacional, garantindo que o dispositivo execute suas funções corretamente. Por exemplo, um driver de placa de vídeo traduz os comandos gráficos do sistema operacional em instruções que a GPU pode entender e processar para exibir gráficos.

### Quais são os desafios associados ao desenvolvimento e manutenção de drivers de dispositivos? 

Os principais desafios no desenvolvimento e manutenção de drivers de dispositivos incluem garantir compatibilidade com diferentes sistemas operacionais e hardware, otimizar o desempenho, gerenciar questões de segurança, realizar testes rigorosos, manter e fornecer suporte contínuo, enfrentar problemas de documentação e complexidade de código, e lidar com questões de licenciamento e propriedade intelectual. Esses desafios exigem habilidades técnicas avançadas e um esforço contínuo para garantir que os drivers funcionem corretamente e atendam às necessidades dos usuários.

### O que é polling ? (interrupções e polling)
#### O que é interrupt ?
São sinais enviados por dispositivos de hardware. os Interrupts são gerados por linhas específicas que existem nos CPUs e microprocessadores e que permitem interromper o funcionamento normal do processador.

### O que é polling ?
**Polling** é uma técnica onde o sistema verifica periodicamente o status de um dispositivo para determinar se há novas informações ou se é necessário realizar uma ação. Em vez de esperar por um sinal do dispositivo, o sistema realiza checagens regulares. Isso pode resultar em uso ineficiente dos recursos e maior latência na detecção de eventos, mas é simples de implementar e controlar.

### Como um sistema operacional gerencia dispositivos de entrada e saída ?


# Resposta:

## 1 )
---

Dispositivos de E/S são dispositivos que se comunicam com o S.O. Ambos podem ser de caractere ou blocos. Os dispositivos de caracteres são aqueles em que a transferência é encaminhada de imediato para o sistema operacional, em grande parte sem a necessidade de buffer, como: mouse e teclado. Estes citados priorizam a comunicação por meio do envio e recebimento de fluxo de caracteres e não tão somente o seu volume, exceto em alguns casos, como impressoras, que, devido à grande quantidade de volume de transferência, é necessário o uso de buffer para otimizar o seu processo de transferência. Por outro lado, existem dispositivos de blocos que funcionam de forma similar à de dispositivos de caractere, porém a transferência é realizada por meio de blocos de dados, como: SSD, placa de vídeo, pendrive, flash drives ou qualquer outro dispositivo de armazenamento. Esses dispositivos de blocos utilizam buffer para otimizar o desempenho de transferência de dados. Esses blocos são unidades de tamanho fixo. O tamanho varia de 512 bytes a 32 KB, diferentemente dos dispositivos de caracteres, que processam os dados com um fluxo de bytes. Normalmente, são armazenados em sistemas de arquivos, organizados em diretórios e arquivos.

## 2 ) 
---

Os drivers traduzem os comando do S.O para o hardware do dispositivo de E/S ele funciona com uma ponte intermediária entre essa comunicação. Desta forma o mesmo interpreta para S.O e hardware e vice-versa, também supervisona o hardware para que o dispositivo E/S funcione perfeitamente. Exemplo: NVIDIA e sua função de DLSS é interpretada pelo driver e o mesmo traduz a instrução para a placa de vídeo fazer o upscale da imagem.

Um dos grandes problema no desenvolvimento e manutenção do sistema operacional é lidar com problemas de licenciamento e propriedade intelectual, ter compatibilidade com inúmero sistemas operacionais e diversos hardwares, ter uma boa otimização, ter uma integridade e blindagem contra problemas de segurança, manter suporte contínuo, lidar com documentação e complexidade de código e etc.

## 3 )
---

Primeiramente, será necessário conhecer o que é polling e interrupt. Polling é uma técnica na qual o sistema verifica a cada tempo estipulado se existe alguma requisição a ser realizada, sem a necessidade do dispositivo solicitar. Diferentemente do interrupt, no qual "são enviados sinais por dispositivos de hardware. Os interrupts são gerados por linhas específicas que existem nos CPUs e microprocessadores e que permitem interromper o funcionamento normal do processador" (ABERTO ATÉ DE MADRUGADA, 2024).

A vantagem do interrupt em relação ao polling é que a requisição somente será encerrada a pedido do dispositivo de hardware. Porém, se houver algum problema no processamento de transferência de dados, o polling será de grande importância na identificação. Afinal, o mesmo verifica, de forma periódica, aqueles dispositivos de E/S.

## Texto Elaborado:
---
Placa de vídeo:

A placa de vídeo é um hardware que se conecta ao PCI Express da placa-mãe do computador. Quando a mesma é conectada ao computador, é necessário o gerenciamento de entrada e saída de transferência de dados, sendo caracterizada como um dispositivo de bloco devido à quantidade de dados que é encaminhada e, por sua vez, à necessidade de utilizar buffer para otimização dessa transferência. Para que a placa de vídeo funcione perfeitamente no computador, é necessário utilizar o driver da placa de vídeo. Esse driver atuará como intermediário entre o sistema operacional e o hardware, de forma que os comandos do sistema operacional sejam traduzidos para o dispositivo de entrada e saída (placa de vídeo). Caso o driver não esteja instalado, há a possibilidade de a placa de vídeo não gerar vídeo ou ficar com uma resolução incompatível com o monitor ou também não apresentar um desempenho adequado nas tarefas que exigem de GPU.


# Referências
---
1. **UNIVERSIDADE FEDERAL DO RIO GRANDE DO NORTE (UFRN).** *Gerência de Dispositivos de Entrada e Saída*. Disponível em: https://materialpublic.imd.ufrn.br/curso/disciplina/5/16/2/7. Acesso em: 22 ago. 2024.

2. **WIKIBOOKS.** *Sistemas Operacionais/Gerência de Dispositivos de Entrada e Saída*. Disponível em: https://pt.wikibooks.org/wiki/Sistemas_operacionais/Ger%C3%AAncia_de_dispositivos_de_entrada_e_sa%C3%ADda. Acesso em: 22 ago. 2024.

3. **MICROSOFT.** *O que é um driver?*. Disponível em: https://learn.microsoft.com/pt-br/windows-hardware/drivers/gettingstarted/what-is-a-driver-. Acesso em: 22 ago. 2024.

4. **CANALTECH.** *O que são drivers?*. Disponível em: https://canaltech.com.br/produtos/o-que-sao-drivers-195604/. Acesso em: 22 ago. 2024.

5. **TOOLIFY.** *Desenvolvimento de Drivers com EDK II: Desafios e Melhores Práticas*. Disponível em: https://www.toolify.ai/pt/hardwarept/desenvolvimento-de-drivers-com-edk-ii-desafios-e-melhores-prticas-3165626. Acesso em: 22 ago. 2024.

6. **TANENBAUM, Andrew S.; BOS, Herbert.** *Operating Systems: Design and Implementation*. 3. ed. São Paulo: Pearson, 2015. ISBN 978-0131429383.

7. **RUSSINOVICH, Mark; SOLOMON, David; IONESCU, Alex.** *Windows Internals*. 7. ed. Redmond: Microsoft Press, 2017. ISBN 978-0735684188.

8. **CORBET, Jonathan; RUBINI, Alessandro; KROAH-HARTMAN, Greg.** *Linux Device Drivers*. 3. ed. Sebastopol: O'Reilly Media, 2005. ISBN 978-0596005900.

9. **HAEUSLER, Martin.** *Driver Development for Windows: A Comprehensive Guide*. Upper Saddle River: Prentice Hall, 2001. ISBN 978-0130679600.

10. **MICROSOFT.** *Driver Development Documentation*. Disponível em: https://docs.microsoft.com/en-us/windows-hardware/drivers/. Acesso em: 22 ago. 2024.

11. **LINUX KERNEL.** *Driver Development*. Disponível em: https://www.kernel.org/doc/html/latest/driver-api/index.html. Acesso em: 22 ago. 2024.

12. **ABERTO ATÉ DE MADRUGADA.** _O que são os interrupts e o polling_. Disponível em: [https://abertoatedemadrugada.com/2012/10/o-que-sao-os-interrupts-e-o-polling.html](https://abertoatedemadrugada.com/2012/10/o-que-sao-os-interrupts-e-o-polling.html). Acesso em: 22 ago. 2024.

13. **RIOS, Vitor.** _Entendendo Polling: Técnicas, Implementações e Alternativas para Comunicação em Tempo Real_. Disponível em: [https://dev.to/vitorrios1001/entendendo-polling-tecnicas-implementacoes-e-alternativas-para-comunicacao-em-tempo-real-3d8n](https://dev.to/vitorrios1001/entendendo-polling-tecnicas-implementacoes-e-alternativas-para-comunicacao-em-tempo-real-3d8n). Acesso em: 22 ago. 2024.

14.  **AMD.** *Polling vs. Interrupts*. Disponível em: https://docs.amd.com/r/en-US/ug1586-onload-user/Polling-vs.-Interrupts. Acesso em: 22 ago. 2024.