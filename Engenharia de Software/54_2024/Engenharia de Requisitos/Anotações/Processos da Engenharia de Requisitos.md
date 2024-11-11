# Aula 02

# Unidade 02
### **Processo:**
1. ação continuada, realização contínua e prolongada de alguma atividade; seguimento, curso, decurso.
2. sequência contínua de fatos ou operações que apresentam certa unidade ou que se reproduzem com certa regularidade; andamento, desenvolvimento, marcha.

**Um processo usado nessa engenharia pode variar bastante.**

![[Pasted image 20241104211753.png]]
Pressman e Maxim (2021)

**Especificação de requisitos:** Todas as atividades realizadas para identificar, analisar, especificar e definir as necessidades do sistema.

**Gestão de requisitos**: Atividades responsáveis pela documentação, versionamento, controle de mudanças e qualidade dos requisitos levantados.

---
Sommerville (2018)
### **Três atividades principais:**

- **Elicitação e análise:** Descoberta de requisitos por meio de stakeholders.
- **Especificação:** Conversão dos requisitos em forma padrão 
- **Validação:** Averiguam-se os requisitos definem o sistema desejado pelo cliente.
![[Pasted image 20241104213553.png]]
A Engenharia de Requisitos é um processo iterativo que organiza atividades em espiral, resultando em um documento de requisitos do sistema (Sommerville, 2018).

**Validação x Verificação**
> Fazer uma breve diferenciação... (vídeo)

### **Levantamento e Análise de Requisitos de Software**

Compreender as necessidades do cliente e proposta de solução. Uma das missões mais desafiadoras pois é preciso compreender os requisitos dos stakeholders. Durante essa etapa há a interação com o usário para identificar o domínio, regras de negócio e serviços desejados. (Contato com o cliente). Também conhecida com o **elicitação e análise de requisitos**

**Por que o levantamento de requisitos é considerado um processo difícil ?**
- Usuários muitas vezes não sabem exatamente o que querem, fazendo exigências irreais.
- Expressam requisitos em seus próprios termos, o que pode confundir engenheiros sem experiência no domínio.
- Diferentes usuários podem expressar requisitos de maneiras variadas.
- Fatores políticos e tributários influenciam os requisitos do sistema.
- O ambiente econômico é dinâmico, resultando em mudanças durante a análise.
- Novos requisitos podem surgir devido a mudanças e novos usuários que não foram consultados originalmente.

Levantamento de análise de requisitos(modelo de processo)
![[Pasted image 20241104214713.png]]
A compreensão do engenheiro de software sobre os requisitos melhora a cada iteração do processo, resultando na produção do documento final.

1. **Descoberta e compreensão dos requisitos:** Interação com os stakeholders para identificar e documentar os requisitos de domínio, assegurando que o engenheiro compreenda o contexto da aplicação para uma transcrição clara.

2. **Classificação e organização dos requisitos:** Os requisitos são agrupados de forma coerente, facilitando sua gestão e análise.

3. **Priorização e negociação dos requisitos:** Os requisitos mais importantes são priorizados, e ocorrem negociações para resolver conflitos entre eles.

4. **Documentação dos requisitos:** Os requisitos identificados são documentados, servindo como base para as próximas etapas do processo de desenvolvimento.

### Verificação e Validação de Requisitos de Software

**Validação**: Valida se os requisitos no levantamento está de acordo com o que o cliente precisa. (O sistema atende o que é proposto ?)

**Verificação:** Avaliar se o que foi planejado, realmente, foi realizado, se os requisitos e funcionalidades documentados foram implementa- dos.

Etapa de extrema importância, pois um erro de requisito identificado após a implementação do sistema exige a revisão de todos os artefatos, gerando custos significativos.

**Tipos de verificação**
- **Verificações de validade:** Identificar se certas funções citada como necessárias são indispensáveis. (afinal o cliente é burro)

- **Verificações de consistência:** Os requisitos não podem estar em conflitos, redundância ou contradição. (requisitos harmoniosos)

- **Verificações de completude:** Deve estar completa, começo, meio e fim; deve  incluir todas as funções e restrições pretendidas pelo usuário.

- **Verificações de realismo:** Se os requisitos são realmente possíveis de serem implementados.

- **Verificabilidade:** Deve ser passível de verificação.

Sommerville(2018) - Técnicas de validação
![[Pasted image 20241104222105.png]]
- Cheklist (bonus)
![[Pasted image 20241104222424.png]]

**As características de validação dos requisitos incluem:**
- **Não ambíguo:** Cada requisito deve ter uma única interpretação.
- **Consistente:** Nenhum requisito pode entrar em conflito com outros.
- **Completo:** Deve conter todas as informações necessárias para o desenvolvimento do software.

![[Pasted image 20241104222806.png]]

### Especificação de Requisitos

