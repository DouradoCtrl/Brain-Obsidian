#   Unidade 1
#Leitura1 

**Pontos abordados**
- Diagrama de casos de uso
	- Atores
	- UML

## Especificação de Requisitos Funcionais Utilizando Casos de Uso

> Empregar cado de  uso significa que queremos colocar o usuário no centro do processo de coleta de requisito, visando a definir funcionalidade que agreguem valor a esse usuário.

**Etapa I:** Construção de diagrama de casos de uso.
**Etapa II:** Especificação dos requisitos que acompanham o diagrama de caso de uso.

- **Usado para elicitação de requisitos, facilita a compreensão de alguns deles**

###### Características:
- Flexível
- Abstrato
- Informal

##### Etapa 1
###### Estrutura:
- Usuários representados por atores
	->Elementos externos que interagem com o sistema.
- Eclipses
	- Serviço/tarefa/função
	- Texto interno
		- Nome = verbo + substantivo (indicação de ação)
![[Pasted image 20241117115038.png]]
###### Objetivo/Funcionalidade:
- Modelas as  funcionalidades e os serviços oferecidos pelo sistema
- Descreve funcionalidade proposta
- Representa uma única funcionalidade

#### Etapa 2
![[Pasted image 20241117115741.png]]
![[Pasted image 20241117115756.png]]
![[Pasted image 20241117115831.png]]
![[Pasted image 20241117115849.png]]

1. **Identificador único do caso de uso:** Nome do caso de uso, caracteriza a ação que será realizada. **Realizar compra** 
2. **Descrição**: Visão resumida do objetivo
3. **Ator principal**: Inicia o caso de uso (cliente)
4. **Atores secundários**: Participam da execução do cado de uso
5. **Pré-condição:** Condição verdadeira para quer ter o início ao caso de uso.
6. **Pós-condição:** Status final quando finalizada a execução.
7. **Gatilho:** Evento que dá início ao caso de uso. (cado de uso chamado pelo ator principal "realizar compra")
8. **Fluxo principal:** Cenário mais comum do caso de uso. (caminho feliz).
9. **Fluxo alternativos:** Possibilidade de cenários alternativos ao fluxo principal.
10. **Fluxos de exceção:** Como o sistema reagirá a situações inesperadas. (pode ocorrer dentro dos dois tipos de fluxos citados)

## Especificação de Requisitos Funcionais utilizando histórias de usuário.

> São descrições feitas pelos clientes como: funções, as quais os cliente gostariam que o sistema realizasse. 

- **Ponto central:** Está nas necessidades do usuário.

> Reinehr (2020, p. 155) -> “Independentemente da forma que se escolha para realizar as atividades relacionadas a requisitos, um ponto é chave: o foco na entrega de valor para o cliente

**Se não houver valor na entrega ao cliente, ela não dever ser realizada**

**Para que serve ?**
- Elicitação de requisitos
- Estima o quer será realizado para compor o planejamento da **_sprint_**
	- Modelo ágil, scrum.

##### Estrutura 3Cs:
1. Cartão (Card)
	-> Afirmações descritas em primeira pessoa
2. Conversa
3. Confirmação

##### Card
Dividido em **Quem**(papel), **O que**(ação), **Porque**(valor de negócio)
![[Pasted image 20241117122340.png]]
**Quem:** Quem se beneficiará com a  funcionalidade. (tipo de usuário e não quem está solicitando)

**O que:** Descrição da funcionalidade.

**Porque:** Resultado ou o valor agregado à funcionalidade. (O que será entregue ao cliente)

**Elemento mais importante:** Se preocupar com os usuários e os clientes que utilizarão a funcionalidade. Após isso entender  o que deve ser desenvolvido.

---
##### Conversation:
- Ponto de partida para que os requisitos sejam coletados e compreendidos.

##### Confirmação:
- São critérios de aceitação que ajudam a esclarecer como será validada a história de usuário.

