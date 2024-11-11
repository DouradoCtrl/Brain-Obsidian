# Unidade 03
#leitura1
- fontes de informação (pag 109)
- coleta de requisitos x levantamento/elicitação de requisitos
- técnicas e ferramentas (entrada e saída) 
	- entrevista
	- brainstorming
	- questionário
	- Oficinas
		- intermediadors
		- jad (sono)
		- user stories (sono)
			- INVEST
- Quando usar a técnica
- Qual técnica Usar

#leitura2
**Fontes de informação:** Onde você pega as informações para construir seus requisitos (normalmente stakeholders) ou até mesmo documentação de processos.

**Classificação de fonte de informação:**

| **Tipo de Informação**   | **Descrição**                                                                                                                                                 | **Exemplos**                                                                          |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **Stakeholders**         | Influenciam direta ou indiretamente os requisitos do sistema, como usuários, operadores, desenvolvedores, arquitetos, clientes e testadores.                  | Usuários, Operadores, Desenvolvedores, Arquitetos, Clientes, Testadores.              |
| **Documentos**           | Recursos que contêm informações importantes que podem se tornar requisitos, como documentos legais, normativos, padrões ou específicos do negócio ou empresa. | Documentos legais, normas e padrões, documentos específicos do domínio ou da empresa. |
| **Sistemas em Operação** | Sistemas legados, predecessores ou concorrentes que podem fornecer informações sobre novas funcionalidades desejadas pelos clientes.                          | Sistemas legados, sistemas concorrentes, predecessores do sistema atual.              |

**Escopo do cliente:** Produto e serviço gerado entregue ao cliente
**Escopo do projeto:** Depende da estratégia de condução do projeto

**Levantamento de requisitos x Diferenças de requisitos**
...

![[Pasted image 20241107175115.png]]

### Técnica de Entrevista

- **Objetivo**: Coletar informações diretamente dos stakeholders para ajudar na definição de requisitos do sistema.
  
- **Características**:
  - Conversa entre duas pessoas com um objetivo definido.
  - Foco na interação pessoal e no compartilhamento de conhecimento que pode estar na memória dos envolvidos.
  - Permite obter informações sobre qualificações, processos, atribuições e opiniões dos stakeholders.

- **Procedimentos para realizar uma boa entrevista**:
  1. **Identificar os stakeholders** que serão entrevistados.
  2. **Criar um clima amigável**, mas profissional – lembre-se de que o entrevistado não é seu amigo.
  3. **Evitar induzir respostas**: Não influencie as respostas, como sugerir soluções (ex.: "Não seria melhor multiplicar A por B?").
  4. **Preparar uma lista de questões** a serem abordadas durante a entrevista.
  5. **Registrar anotações** detalhadas durante a entrevista, pois podem ser úteis posteriormente.
  6. **Conforto do entrevistado**: Deixe o usuário à vontade, já que muitas pessoas podem não gostar de ser entrevistadas.

Esse método é especialmente útil nas fases iniciais do levantamento de requisitos e proporciona insights valiosos diretamente dos envolvidos no processo.

![[Pasted image 20241107175629.png]]
### Técnica de Brainstorming

- **Objetivo**: Gerar uma grande quantidade de ideias criativas para resolver problemas específicos, sem julgamentos ou análises durante o processo.
  
- **Características**:
  - Sessão grupal focada na quantidade de ideias, não na qualidade imediata.
  - Ambiente descontraído e informal, onde todos os participantes podem contribuir.
  - A fase final pode incluir a análise ou votação das melhores ideias.

- **Fases do Brainstorming**:
  1. **Aquecimento**: Escolha da dinâmica para preparar o grupo.
  2. **Ideação**: Geração de ideias pelos participantes.
  3. **Encerramento**: Agrupamento das ideias geradas. Pode incluir uma votação ou análise das melhores ideias.