> Segundo Somerville é o processo de escrever os requisitos de usuário e de sistema em um documento de requisitos

**Devem ser:**
- Claros
- Inequívocos
- Fácil compreensão
- Completos
- Consistentes

**Públicos-alvo do documento de requisitos:**
- **Clientes:** Lê o documentos para saber se está de acordo com o solicitado
- **Gerentes:** Utiliza o documentos para solicitar um anova proposta e planejar o processo de desenvolvimento.
- **Programadores:** Utiliza o documento para entender o que dever ser desenvolvido. 
- **Testes:** Utiliza o documento para planejar os testes de validação
- **Manutenção:** Utiliza o documento para compreender o sistema e suas relações.

**Sommerville (2018)**
- **Necessidade:** "Está função é necessária ?"
- **Verificável:** Verifique se o que está sendo produzido é verificável. "Como posso testar essa função ?"
- **Realizável:** Analise se pode ser desenvolvido. "O requisito é atingível ?"
- **Claro:** Verifique se cada requisito expressa uma única função e se é um bom requisito. "Está claro o que precisa se feito ?" 

> **O documento em si deve descrever os requisitos do sistema e não os detalhes da arquitetura.**

> É recomendável usar uma linguagem natural, tabelas simples e diagrama intuitivos

**Linguagem natural**
- A linguagem natural possui uma ambiguidade intrínseca.
- Muito flexível
- Não possibilita padronização

**Tipos de padronização (Linguagens)**
1. **Linguagem natural estruturada:** Requisitos escrito em padrão ou template
2. **Linguagem de descrição de projeto:** Requisitos escritos em uma linguagem (programação) porém com características mais abstratas
3. **Notações gráficas:** Requisitos definidos com modelos gráficos. (UML, caso de uso, anotações de texto)
4. **Especificações matemáticas:** Requisitos escritos com notações matemáticas, como máquinas de estado finito ou conjuntos, podem reduzir a ambiguidade nas especificações. No entanto, a maioria dos clientes tem dificuldade em entender especificações formais desse tipo.

> **pag74 - Visualize a linguagem natural estruturada documentação template**





# FlashCards
---
#eng_req/unidade2

Segundo as atividades de engenharia de software de Pressman e Maxim. O que é **Especificação de requisitos ?**
??
representa todas as atividades realizadas para identificar, analisar, especificar e definir as necessidades do sistema (levantamento/elicitação e análise, negociação, documentação, validação e verificação)
![[Pasted image 20241104211753.png]]

Segundo as atividades de engenharia de software de Pressman e Maxim. O que é **Gestão de requisitos ?**
??
Atividades responsáveis pela documentação, versionamento, controle de mudanças e qualidade dos requisitos levantados.
![[Pasted image 20241104211753.png]]

**Pergunta:** Qual é o objetivo da Elicitação e análise na Engenharia de Requisitos?
??
**Resposta:** O objetivo da **Elicitação e análise** é descobrir os requisitos por meio da interação com os stakeholders.

**Pergunta:** Qual é o objetivo da Validação na Engenharia de Requisitos?
??
**Resposta:** O objetivo da **Validação** é assegurar que os requisitos realmente definem o sistema desejado pelo cliente.

**Pergunta:** Qual é o objetivo da Validação na Engenharia de Requisitos?
??
**Resposta:** O objetivo da **Validação** é assegurar que os requisitos realmente definem o sistema desejado pelo cliente.

**Pergunta:** Qual é a importância da fase de elicitação e análise de requisitos na Engenharia de Requisitos?
??
**Resposta:** É nessa fase que ocorre o contato direto com o cliente e usuários, permitindo entender suas necessidades e expectativas para o sistema, garantindo que os requisitos sejam bem compreendidos.

**Pergunta:** O que ocorre na atividade de descoberta e compreensão dos requisitos? 
??
**Resposta:** Interação com os stakeholders para identificar e documentar os requisitos de domínio, garantindo uma compreensão clara do contexto da aplicação.

**Pergunta:** Qual é o objetivo da classificação e organização dos requisitos?
??
**Resposta:** Agrupar os requisitos de forma coerente para facilitar sua gestão e análise.

**Pergunta:** O que envolve a priorização e negociação dos requisitos?
??
**Resposta:** Priorizar os requisitos mais importantes e negociar para resolver conflitos entre eles.

**Pergunta:** Qual é a finalidade da documentação dos requisitos?
??
**Resposta:** Documentar os requisitos identificados, servindo como base para as próximas etapas do processo de desenvolvimento.

**Pergunta:** Qual é a diferença entre validação e verificação de requisitos?
??
**Resposta:** A validação assegura que o software atende às expectativas do cliente ("estamos construindo o sistema correto?"), enquanto a verificação garante que o software foi implementado corretamente de acordo com o planejamento ("estamos construindo corretamente o sistema?").

