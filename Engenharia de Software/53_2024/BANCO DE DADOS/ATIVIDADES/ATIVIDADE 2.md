# Questão 1
---
Analise a tabela abaixo:  
   
**Tabela:** VENDEDOR  
![](https://sistemasead.unicesumar.edu.br/flex/amfphp/services/Portal/ImagemQuestionario2/QUE_222214_394022_1.png)  
  
Baseando-se nos dados da tabela, assinale a alternativa que contém o resultado da execução da seguinte consulta:  
   
UPDATE VENDEDOR  SET VEND_PERC = 15  WHERE VEND_COD = 2;

Alternativas:
- a. Após a execução será alterado o percentual do vendedor Marcos Pontes para 15.
	- errado
- b. Após a execução será alterado o percentual do vendedor Danilo Almeida para 2.
	- errada
- c. Após a execução será alterado o percentual da vendedora Amanda Silva para 15.
	- certo
- d. Após a execução será alterado o percentual do vendedor Maurício Freitas para 15.
	- errada
- e. Após a execução será alterado o percentual da vendedora Vivian Moura para 2.
	- errada

# Questão 2
---
As [[TRANSAÇÕES|transações]] em sistemas de bancos de dados desempenham um papel crucial na garantia da integridade e consistência dos dados. Compreender os conceitos relacionados às transações é essencial para o desenvolvimento e a manutenção de aplicações confiáveis.  
  
Fonte: YANAGA, E.; PEDROSO, V. de M. **Banco de Dados**. Maringá: UniCesumar, 2016.

  
Sobre a importância das transações em sistemas de bancos de dados, analise as afirmativas a seguir:  
  
I. As propriedades ACID de transações significam Atomicidade, Coerência, Integrabilidade e Durabilidade.  
II. As transações garantem a consistência dos dados, permitindo que as operações sejam executadas de forma isolada, sem interferência de outras transações.   
III. Uma das vantagens das transações é a recuperação de dados em caso de falha do sistema, garantindo que as alterações sejam duráveis e não perdidas.   
IV. Transações não são necessárias em ambientes de banco de dados, pois as operações podem ser realizadas individualmente sem risco de inconsistência nos dados.   
V. O isolamento das transações não é implementado pelo SGDB relacional, já que o acesso simultâneo aos dados por várias transações é necessário, e não afeta a consistência dos resultados.  
  
​É correto o que se afirma em:

Alternativas:

- a. I e II, apenas.
	- errado
- b. I e IV, apenas.
	- errado
- c. II e III, apenas.
	- certo
- d. III e IV, apenas.
	- errado
- c. IV e V, apenas.
	- errado

# Questão 3
---
Para um sistema de Banco de Dados aplicado numa média e complexa atividade, existem algumas pessoas envolvidas, desde o projeto até a manutenção propriamente dita.  
 
Disponível em: https://bit.ly/2W9S4Bw Acessado em: 16/03/2021 (Adaptado)
   
A partir disso, e baseando-se nos Papéis assumidos pelos usuários de SGBDs, analise as afirmações abaixo e assinale a alternativa que contempla apenas funções que podem ser executadas por usuários finais em um SGBD:  
   
I - O usuário final pode criar consultas em SQL.  
II - O usuário final faz projeção e administração do um banco de dados.  
III - O usuário final é responsável por projetar e codificar a construção do SGBD.  
IV - O usuário final faz a interação com as aplicações e não diretamente com o banco de dados.  
   
É correto o que se afirma em:

- a. I, apenas.
	- errado
- b. IV, apenas.
	- errado
- c. I e IV, apenas.
	- certo
- d. II, III e IV, apenas.
	- errado
- e. I, II, III, IV.
	- errado

# Questão 4
---
Uma transação é uma sequência de operações executadas como uma única unidade lógica de trabalho. ACID é um conceito que se refere às quatro propriedades de transação de um sistema de banco de dados: Atomicidade, Consistência, Isolamento e Durabilidade.  
  
Considerando o texto acima, analise as afirmativas a seguir:   
  
​I - Durabilidade diz respeito à conclusão de uma transação, caso uma transação tenha sido finalizada com sucesso, seus dados deverão estar armazenados corretamente.  

II - Atomicidade tem como pressuposto que a transação seja executada por completo ou não seja executado nada.  

III - O isolamento transacional proporciona que o resultado de uma sequência de execuções tenham o resultado diferente entre uma e outra execução.  

IV - Consistência refere-se ao estado do dado armazenado, este deve estar de modo conciso e imutável seguindo exclusivamente as regras de negócio do sistema implementado sem restrições.    
  
É correto o que se afirma em:

- a. I e II apenas
	- Certo
- b. III e IV apenas.
	- Errada
- c. I, II, III apenas
	- Errada
- d. II, III, IV apenas
	- Errada
- e. I, II, III, IV.
	- Errada.

# Questão 5
---
As propriedades ACID (Atomicidade, Consistência, Isolamento e Durabilidade) são fundamentais para garantir a integridade e a confiabilidade das transações em sistemas de bancos de dados. Conhecer como essas propriedades se relacionam com as características e vantagens do uso de um SGBD é essencial para entender seu impacto na gestão de dados.  
 
Fonte: YANAGA, E.; PEDROSO, V. de M. **Banco de Dados**. Maringá: UniCesumar, 2016.
  
Considerando o texto apresentado, na relação entre as propriedades ACID e as características e vantagens do uso de um SGBD, analise as afirmativas a seguir:  
  
I. A propriedade de Durabilidade garante que os efeitos de uma transação confirmada sejam permanentes, mesmo no caso de falhas no sistema, o que contribui para a confiabilidade e a recuperação de dados.   

II. Os SGBDs geralmente não oferecem suporte à propriedade de Isolamento, o que pode resultar em problemas de concorrência e inconsistências nos dados.   

III. A propriedade de Atomicidade assegura que as transações sejam realizadas completamente ou não realizadas de forma alguma, contribuindo para a integridade dos dados em um SGBD.   

IV. As propriedades ACID aumentam a complexidade do uso de um SGBD e podem impactar negativamente o desempenho das operações de gerenciamento de dados.  

V. A propriedade de Consistência garante que o banco de dados permaneça em um estado consistente antes e após a execução de uma transação, promovendo a confiabilidade das operações.   
  
É correto o que se afirma em:

- a. I, II e III, apenas.
	- Errada
- b. I, III e V, apenas.
	- Certa.
- c. I, IV e V, apenas.
	- Errada
- d. II, III e IV, apenas.
	- Errada.
- e. III, IV e V, apenas.
	- Errada.
# Questão 6
---
O Modelo Relacional é uma abordagem fundamental em bancos de dados que organiza os dados em tabelas relacionadas. Compreender as características desse modelo é essencial para o projeto e a implementação eficazes de sistemas de banco de dados relacionais.

Fonte: YANAGA, E.; PEDROSO, V. de M. **Banco de Dados**. Maringá: UniCesumar, 2016.

Considerando o texto apresentado, relacionado ao modelo relacional, analise as afirmativas a seguir:  
​  
I. Apesar do modelo relacional trabalhar com a definição prévia do esquema de tabelas, no momento da inserção de dados em uma relação, podem ser inseridos campos não definidos para a entidade no esquema, desde que contenha os campos pré-especificados. 

II. As tabelas no Modelo Relacional são organizadas em linhas e colunas, em que cada linha representa uma entidade e cada coluna representa um atributo dessa entidade.  

III. No Modelo Relacional, as chaves primárias são utilizadas para identificar exclusivamente cada registro em uma tabela e as chaves estrangeiras são usadas para estabelecer relacionamentos entre tabelas.  

IV. No modelo relacional, uma chave estrangeira referencia uma chave primária na tabela referenciada, sendo que uma chave estrangeira também pode ser, ao mesmo tempo, uma chave primária.  

V. As chaves estrangeiras seguem as mesmas restrições impostas às chaves primárias.  
  
​É correto o que se afirma em:

- a. I, II e III, apenas.
	- errado.
- b. I, III e IV, apenas.
	- errado.
- c. II, III e V, apenas.
	- certo.
- d. II, III e IV, apenas.
	- errado.
- e. III, IV e V, apenas.
	- errado.

# Questão 7
---
Os sistemas de bancos de dados desempenham um papel crucial na gestão eficiente e segura de grandes volumes de dados em ambientes computacionais. Conhecer suas características e vantagens é fundamental para a compreensão de seu funcionamento e aplicabilidade.  
  
Fonte: YANAGA, E.; PEDROSO, V. de M. **Banco de Dados**. Maringá: UniCesumar, 2016.  
  
​Considerando o texto apresentado, sobre as características e vantagens dos sistemas de bancos de dados, analise as afirmativas a seguir:  
  
I. A escalabilidade é uma característica dos sistemas de bancos de dados que permite aumentar sua capacidade para lidar com um volume crescente de dados sem comprometer o desempenho.  

II. Uma das vantagens dos SGBDs é a redução da redundância e inconsistência dos dados, promovendo a integridade e a consistência das informações armazenadas.  

III. Os sistemas de bancos de dados geralmente não oferecem suporte à segurança dos dados, tornando-os vulneráveis a acessos não autorizados.  

IV. A independência de dados é uma característica dos SGBDs que permite que os programas de aplicação sejam modificados sem afetar a estrutura dos dados subjacentes. 

V. Utilizar um SGBD aumenta significativamente os custos operacionais, tornando-o menos acessível para pequenas e médias empresas.  
  
É correto o que se afirma em:

- a. I e II, apenas.
	- Certo
- b. I e III, apenas.
	- Errada
- c. I e V, apenas.
	- Errada.
- d. II e IV, apenas.
	- Certo
- e. III e IV, apenas.
	- Errada.
# Questão 8
---
Um SGBD pode ser considerado um dos pontos vitais de qualquer sistemas, visto que de nada importa ter um sistema sem ter dados a serem armazenados, manipulados e analisados. Atualmente, cada vez mais empresas utilizam os dados armazenados para auxiliar a alta gestão nas tomadas de decisões estratégicas. Um SGBD deixou de ser artefato do sistema, por isso a alegação deste ser um item vital para a empresa. No mercado atual escutamos falar muito sobre os vários tipos de SGBD (Relacional, NoSQL e NewSQL). 

Com base no contexto apresentado e em nossos estudos na disciplina, analise as alternativas a seguir, indique qual desta contém apenas SGBD Relacionais

- a. Riak, Access, DB2, Redis
	- Errado.
- b. MySQL, DB2, Neo4j, Riak
	- Errado.
- c. Derby, Oracle, H2, SQL Server
	- Certo.
- d. SQL Server, Derby, Redis, Neo4j
	- Errado.
- e. PostgreSQL, MongoDB, Redis, MySQL
	- Errado.

# Questão 9
---
**Tabela:** VENDEDOR  
![](https://sistemasead.unicesumar.edu.br/flex/amfphp/services/Portal/ImagemQuestionario2/QUE_222214_394019_1.png)  
Baseando-se nos dados da tabela, assinale a alternativa que contém o resultado da execução da seguinte consulta:  
   
SELECT * FROM VENDEDOR;

Alternativas:

- a. 10
	- Errada.
- b. 36
	- Errada.
- c. Vivian
	- Errada.
- d. Danilo Almeida
	- Errada.
- e. Todas as colunas e linhas da tabela vendedor.
	- Certa.
# Questão 10
---
Os sistemas de bancos de dados desempenham um papel fundamental na organização e manipulação de dados em ambientes computacionais. Eles possuem características específicas e oferecem [[VANTAGENS DE SE UTILIZAR UM SGBD|vantagens]] distintas em comparação com abordagens tradicionais de armazenamento de dados.

Fonte: YANAGA, E.; PEDROSO, V. de M. **Banco de Dados**. Maringá: UniCesumar, 2016.
  
Considerando o texto apresentado, sobre as [[CARACTERÍSTICA DE SISTEMAS DE BANCO DE DADOS|características]] e [[VANTAGENS DE SE UTILIZAR UM SGBD|vantagens]] dos sistemas de bancos, analise as afirmativas a seguir:  
  
I. Os sistemas de bancos de dados oferecem redundância controlada, o que significa que os dados são armazenados de forma organizada e sem duplicações desnecessárias.   

II. Uma das vantagens de se utilizar um SGBD é a garantia de integridade dos dados, através de mecanismos como chaves estrangeiras e restrições de integridade.  

III. Os sistemas de bancos de dados não oferecem suporte a transações, tornando-os inadequados para ambientes que exigem atomicidade e consistência nos dados.   

IV. Uma das características dos sistemas de bancos de dados é a independência de dados, o que permite alterar a estrutura do banco sem afetar os programas que o utilizam.   

V. Utilizar um SGBD aumenta a complexidade do gerenciamento de dados, tornando-o mais difícil de manter em comparação com o uso de arquivos tradicionais.  
  
​É correto o que se afirma em:

Alternativas:

- a. I, II e III, apenas.
	- Incorreta.
- b. I, II, e IV, apenas.
	- Correta.
- c. I, III e V, apenas.
	- Incorreta.
- d. II, IV e V, apenas.
	- Incorreta.
- e. III, IV e V, apenas.
	- Incorreta.