Exemplo: 
![[Pasted image 20241117125417.png]]

##### Como construir uma boa história de usuário ?

**Delimite o problema:** Para quem o software está sendo desenvolvido.
**Mapeie a visão geral:** Fazer um mapa que mapeie o mundo com as dores e alegrias dos usuários.
**Explore:** Se aprofundar, como as outras pessoas fazem a mesma coisa.
**Gere uma estratégia de entrega:** Pesquisar antes para construir e priorizar o que agrega mais valor.
**Gere  uma estratégia de aprendizagem:** Produto mínimo viável, aprenda com o teste com público-alvo.
**Gere uma estratégia de desenvolvimento:** Dividir o que será desenvolvido. Desenvolver o que oferece mais riscos primeiro.

##### Características:
- Não detalham as especificações de requisitos
- Curta e fáceis de ler e compreensíveis por stakeholders
- Bem negociável
- Pequenos incrementos de funcionalidade de valor.
- Relativamente fáceis de estimar
- Escritas e organizadas em lista passíveis de serem arrumadas. (just in time)
- Pouca ou nenhuma manutenção.
- Podem ser facilmente descartadas

####

## Especificação de requisitos para um cenários de negócios

**Exemplo:**
![[Pasted image 20241117130716.png]]
**Atores**:
  - **Detran**: órgão responsável pela gestão e fiscalização do trânsito.
  - **Motorista**: pessoa que dirige o veículo e interage com o Detran.
  - **Agente de Trânsito**: responsável pela fiscalização e aplicação das leis de trânsito.
  - **Bancos**: instituições financeiras para pagamento de taxas e multas.
  - **Clínicas Médicas**: responsáveis por realizar exames para renovação da CNH.

**Proprietário**: 
  - É o **dono do veículo**, que pode ou não ser o motorista, dependendo da situação.

##### Processo de elicitação de requisitos:
![[Pasted image 20241117131139.png]]

A seleção das técnicas para coleta de requisitos é essencial para o sucesso de um projeto de sistema. É importante considerar:

1. **Disponibilidade das fontes de informação**.
2. **Tempo disponível para a coleta**.
3. **Contexto do projeto**.
4. **Tipo de informação necessária**.

## Indicadores para avaliar requisitos de software

**Algumas perguntas:**
- Quanto tempo para entregar a funcionalidade ?
- Quantas pessoas são necessária para o projeto ?
- Quanto tempo falta para terminar o projeto ?
- Qual é a produtividade média de equipe ?
- Qual é a gravidade deste risco ?
- Quanto tempo levaríamos para implementar todo backlog do produto?

> **Só é possível controlar aquilo que se consegue medir**
##### Como podemos avaliar os requisitos de software ?
- Investindo na elicitação de requisitos e posteriormente identificar se a equipe de desenvolvimento atendeu às necessidades dos usuários de acordo com o planejado.

| **Termo**                   | **Descrição**                                                                                                                      |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Função de medição**       | Algoritmo ou cálculo realizado para combinar duas ou mais medidas básicas.                                                         |
| **Medição**                 | Função de medição. Algoritmo ou cálculo realizado para combinar duas ou mais medidas básicas.                                      |
| **Medida**                  | Variável à qual um valor é atribuído resultante de uma medição.                                                                    |
| **Procedimento de medição** | Conjunto de operações, descrito especificamente, utilizado no desempenho de determinada medição, de acordo com determinado método. |
| **Valor**                   | Resultado numérico ou categórico atribuído a uma medida básica, medida derivada ou indicador.                                      |
Para medir a produtividade de um stakeholder em relação à sua equipe de desenvolvimento, o processo pode ser resumido da seguinte forma:

1. **Identificar o Objeto e seus Atributos**: Determine o que será medido (exemplo: uma história de usuário) e seus atributos (exemplo: tamanho da tarefa e tempo de desenvolvimento).
    