- **Regras Importantes**:
  - **Quantidade é a prioridade**: Muitas ideias, sem se preocupar com a qualidade inicial.
  - **Proibição de julgamentos**: Não criticar ou avaliar as ideias durante a sessão.
  - **Ambiente descontraído**: Foco no enriquecimento das ideias e não em discussões.
  - **Papel do condutor e do escriba**: O condutor guia a sessão, e o escriba anota as ideias (em quadro branco, notas adesivas, etc.).

- **Métodos para uma sessão eficiente**:
  1. **Divulgação clara dos objetivos**: Certifique-se de que todos entendem o propósito da sessão.
  2. **Duração da ideação**: Entre 20 a 60 minutos.
  3. **Intervalo para relaxamento**: Pode ajudar a melhorar a criatividade.
  4. **Estudo detalhado das ideias**: Após a geração de ideias, é importante detalhar e analisar as sugestões.

O brainstorming é uma ferramenta eficaz para fomentar a criatividade, engajar os participantes e gerar soluções inovadoras de maneira colaborativa.

![[Pasted image 20241107175838.png]]

Aqui está um resumo em tópicos sobre a técnica de **questionário**:

### Técnica de Questionário

- **Objetivo**: Coletar informações dos stakeholders de forma estruturada, especialmente útil quando há muitos participantes ou quando os envolvidos estão em locais distantes.

- **Características**:
  - Conjunto de questões objetivas ou abertas que os participantes devem responder.
  - Pode ser usado para coletar dados de um grande número de pessoas de forma eficiente.
  - Utilizado quando há necessidade de coletar informações amplas e estatísticas.

- **Tipos de Questionários**:
  - **Múltipla escolha**
  - **Lista de verificação**
  - **Questões com espaços em branco**
  
- **Vantagens**:
  - **Custos reduzidos**.
  - **Alcança muitas pessoas**.
  - **Liberdade para os participantes** responderem no seu próprio ritmo.
  
- **Dificuldades**:
  - **Equívocos no significado das perguntas** por parte dos entrevistados.
  - **Muitas opiniões distintas**, o que pode dificultar a análise.
  
- **Aplicação**:
  - **Quando a distância é considerável** entre os participantes.
  - **Quando se quer um primeiro conhecimento** sobre o problema ou as necessidades dos stakeholders.

- **Procedimentos para Aplicar um Questionário**:
  1. **Determinar os objetivos da pesquisa**: Entender as necessidades ou problemas do sistema e identificar os requisitos prioritários.
  2. **Identificar o público-alvo**: Definir quem são os usuários ou stakeholders que responderão ao questionário.
  3. **Elaborar e revisar as questões**: As perguntas devem ser claras, objetivas e evitar ambiguidades. A elaboração é a etapa mais crítica.
  4. **Estimar o tempo de preenchimento**: Considerar o perfil dos participantes e o tempo necessário para completar o questionário.
  5. **Realizar teste-piloto**: Validar o questionário com um grupo pequeno para identificar falhas ou problemas nas perguntas.
  6. **Distribuir o questionário**: Escolher a estratégia de distribuição (online, impresso, presencial, etc.).
  7. **Analisar os resultados**: Interpretar as respostas coletadas e usá-las para definir requisitos do sistema.

- **Boas Práticas**:
  - **Introdução clara**: Explique os objetivos e o propósito do questionário.
  - **Linguagem simples e objetiva**: Evite termos técnicos e complexos.
  - **Questões objetivas**: De preferência, utilize perguntas fechadas para facilitar a tabulação e análise.
  - **Evitar perguntas ambíguas**: Certifique-se de que as perguntas não possam ser interpretadas de diferentes formas.
  - **Tamanho adequado**: Mantenha o questionário curto para não desmotivar os participantes.
  
