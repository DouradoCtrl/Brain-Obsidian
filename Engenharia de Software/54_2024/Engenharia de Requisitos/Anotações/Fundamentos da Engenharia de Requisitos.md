# Aula 1
-  Os requisitos são funcoes e restricoes que sao geradas durante o processo de engenharia de requisitos
- Segundo a professora engenharia de requistos faz parte do processo de software como abordado na atividade engenharia de software
- Segundo a mesma engenharia de requisitos fazer parte da etapa de especificao de um processo de software

- Engenharia de requisito também é um processo

**Tipos de requisitos:**
- Funcional
	- definicao das funcoes
	- entradas e saidas
- Não funcional 
	- dizem respeito as retricoes
	- interfaces com o usuario, desempenho, portabilidade, padroes, confiabilidade etc
- Requisito de domínio

# Unidade 1
>**Engenharia de requisitos:**
>	1. Analisar
>	2. Documentar
>	3. Verificar

**Processo de software:** Entregar um software com qualidade, dentro do prazo e seguindo orcamento estipulado

> Pressman e Maxim - Processo eficaz

**Como identificar o domínio do problema ?  Abaixo algumas perguntas.**
1. Que informação deve ser processada? 
2. Quais função e desempenho são desejados? 
3. Que comportamento deve ser esperado do sistema? 
4. Quais interfaces devem ser estabelecidas?
5. Quais são as restrições de projeto? 
6. Quais critérios de validação serão usados?

**Como identificar o domínio da solução do problema ? Abaixo mais algumas perguntas.**
1. Como os dados devem ser?
2. Como a função deve ser implementada dentro da arquitetura do software? 
3. Como os detalhes dos procedimentais devem ser implementados? 
4. Como as interfaces devem ser caracterizadas? 5. Como o projeto deve ser traduzido em linguagem de programação?


**Processo de Software - Cinco atividades principais**
![[images01.png]]
- **Especificação**: Onde é definida as funcionalidade e restrições do software
- **Projeto e Implementação**: Onde é definida quais funcionalidades sera implementadas para um produto final
- **Validação**: A palavra por si só já fala
- **Evolução**: Fase a qual são atendidas possíveis mudanças de ocorrer durante o ciclo de vida do software

> **Sommervile 2018**


- **Não existe processo ideal de desenvolvimento de software**

> Pressman e Maxin (2021) -  Engenharia de Requisitos

pag 23, revisar

> **Stakeholders:** quaisquer pessoas ou organizações que executam ou sofrem alguma ação relacionada ao projeto a ser desenvolvido.
- Deve se ouvir e interpretá-los

**Tipos de Stakeholders:**
- Favoráveis
- Neutros
- Contrários
- Sabotadores

### Níveis de requisitos
1. **Requisitos de usuários:** Pessoas envolvidos no uso e aquisicao do sisetma
2. **Requisitos do sistema:** Funcoes que o sistema deve fornecer (Programacao)
3. **Regra de negócio:** Orientacões e restricoes que como  a empresa opera seu negocio

**Nível de Generalizacao
![[Pasted image 20241030210143.png]]**

### Requisitos Funcionais
> os quais dizem respeito à definição das funções que um sistema ou um componente de sistema deve fazer (entradas e saídas).

**Exemplos ::**
- [RF001] O sistema deve cadastrar médicos profissionais (entrada). 
- [RF002] O sistema deve emitir um relatório de clientes (saída). 
- [RF003] O sistema deve transferir um cliente da situação “em consulta” para “consultado”, quando esse cliente terminar de ser atendido (mudança de estado). 
- [RF004] O cliente pode consultar os seus dados no sistema.

#### Importância dos requisitos funcionais:
> Funcionalidade do sistema existem, somente, para realizar Requisitos Funcionais, sem eles não há funcionalidade, sem funcionalidade sem sistema.

- **Requisitos funcionais de qualidade devem atender alguns atributos qualitativos** 
	-  Unidade, completude, consistência, atomicidade, não ambiguidade, ser verificável e rastreável