2. **Definir o Método de Medição**: Estabeleça como medir os atributos, como calcular o tempo e o tamanho da tarefa.
    
3. **Usar uma Função de Medição**: Combine as medições para calcular a produtividade, como a razão entre os pontos da história de usuário e o tempo de desenvolvimento.
    
4. **Procedimento de Medição**: Realize a medição e crie um indicador para comparar a produtividade com a média do mercado (exemplo: abaixo, na média ou acima).

---
### Modelo de Informação de Medição

- **Objetivo**: Estabelecer uma base para medir e avaliar a produtividade (ou qualquer outro atributo) no desenvolvimento de software.
- **Etapas do Modelo**:
    1. **Entidade**: O que será medido (ex.: tarefa).
    2. **Atributo**: Características que precisam ser medidas (ex.: tamanho da tarefa, tempo de desenvolvimento).
    3. **Método de Medição**: Como obter os dados (ex.: pontos de história de usuário, tempo decorrido).
    4. **Medidas Básicas**: Dados brutos coletados (ex.: pontos de história x tempo).
    5. **Função de Medição**: Como combinar as medidas básicas (ex.: razão entre pontos e tempo).
    6. **Medidas Derivadas**: Cálculos realizados a partir das medidas básicas.
    7. **Modelo de Análise**: Como as medidas serão analisadas (ex.: comparar com a média de produtividade do mercado).
    8. **Indicador**: Resultado final da medição (ex.: produtividade acima, abaixo ou na média do mercado).
    9. **Interpretação**: Explicação do que o indicador significa.

---
### Exemplo Prático (Produtividade da Equipe):

- **Entidade**: Tarefa realizada.
- **Atributos**: Tamanho da tarefa e tempo de desenvolvimento.
- **Método de Medição**: Usar história de usuário com pontos de história e medir o tempo de execução.
- **Função de Medição**: Calcular a razão entre pontos de história e tempo.
- **Modelo de Análise**: Comparar produtividade da equipe com a média do mercado.
- **Indicador**: Se a produtividade está acima, na média ou abaixo do mercado.

---
### Norma ISO/IEC 14598:

- **Objetivo**: Avaliar a qualidade do produto de software.
- **Etapas**:
    1. **Análise de Requisitos da Avaliação**: Definir os objetivos da avaliação.
    2. **Especificação da Avaliação**: Detalhar o que será avaliado.
    3. **Projeto da Avaliação**: Planejar a execução da avaliação.
    4. **Execução da Avaliação**: Realizar os testes e medições.
    5. **Conclusão da Avaliação**: Concluir e gerar relatórios.

---
### Requisitos Funcionais e Não Funcionais:

- **Requisitos Funcionais**: Definem funcionalidades que o sistema deve ter.
    - **Qualidade**: Devem ser claros, completos, não ambíguos e bem definidos.
    - **Exemplo de qualidade**:
        - Unidade: Requisito único (ex.: "Incluir cliente" deve ser específico, como "Incluir cliente pessoa física").
        - Completude: Requisito completo e sem lacunas.
        - Não ambiguidade: Requisito sem interpretações diferentes (ex.: "Emitir relatório de saldo da conta corrente do cliente").
- **Requisitos Não Funcionais (RNFs)**: Relacionados a desempenho e outras qualidades do sistema.
    - **Exemplo de RNF**: Tempo máximo para processar a solicitação de liberação de carga (ex.: 20 minutos).
    - **Cenário Negativo**: Ignorar os RNFs pode levar a falhas no sistema. Exemplo: Se o RNF de tempo de processamento for ignorado, o sistema pode demorar demais, tornando-o inviável.


# FlashCards
---
#eng_req/unidade4

### Flashcard 1
2
**Pergunta:** O que é o objetivo principal da coleta de requisitos no processo de desenvolvimento de software?  
??  
**Resposta:** Definir e documentar as características dos produtos e serviços que satisfaçam as necessidades e expectativas dos usuários do sistema.