**Pergunta:** O que são verificações de validade?
??
**Resposta:** Identificam se funções consideradas necessárias pelos usuários são, de fato, indispensáveis para o sistema.

**Pergunta:** Qual é o objetivo das verificações de consistência?  
??
**Resposta:** Garantir que os requisitos no documento não entrem em conflito e que não haja restrições contraditórias ou descrições diferentes da mesma função.

**Pergunta:** O que é verificação de completude? 
??
**Resposta:** Assegura que todos os requisitos que definem as funções e restrições do sistema estejam incluídos no documento.

**Pergunta:** O que envolve as verificações de realismo?
??
**Resposta:** Verificar se os requisitos podem ser implementados (possível) e se está dentro do orçamento considerado e o cronograma.

**Pergunta:** O que significa verificabilidade dos requisitos?
??
**Resposta:** Os requisitos devem ser passíveis de verificação por meio de testes que demonstrem que o sistema atende a cada requisito especificado.

**Pergunta:** O que significa um requisito "não ambíguo"? 
??
**Resposta:** Um requisito é "não ambíguo" se é suscetível a apenas uma interpretação.

**Pergunta:** Quando um requisito é considerado "consistente"?
??
**Resposta:** Um requisito é "consistente" se não está em conflito com outros requisitos do mesmo documento.

**Pergunta:** O que define um requisito "completo"?
??
**Resposta:** Um requisito é "completo" se contém toda a informação necessária (e apenas ela) para produzir o software.

**Pergunta:** O que é a especificação de requisitos?
??
**Resposta:** Segundo Sommerville (2018), é o processo de escrever os requisitos de usuário e de sistema em um documento de requisitos.

**Pergunta:** Quais características devem ter os requisitos?
??
**Resposta:** Os requisitos devem ser claros, inequívocos, de fácil compreensão, completos e consistentes.

**Pergunta:** Por que especificar requisitos é uma tarefa desafiadora?
??
**Resposta:** Porque os requisitos podem ser interpretados de formas diferentes pelos stakeholders, gerando conflitos, inconsistências e ambiguidades.

**Pergunta:** O que o documento de requisitos deve considerar ao ser escrito?  
??
**Resposta:** Deve considerar o público-alvo, ou seja, os leitores, para ser compreensível para eles.

**Pergunta:** Quais são os principais públicos-alvo do documento de requisitos e suas funções?
??
**Resposta:**
1. **Clientes**: Validam se o documento atende ao solicitado.
2. **Gerentes**: Usam o documento para solicitar propostas e planejar o desenvolvimento.
3. **Programadores**: Consultam para entender o que deve ser desenvolvido/implementado.
4. **Equipe de Testes**: Utiliza para planejar os testes de validação do sistema.
5. **Manutenção**: Usa o documento para compreender o sistema e suas relações.

**Pergunta:** Qual é o foco do documento de requisitos?
??
**Resposta:** Descrever os requisitos do sistema, não os detalhes da arquitetura ou do projeto.

**Pergunta:** É recomendado evitar jargões de software e notações estruturadas ao escrever requisitos de usuário. (Verdadeiro ou Falso?)
??
**Resposta:** Verdadeiro. Requisitos de usuário devem ser claros e compreensíveis para todos os stakeholders, sem jargões ou notações complexas.

**Pergunta:** Quais parâmetros considerar na validação dos requisitos?
??
**Resposta:**
1. **Necessidade**: Verifique se cada requisito é realmente necessário.
2. **Verificável**: Certifique-se de que cada função pode ser testada.
3. **Realizável (atingível)**: Analise se o requisito pode ser implementado considerando a tecnologia, orçamento e prazos.
4. **Claro**: Releia o documento e verifique se cada requisito expressa uma única função claramente. Pergunte-se: “está claro o que precisa ser feito?”

**Pergunta:** Regras básicas para descrever requisitos (recomendável linguagem natural)
??
**Resposta:**
1. Use formato padrão para todos os requisitos.
2. Seja coerente na linguagem; use verbos para requisitos obrigatórios/desejáveis.
3. Destaque as partes importantes.
4. Evite jargões técnicos; detalhe termos de negócio.

**Pergunta:** Quais são as linguagens padronizadas para a especificação de requisitos? 
??
**Resposta:**
1. **Linguagem Natural Estruturada**: Requisitos escritos em linguagem natural em um formulário padrão, com campos que detalham aspectos do requisito.
2. **Linguagem de Descrição de Projeto**: Requisitos escritos em uma linguagem semelhante à programação, mas mais abstrata, definindo um modelo operacional.
3. **Notações Gráficas**: Requisitos definidos por modelos gráficos, acompanhados de anotações, diagramas de caso de uso e sequência da UML®.
4. **Especificações Matemáticas**: Requisitos escritos com notações matemáticas (ex: máquinas de estado finito), que podem ser difíceis para a maioria dos clientes entender.