| Atributo        | Descrição                                                                                  |
|------------------|------------------------------------------------------------------------------------------|
| **Unidade**      | Propor apenas uma necessidade específica.                                                 |
| **Completude**   | Ser autocontido, com início, meio e fim.                                                |
| **Consistência** | Não contradizer outros requisitos funcionais.                                            |
| **Atomicidade**  | Assumir uma única responsabilidade, indivisível.                                       |
| **Não ambiguidade** | Ser claro e específico, sem proposições vagarosas.                                     |
| **Verificável**  | Ser testável, validável quanto à necessidade do cliente.                                 |
| **Rastreável**   | Possibilidade de rastreamento no sistema.                                               |
| **Tempo verbal** | Utilizar verbos de ação que indiquem o que será feito (ex: realizar, comprar).         |

Espero que isso ajude nas suas anotações!


### Requisitos não Funcionais
> Diz respeito as restricoes: desempenho, interface de usuário, seguranca, permissoes e etc

- Sempre que possível escritos quantitativamente

**Exemplos::**
- [RNF001] O sistema deve imprimir o relatório em até cinco segundos. 
- [RNF002] Todos os relatórios devem seguir o padrão de relatórios especificado pelo setor XYZ. 
- [RNF003] O sistema deve ser implementado em Java. 
- [RNF004] O sistema deve ser protegido para o acesso de usuários.

#### Divisão de tipo de requisitos
- **Requisitos  do produto**:
	-> Especificam ou restringem o comportamento de um software
		-> Rapidez do sistema e quantas memória deve receber
		-> Estabelecer taxa de erros aceitáveis.
- **Requisitos organizacionais:**
	-> Requisitos do sistema derivado das políticas e organizacao do cliente e do desenvolverdore
	 -> Como o sistema será usado
	 -> Qual linguagem de programacao utilziada, ambiente de desenvolvimente ou normas a serem utilizadas
	 -> Ambiente operacional do sistema
- **Requisitos Externos:**
	-> Requisitos derivados de fatores externos
		->O que deve ser feito para o sistema ser aprova ao uso uso por um regulador(banco central). **(Requisito regulador)**
		-> Garantir que o sistema opere dentro da Lei (Requisito legal)
		-> O sistema seja aceitável para seus usuários (Requisito ético)

> Geralmente os RNFs são **mensuráveis**, ou seja para cada requisito não funcional deverá associar uma medida ou referência.

#### Importância dos requisitos funcionais:

**Exemplo:**
> A empresa de transportes XYZ possui uma frota de 600 caminhões, mas eles não podem ficar esperando muito tempo no pátio, mesmo para saí- rem dos armazéns de carga. A empresa solicitou que, no módulo de logís- tica, todas as cargas devem ser liberadas em, no máximo, 15 minutos. Para isso, é emitido um documento de solicitação de liberação de carga, nele é anexado a nota fiscal eletrônica dos produtos contidos no caminhão.

**Identificando o requisitos não funcional:**
- [RNF01] Requisito de Desempenho: tempo limite de, no máximo, 12 minutos para o processamento de solicitação de liberação de carga.

Os desenvolvedores ignoraram o Requisito Não Funcional (RNF01) sobre o tempo de resposta da nota fiscal, planejando implementá-lo no final do projeto. Durante os testes, o sistema levou 1 hora para liberar a carga, sendo reprovado pelos usuários de logística. Como resultado, o sistema foi considerado inviável e precisou de uma reestruturação total para melhorar a performance.


**Exemplo:**

| Propriedade       | Exemplo de métricas                                                                                                         |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Velocidade        | Transações processadas/segundo, Tempo de resposta de usuário/evento, Tempo de atualização de tela                           |
| Facilidade de Uso | Tempo de treinamento, Número de frames (telas) de ajuda                                                                     |
| Confiabilidade    | Tempo médio para falha, Probabilidade de indisponibilidade, Taxa de ocorrência de falhas, Disponibilidade                   |
| Robustez          | Tempo de reinício após falha, Percentual de eventos que causam falhas, Probabilidade de corrupção de dados em caso de falha |
| Portabilidade     | Percentual de declarações dependentes do sistema-alvo, Número de sistemas-alvo                                              |