---
### Flashcard 2

**Pergunta:** Quais são as duas etapas principais na especificação de Requisitos Funcionais utilizando casos de uso?  
??  
**Resposta:** 
1. Construção do diagrama de casos de uso.  
2. Especificação dos requisitos que acompanham o diagrama de caso de uso.

---
### Flashcard 3

**Pergunta:** O que é representado no diagrama de caso de uso?  
??  
**Resposta:** As funcionalidades e os serviços oferecidos pelo sistema, com os usuários sendo representados por atores e as funcionalidades por elipses.

---
### Flashcard 4

**Pergunta:** Como são descritos os casos de uso no diagrama?  
??  
**Resposta:** O texto interno de cada elipse deve seguir o formato "Nome = verbo + substantivo", indicando a ação realizada, como "Abrir Conta" ou "Comprar Produtos".

---
### Flashcard 5

**Pergunta:** Qual é o objetivo do diagrama de casos de uso?  
??  
**Resposta:** Modelar as funcionalidades do sistema de maneira gráfica e facilitar a compreensão dos requisitos, sendo uma ferramenta útil na elicitação de requisitos.

---
### Flashcard 6

**Pergunta:** O que é especificado na etapa de especificação de casos de uso?  
??  
**Resposta:** Detalhamento dos cenários de execução, com informações adicionais que complementam o diagrama de casos de uso, ajudando na validação e implementação.

---
### Flashcard 7

**Pergunta:** Qual a diferença entre o diagrama de casos de uso e a especificação de casos de uso?  
??  
**Resposta:** O diagrama de casos de uso fornece uma visão geral e gráfica das funcionalidades, enquanto a especificação detalha os cenários de execução, descrevendo os fluxos e condições do caso de uso.

---
### Flashcard 8

**Pergunta:** O que é um fluxo principal em um caso de uso?  
??  
**Resposta:** O fluxo principal é o cenário mais comum do caso de uso, o "caminho feliz", onde tudo ocorre conforme esperado, sem exceções ou alternativas.

---
### Flashcard 9

**Pergunta:** O que são fluxos alternativos e fluxos de exceção em um caso de uso?  
??  
**Resposta:** Fluxos alternativos são cenários alternativos ao fluxo principal, enquanto fluxos de exceção lidam com situações inesperadas que podem ocorrer durante a execução do caso de uso.

---
### Flashcard 10

**Pergunta:** Como as operações CRUD (Create, Retrieve, Update, Delete) devem ser tratadas em um diagrama de casos de uso?  
??  
**Resposta:** Não existe uma forma padrão. Algumas abordagens agrupam as operações CRUD em um caso de uso genérico, como "Manter" ou "Gerenciar", para simplificar o diagrama e a especificação.

---
### Flashcard 11

**Pergunta:** O que são histórias de usuário e como são usadas na especificação de Requisitos Funcionais?  
??  
**Resposta:** Histórias de usuário são descrições feitas pelos clientes sobre as funcionalidades que gostariam que o sistema realizasse. Elas ajudam a especificar Requisitos Funcionais, com foco nas necessidades do usuário, e são usadas nas metodologias ágeis para criar valor para o cliente. Uma história de usuário é composta por três elementos principais: o **quem** (tipo de usuário), o **o que** (descrição da funcionalidade) e o **porquê** (resultado ou valor agregado). A equipe de desenvolvimento utiliza essas histórias para criar um backlog de itens para a sprint, priorizando e detalhando as funcionalidades.  

---
### Flashcard 12