Exemplo de perguntas em um **questionário de levantamento de requisitos para um sistema de controle de vendas e compras**:
- Como é feito o controle do caixa?
- Como é realizado o controle de estoque?
- Como são realizados os pedidos de venda?
- Como é feito o pedido dos produtos que faltam no estoque?
  
Essa técnica é muito útil para obter dados de forma estruturada e eficaz, especialmente quando a amostra de participantes é grande ou distribuída geograficamente.

![[Pasted image 20241107180112.png]]

Aqui está um resumo em tópicos sobre a técnica de **Oficinas de Requisitos (JAD e Histórias de Usuário)**:

### Técnicas de Oficina para Levantamento de Requisitos

#### 1. **JAD (Joint Application Design)**

- **Objetivo**: Coletar informações de alta qualidade dos stakeholders em um curto período por meio de reuniões estruturadas, com foco em decisões por consenso.
  
- **Princípios do JAD**:
  - **Dinâmica de grupo**: Facilita a troca de ideias e a criatividade.
  - **Recursos visuais**: Uso de painéis, protótipos e transparências para melhor visualização e comunicação.
  - **Processo organizado e racional**: Análise top-down e atividades bem definidas para atingir objetivos claros.
  - **Documentação padrão**: Registro formal dos resultados da sessão para garantir entendimento e alinhamento entre todos.

- **Benefícios do JAD**:
  - Aumento da **produtividade** e **qualidade**.
  - **Trabalho em equipe** e redução de custos de desenvolvimento e manutenção.

- **Visão Geral do Processo JAD**:
  1. **Preparação**: Coleta de dados e definição dos objetivos.
  2. **Sessão**: Realização da oficina para geração de soluções.
  3. **Revisão**: Avaliação dos resultados e ajustes necessários.

#### 2. **Histórias de Usuário (User Stories)**

- **Objetivo**: Descrição simples e curta das funcionalidades que os usuários desejam que o sistema execute. Usada principalmente em metodologias ágeis.

- **Formato das Histórias de Usuário**:
  - **Quem?** (papel do usuário): Identifica quem se beneficiará da funcionalidade.
  - **O quê?** (atividade): O que o sistema deve fazer.
  - **Por quê?** (valor de negócio): O valor ou benefício que a funcionalidade traz ao usuário.

  **Modelo de Histórias de Usuário**:
  - Exemplo: *Como vendedor, quero procurar por livros filtrando por nome para verificar se o livro X está disponível para pronta entrega.*

- **Benefícios das Histórias de Usuário**:
  - Promovem **entendimento comum** entre equipe de desenvolvimento e cliente.
  - **Flexibilidade** para adaptação conforme mudanças nas necessidades do cliente.
  - **Foco no valor** entregue ao cliente e em entregas incrementais.

- **Técnica INVEST** (Boas práticas para Histórias de Usuário):
  - **I**: **Independente** – A história deve ser autônoma e livre de dependências.
  - **N**: **Negociável** – Deve ser possível negociar mudanças na história.
  - **V**: **Valiosa** – A história deve agregar valor ao cliente.
  - **E**: **Estimável** – A história deve ser passível de estimativas de esforço.
  - **S**: **Small** – A história deve ser pequena o suficiente para ser concluída em uma única iteração.
  - **T**: **Testável** – Deve ser possível testar a história para validar se foi implementada corretamente.

- **Exemplos de Histórias de Usuário**:
  - *Consultar cliente pelo CNPJ*: "Como vendedor, quero consultar meus clientes pelo CNPJ para negociar com informações mais precisas."
  - *Alterar horários*: "Como usuário não administrativo, quero modificar meus horários para não precisar abrir chamados toda vez que minhas tarefas mudarem."

### Conclusão:
- As **oficinas** de levantamento de requisitos, como o **JAD** e as **Histórias de Usuário**, são técnicas eficientes para garantir que os requisitos sejam bem compreendidos e alinhados com as necessidades reais dos usuários.
- **JAD** é ideal para obter consenso rápido e eficaz em grupo, enquanto **Histórias de Usuário** são perfeitas para metodologias ágeis e focam nas necessidades dos usuários de forma simples e direta.