### Requisitos de domínio/Negócio (RDs)
> São os requisitos derivados do domínio da aplicação. Descrevem as características do sistema e as qualidades que refletem a regra de negócio do cliente.

>**Cenário de negócios e Domínio:** Domínio são requisitos voltados a área específica de negócio do clientes

- Podem ser novos requisitos funcionais ou algumas restricao de algum requisitos existente, ou calculo

**Exemplo:**
- [RD001] O cálculo da média final de cada aluno é dado pela fórmula: (Nota1 * 2 + Nota2 * 3)/5. 
- [RD002] O valor do IPI é calculado em relação ao valor da nota fiscal da mercadoria despachada e pode, eventualmente, incluir valores sobre o frete e despesas acessórias (juros, taxas etc.). 
- [RD003] O cálculo de comissão dos vendedores é de 15% sobre o total líquido das vendas no mês.

1. **Impactos da Ambiguidade nos Requisitos**
	- Ambiguidade leva a implementações inadequadas e retrabalho, gerando insatisfação do cliente.

2. **Consequências de Mudanças nos Requisitos**
	- Novos requisitos causam atrasos e aumentam custos, afetando cronograma e viabilidade do projeto.

### Valores do manifesto ágil...

###  Priorização dos requisitos de software
- Os mais prioritário para o início da lista.

**Ordem de execução**
- **Essencial**:
  - Imprescindível para o funcionamento do sistema.
  - Deve ser disponibilizado na implantação.

- **Importante**:
  - Permite o funcionamento do sistema de forma satisfatória.
  - Não impede a implantação, mas deve ser implementado rapidamente.

- **Desejável**:
  - Não compromete as funcionalidades básicas do sistema.
  - Pode ser entregue em qualquer momento sem prejuízo para os serviços.


#### Documento de Requisitos de Software (rever)

**Função:**
- Documentar acordos entre solicitantes e desenvolvedores.
- Estabelecer o escopo e as funcionalidades do software.
- Servir de referência para desenvolvimento, testes, manutenção e evolução.

**Usuários do Documento:**
- **Clientes:** Especificam e conferem requisitos.
- **Gerentes:** Planejam propostas e processos de desenvolvimento.
- **Engenheiros de Sistema:** Compreendem o sistema a ser desenvolvido.
- **Engenheiros de Testes:** Desenvolvem testes de validação.
- **Engenheiros de Manutenção:** Entendem o sistema e suas partes.

**Importância:**
- Essencial em desenvolvimento terceirizado ou por equipes diferentes.
- Garante entendimento e atualizações constantes.

##### Estrutura do Documento de Requisitos (exemplo de itens):

1. **Prefácio:** Leitores e histórico de versões.
2. **Introdução:** Necessidades e funções do sistema.
3. **Glossário:** Definição de termos técnicos.
4. **Definição de Requisitos de Usuário:** Serviços fornecidos.
5. **Arquitetura do Sistema:** Visão geral e distribuição de funções.
6. **Especificação de Requisitos:** Detalhes de requisitos funcionais e não funcionais.
7. **Modelagem do Sistema:** Modelos gráficos de relacionamentos.
8. **Evolução do Sistema:** Mudanças previstas.
9. **Apêndices:** Informações adicionais.
10. **Índice:** Índices alfabéticos e de diagramas.

##### Exemplo de Requisitos (SGCA):

- **Objetivos:** Sistema online para gerenciar casas de apoio social.
- **Requisitos Funcionais:** Ex: RF001 - Login de usuário.
- **Requisitos Não Funcionais:** Ex: RNF001 - Suporte a usuários simultâneos.
- **Escopo não contemplado:** Relatórios e atendimento por e-mail.
# Questões
> Preciso fazer