**Pergunta:** Quais são os 3 Cs das histórias de usuário?  
??  
**Resposta:** Os 3 Cs das histórias de usuário são:  
1. **Cartão (Card)**: Formato padrão em que a história de usuário é escrita, contendo o "quem", "o que" e "porquê".  
2. **Conversa (Conversation)**: A comunicação entre a equipe de desenvolvimento e o cliente para entender melhor os requisitos e garantir que sejam compreendidos.  
3. **Confirmação (Confirmation)**: Critérios de aceitação que ajudam a validar se a história foi implementada corretamente.  

---
### Flashcard 13

**Pergunta:** Quais são os elementos principais de uma história de usuário no formato do cartão?  
??  
**Resposta:** Os elementos principais de uma história de usuário são:  
1. **Quem**: O tipo de usuário que se beneficiará com a funcionalidade.  
2. **O que**: A descrição da funcionalidade ou requisito funcional do sistema.  
3. **Porque**: O resultado ou valor agregado que será entregue ao cliente com a implementação da funcionalidade.  

---
### Flashcard 14

**Pergunta:** Como são definidos os critérios de aceitação de uma história de usuário?  
??  
**Resposta:** Os critérios de aceitação de uma história de usuário são definidos como condições específicas que devem ser atendidas para que a história seja considerada concluída e funcional. Esses critérios podem incluir, por exemplo, as ações esperadas do sistema ou comportamentos específicos em diferentes situações. No exemplo de um sistema de check-in, os critérios de aceitação podem incluir: apresentar assentos para seleção, permitir a compra de bagagem extra e destacar assentos especiais.  

---
### Flashcard 15

**Pergunta:** Como construir boas histórias de usuário?  
??  
**Resposta:** Para construir boas histórias de usuário, é importante:  
1. **Delimitar o problema**: Definir para quem o software está sendo desenvolvido e por que.  
2. **Mapear a visão geral**: Entender as dores e alegrias do usuário.  
3. **Explorar**: Analisar como outras pessoas fazem a mesma coisa.  
4. **Gerar uma estratégia de entrega**: Priorizar o que agrega mais valor.  
5. **Gerar uma estratégia de aprendizagem**: Construir e testar um produto mínimo viável.  
6. **Gerar uma estratégia de desenvolvimento**: Dividir o desenvolvimento em etapas, começando pelo que oferece mais riscos.  

---
### Flashcard 16

**Pergunta:** Quais as principais diferenças entre histórias de usuário e outras abordagens para a coleta de requisitos?  
??  
**Resposta:** As principais diferenças são:  
1. Histórias de usuário não detalham especificações de requisitos, mas sim intenções negociáveis.  
2. São curtas, compreensíveis e de fácil leitura por stakeholders, desenvolvedores e usuários.  
3. Representam pequenos incrementos de funcionalidade de valor.  
4. São fáceis de estimar e não requerem manutenção contínua.  
5. São desenvolvidas conforme necessário, no modelo "just-in-time", e podem ser descartadas após implementadas.  

---
### Flashcard 17

**Pergunta:** Qual é a primeira atividade ao iniciar o levantamento de requisitos para o desenvolvimento de um sistema?  
??  
**Resposta:** A primeira atividade é compreender o contexto do problema a ser resolvido pelo sistema. Isso envolve identificar as fontes de informações, como gestores e principais usuários, e coletar informações relevantes para o projeto. Também é importante pesquisar sobre o negócio, as terminologias, regras e regulamentações do setor em que o sistema será aplicado, para garantir um entendimento completo.

---
### Flashcard 18

**Pergunta:** Quais são alguns itens importantes a serem pesquisados ao começar um levantamento de requisitos para um novo sistema?  
??  
**Resposta:** Alguns itens importantes a serem pesquisados incluem:
1. Informações sobre o negócio ao qual o sistema se refere (por exemplo, o funcionamento de Detrans).
2. Dados sobre sistemas similares disponíveis.
3. Leis e regulamentações do setor (como regras de trânsito e requisitos para habilitação).
4. Inovações no setor que possam impactar o sistema.

---
### Flashcard 19