# FlashCards
#eng_req/unidade3

**Pergunta:** O que é uma entrevista como técnica de levantamento de requisitos?
??
**Resposta:** A entrevista é uma técnica simples e tradicional, baseada em uma conversa entre duas pessoas, com o objetivo de coletar informações e requisitos de stakeholders. Ela facilita o contato pessoal e a obtenção de informações que podem estar apenas na memória dos envolvidos.

---

**Pergunta:** Quais são os cuidados ao realizar uma entrevista para levantamento de requisitos?
??
**Resposta:**
1. Identificar os stakeholders corretos.
2. Evitar induzir as respostas.
3. Preparar uma lista de questões.
4. Anotar todas as informações possíveis.
5. Criar um ambiente confortável para o entrevistado.

---

**Pergunta:** Quais são as vantagens do brainstorming?
??
**Resposta:**
1. Estimula o pensamento criativo.
2. Os participantes se sentem valorizados.
3. Permite a modificação ou combinação de ideias.
4. Incentiva a participação ativa de todos.

---

**Pergunta:** Quais dificuldades podem surgir durante uma sessão de brainstorming?
??
**Resposta:**
1. Alguns participantes podem se sentir tímidos.
2. Pode ser difícil garantir a igualdade de oportunidades para todos.
3. Alguns participantes podem não se sentir à vontade para expor suas ideias.

---

**Pergunta:** Quando é recomendada a aplicação de um questionário no levantamento de requisitos?
??
**Resposta:** Quando se deseja coletar informações de um grande número de pessoas, especialmente quando essas estão distantes fisicamente ou quando é necessário realizar uma análise quantitativa.

---

**Pergunta:** Quais são as vantagens de utilizar um questionário para levantamento de requisitos?
??
**Resposta:**
1. Atinge um grande número de pessoas.
2. Tem custos reduzidos.
3. Dá liberdade aos participantes para responderem no seu próprio tempo.

---

**Pergunta:** Quais dificuldades podem ser enfrentadas ao aplicar um questionário?
??
**Resposta:**
1. O significado das perguntas pode ser mal interpretado pelos respondentes.
2. Diversidade de opiniões pode dificultar a análise das respostas.

---

**Pergunta:** O que caracteriza uma história de usuário (user story) na metodologia ágil?
??
**Resposta:** Uma história de usuário descreve o que o usuário deseja que o sistema faça, de forma curta e simples, com foco nas necessidades e no valor de negócio da funcionalidade. A história segue o formato: Quem ?[tipo de usuário], O quê [ação específica] Por que ? [resultado ou valor]_.

---

**Pergunta:** Quais são os princípios do método JAD (Joint Application Design)?  
??
**Resposta:**
1. Dinâmica de grupo.
2. Uso de recursos visuais.
3. Processo organizado e racional.
4. Documentação padrão.

---

**Pergunta:** Quais são os benefícios do método JAD?
??
**Resposta:**
1. Maior produtividade.
2. Mais qualidade.
3. Trabalho em equipe.
4. Custos mais baixos de desenvolvimento e manutenção.

---

**Pergunta:** Quais são os critérios do acrônimo INVEST para boas histórias de usuário?
??
**Resposta:**
- **I**: Independente
- **N**: Negociável
- **V**: Valiosa
- **E**: Estimável
- **S**: Pequena
- **T**: Testável

---

**Flashcard 12:** **Pergunta:** O que é um "teste-piloto" em um questionário de levantamento de requisitos?
??
**Resposta:** O teste-piloto é uma fase em que o questionário é testado com um pequeno grupo para identificar falhas ou problemas antes de sua distribuição ampla. Isso garante que as questões estejam claras e as respostas sejam relevantes.

**RESPOSTA LIVRO**
a
d
c