**Pergunta:** O que é essencial para um analista de requisitos ao realizar a primeira reunião com o cliente?  
??  
**Resposta:** É essencial que o analista de requisitos chegue bem preparado para a reunião, demonstrando conhecimento sobre o setor, o contexto do problema e as necessidades do cliente. Isso cria uma boa impressão e transmite confiança, o que é fundamental para superar possíveis resistências e iniciar um diálogo produtivo.

---
### Flashcard 20

**Pergunta:** Quais são as atividades envolvidas no processo de elicitação de requisitos?  
??  
**Resposta:** O processo de elicitação de requisitos envolve as seguintes atividades:
1. **Compreensão do contexto**
2. **Identificação das fontes de informação**
3. **Seleção das técnicas de elicitação** (como entrevistas, reuniões, observações, etc.)
4. **Preparação da elicitação de requisitos**
5. **Realização da elicitação de requisitos**
6. **Organização dos requisitos**

---
### Flashcard 21

**Pergunta:** Quais fatores devem ser considerados ao selecionar as técnicas de elicitação de requisitos?  
??  
**Resposta:** Ao selecionar as técnicas de elicitação de requisitos, deve-se considerar:
1. A disponibilidade das fontes de informação.
2. O tempo disponível para realizar a coleta.
3. O contexto do projeto em desenvolvimento.
4. O tipo de informação que precisa ser coletada.

---
### Flashcard 22

**Pergunta:** Quais são os artefatos que podem ser produzidos após o levantamento de requisitos em um projeto de desenvolvimento de sistema?  
??  
**Resposta:** Os artefatos que podem ser produzidos incluem:
1. Uma declaração de necessidade e viabilidade do sistema.
2. Uma lista de clientes, usuários e outros stakeholders que participaram do levantamento.
3. Uma descrição do ambiente técnico do sistema.
4. Uma lista de requisitos organizados por função, junto com as restrições de domínio.
5. Cenários de uso que ilustram como o sistema será utilizado em diferentes condições operacionais.

---
### Flashcard 23

**Pergunta:** Como deve ser a organização dos requisitos após o levantamento?  
??  
**Resposta:** Após o levantamento de requisitos, é fundamental que os requisitos sejam organizados de maneira estruturada, geralmente por função. Isso pode incluir uma lista de requisitos, suas respectivas restrições de domínio e cenários de uso. Esses artefatos são então revisados por todas as partes envolvidas no levantamento de requisitos para garantir que as informações estejam claras e precisas.

---
### Flashcard 24

**Pergunta:** Como podemos avaliar os requisitos de software após a coleta de requisitos?  
??  
**Resposta:** A avaliação dos requisitos de software pode ser feita comparando o que foi coletado com o que foi planejado. Isso envolve a medição e análise de atributos como tempo, produtividade e gravidade dos riscos. Para isso, é necessário ter um padrão para comparar, possibilitando o controle do processo e o planejamento adequado. A avaliação ajuda a garantir que o software atenda às necessidades do usuário conforme esperado.

---
### Flashcard 25

**Pergunta:** Quais são os termos essenciais para a medição no contexto de requisitos de software?  
??  
**Resposta:** Alguns termos essenciais para a medição incluem:
1. **Função de medição:** Algoritmo ou cálculo utilizado para combinar várias medidas.
2. **Medição:** A função de medição realizada para obter dados.
3. **Medida:** Valor atribuído a uma variável após a medição.
4. **Procedimento de medição:** Conjunto de operações realizadas para realizar uma medição específica.
5. **Valor:** Resultado numérico ou categórico atribuído à medida.

---
### Flashcard 26

**Pergunta:** Como usar os termos de medição para avaliar a produtividade de uma equipe de desenvolvimento?  
??  
**Resposta:** Para avaliar a produtividade de uma equipe, é necessário:
1. **Identificar o objeto a ser medido** (exemplo: tarefa ou funcionalidade).
2. **Definir o método de medição**, como pontos de história do usuário (story points) para medir o tamanho da tarefa e o tempo para desenvolvimento.
3. **Utilizar uma função de medição** para combinar as medidas básicas (por exemplo, razão entre pontos de história e tempo de desenvolvimento).
4. **Analisar as medidas obtidas** e compará-las com um indicador de produtividade do mercado para interpretar se a produtividade está abaixo, na média ou acima da média.

---
### Flashcard 27

**Pergunta:** O que é o modelo de informação de medição e como ele pode ser utilizado na avaliação de produtividade?  
??  
**Resposta:** O **modelo de informação de medição** ajuda a estruturar o processo de avaliação, com as seguintes etapas:
1. **Entidade:** Define o que será medido (exemplo: tarefa ou funcionalidade).
2. **Atributo:** Características que devem ser medidas (exemplo: tamanho da tarefa, tempo de desenvolvimento).
3. **Método de medição:** Técnica utilizada para obter as medidas.
4. **Medidas básicas e derivadas:** Dados coletados e combinados para formar a base de análise.
5. **Função de medição:** Como combinar as medidas para gerar uma análise.
6. **Indicadores e interpretação:** Avaliar os resultados em comparação com os padrões do mercado para tomar decisões informadas.

---
### Flashcard 28

**Pergunta:** Como a norma NBR ISO/IEC 14598-1 pode ajudar na avaliação de produto de software?  
??  
**Resposta:** A norma **NBR ISO/IEC 14598-1** fornece requisitos e recomendações para a implementação prática da avaliação de produtos de software. Ela ajuda fornecedores, compradores, laboratórios e outras partes envolvidas a realizar uma avaliação estruturada e padronizada, abordando requisitos de qualidade, desempenho e outros aspectos essenciais do produto. A norma também sugere um processo de avaliação com etapas claras, como análise de requisitos, especificação e execução da avaliação.

---
### Flashcard 29

**Pergunta:** Quais são os atributos que um **Requisito Funcional de qualidade** deve ter?  
??  
**Resposta:** Um **Requisito Funcional** de qualidade deve atender aos seguintes atributos:
1. **Unidade:** Deve propor uma única coisa e não várias responsabilidades.
2. **Completude:** O requisito deve ser autocontido, com um início, meio e fim claros.
3. **Não ambiguidade:** O requisito não pode ser vago ou impreciso.
4. **Tempo verbal:** O requisito deve ser descrito com um tempo verbal que indique uma ação a ser realizada pelo sistema (por exemplo, “realizar compra”).

---
### Flashcard 30

**Pergunta:** Qual é um exemplo de **cenário negativo** relacionado a requisitos não funcionais em um sistema de software?  
??  
**Resposta:** Um **cenário negativo** pode ocorrer quando um **Requisito Não Funcional** (RNF) não é tratado adequadamente durante o desenvolvimento. Exemplo: em um sistema de logística de uma transportadora, o RNF exigia que a **solicitação de liberação de carga** fosse processada em no máximo **20 minutos**. No entanto, devido ao atraso no levantamento de requisitos, a equipe não deu a devida importância ao RNF01, e o sistema demorou **50 minutos** para processar, o que causou **reprovação no teste de aceitação** e inviabilizou a produção. A causa foi o **não atendimento ao requisito de desempenho**.

---
### Flashcard 31

**Pergunta:** Qual a consequência de não atender um **Requisito Não Funcional** crítico em um projeto de software?  
??  
**Resposta:** A consequência de não atender um **Requisito Não Funcional** crítico, como um requisito de desempenho, pode ser grave. No exemplo da transportadora, a demora excessiva no processamento da solicitação de liberação de carga resultou em **falha nos testes de aceitação** e **impossibilidade de produção** do sistema. Isso exigiu **reestruturação do sistema**, atraso no projeto e custos adicionais, tornando o produto inviável para operação.

