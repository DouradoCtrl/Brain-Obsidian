#Database/Questões/AE3
#### No contexto dos bancos de dados, uma transação é uma unidade de trabalho que deve ser realizada de maneira completa ou não realizada de forma alguma. As transações têm propriedades específicas que garantem a integridade dos dados. Abaixo estão algumas afirmações sobre as propriedades das transações (Yanaga; Pedroso, 2023).  
Fonte: YANAGA, E.; PEDROSO, V de M. **Banco de Dados**. Maringá.: Unicesumar, 2016. [Reimpresso em 2023]..
##### Considerando o texto apresentado, sobre as propriedades ACID das transações são verdadeiras, analise as seguintes afirmativas:  
I. A propriedade de Atomicidade garante que todas as operações de uma transação sejam completamente realizadas ou nenhuma delas seja realizada.  
II. A propriedade de Consistência assegura que uma transação leve o banco de dados de um estado consistente para outro estado também consistente.  
III. A propriedade de Isolamento permite que uma transação veja as mudanças feitas por outras transações antes de serem concluídas.  
IV. A propriedade de Durabilidade assegura que, uma vez que uma transação é confirmada, seus efeitos são permanentes, mesmo no caso de uma falha de sistema. 
V. A propriedade de Atomicidade garante que as operações de uma transação possam ser parcialmente realizadas, desde que a maioria seja bem-sucedida.  
##### É correto o que se afirma em:  
- Alternativa 1: I, II e III, apenas.
- Alternativa 2: I, II e IV, apenas.
- Alternativa 3: I, III e V, apenas.
- Alternativa 4: II, IV e V, apenas.
- Alternativa 5: III, IV e V, apenas.
??
- Alternativa 2: I, II e IV, apenas.

---
#### Para criar uma tabela com o título "Status" no SGBD PostgreSQL, João utilizou o seguinte comando:  
CREATE TABLE status (  
Id serial not null primary key,  
Nome character varying(50) not null  
##### Observe que João utilizou a palavra reservada "primary key" para definir a coluna Id, da tabela de Status, como chave primária. Referente a chave primária de uma tabela, podemos afirmar que:  
- Alternativa 1: A chave primária, ou do inglês primary key, diz que o valor do campo é sequencial.
- Alternativa 2: Podemos gravar dados nulos em uma coluna definida como primary key, ou chave primária.
- Alternativa 3: Para interligar duas tabelas em um banco de dados, utilizamos o comando primary key, ou chave primária.
- Alternativa 4: A chave primária, ou do inglês primary key, diz ao banco de dados que o valor do campo Id não pode se repetir, ou seja, é único.
- Alternativa 5: É possível que o valor de uma chave primária, ou do inglês primary key, possa se repetir de forma que garanta a integridade do servidor.
??
- Alternativa 4: A chave primária, ou do inglês primary key, diz ao banco de dados que o valor do campo Id não pode se repetir, ou seja, é único.

---
#### Dentro de um sistema, as entidades relacionam-se uma com as outras. A partir da criação de relacionamentos, temos em modelagem o conceito de ocorrências entre entidades, que é conhecido como Cardinalidade.  
##### Baseado neste conceito, analise o relacionamento abaixo:  
![](https://sistemasead.unicesumar.edu.br/flex/amfphp/services/Portal/ImagemQuestionario2/QUE_222359_397405_1.jpg)  
I – Neste relacionamento, temos como entidades EMPREGADO, PROJETO e CONTÉM;  
II – Neste relacionamento, temos a cardinalidade Um para Muitos;  
III – Neste relacionamento, temos a cardinalidade Muitos para Muitos;  
IV – Neste relacionamento, temos a cardinalidade Um para Um.  
##### É correto o que afirma em:
- Alternativa 1: I, apenas.
- Alternativa 2: III, apenas.
- Alternativa 3: I e III,  apenas.
- Alternativa 4: III e IV, apenas.
- Alternativa 5: I, III e IV, apenas.
??
- Alternativa 2: III, apenas.

---
#### A notação de Chen é uma técnica popular para modelagem de dados em bancos de dados relacionais, desenvolvida por Peter Chen. Compreender os elementos e símbolos utilizados na notação de Chen é fundamental para criar modelos de dados precisos e compreensíveis (Yanaga; Pedroso, 2016).
Fonte: YANAGA, E.; PEDROSO, V. de M. **Banco de Dados**. Maringá: Unicesumar, 2016. [Reimpresso em 2023].  
##### Considerando o texto apresentado, relacionado aos elementos básicos utilizados na notação de Chen para modelagem de dados, analise as sentenças a seguir:
I. Entidades são representadas por retângulos e descrevem os objetos sobre os quais informações serão armazenadas no banco de dados.  
II. Atributos pode ser representado por elipses, e descrevem as características ou propriedades das entidades, sendo obrigatória a sua representação.  
III. Relacionamentos são representados por linhas e indicam como as entidades estão conectadas umas às outras no modelo de dados.  
IV. A cardinalidade é indicada por símbolos como "1" e "N", representando o número máximo de ocorrências de uma entidade que podem estar associadas a outra entidade.  
V. As chaves primárias são destacadas nas entidades por uma linha sublinhada e as chaves estrangeiras não representadas em negrito.  
##### É correto o que se afirma em:  
- Alternativa 1: I e II, apenas.
- Alternativa 2: I e IV, apenas.
- Alternativa 3: I e V, apenas.
- Alternativa 4: II e III, apenas.
- Alternativa 5: III e V, apenas.
??
- Alternativa 1: I e IV, apenas.

---
#### A informação é muitas vezes a coisa mais valiosa das empresas, mantê-las e poder acessá-las sempre que necessário é primordial para tomar decisões importantes. Mas controlar o acesso a essas informações também é importantíssimo. Já pensou se elas caíssem em mãos erradas? E a perda de informações? Já imaginou se estragasse o HD do servidor onde está o banco de dados? Backup é uma forma de garantir que informações não serão perdidas. 
Disponível em: ​https://dicasdeprogramacao.com.br/o-que-e-um-sgbd/. Acessado em: mar.2022.
###### Diante das vantagens de se utilizar um Sistema Gerenciador de Banco de dados (SGBD), leia as alternativas:  
I – Um SGBD centraliza todas as informações, fazendo com que todos os usuários acessem os mesmos dados. Podemos chamar isto de diminuir a redundância e fornecer consistência. 
II – Um SGBD deve oferecer uma combinação de login e senha para acesso a um determinado banco de dados, ou seja, segurança de acesso da informação ou controle de acesso.  
III – Um SGBD deve permitir formas de consultas eficientes aos dados gravados.  
IV – Um SGBD deve fornecer ferramentas que permitam backup do Banco de Dados e restauração em caso de desastre.  
##### É correto o que se afirma em:  
- Alternativa 1: I, apenas.
- Alternativa 2: I e II, apenas.
- Alternativa 3: I e III, apenas.
- Alternativa 4: I, II e III, apenas.
- Alternativa 5: I, II, III e IV.
??
- Alternativa 5: I, II, III e IV.

---
#### No modelo relacional de bancos de dados, os domínios dos atributos desempenham um papel crucial na definição dos tipos de dados que podem ser armazenados em um banco de dados. Compreender os conceitos relacionados aos domínios é fundamental para garantir a consistência e integridade dos dados.  
Fonte: YANAGA, E.; PEDROSO, V. de M. **Banco de Dados**. Maringá: Unicesumar, 2016. [Reimpresso em 2023].  
##### Considerando o texto apresentado, relacionado ao domínio dos dados, analise as afirmativas a seguir:
I. Em um modelo relacional, os domínios são opcionais e podem ser omitidos se não forem necessários para a aplicação.   
II. A definição de domínios permite que os atributos sejam associados a múltiplos tipos de dados, tornando-os mais flexíveis em termos de manipulação e armazenamento de informações.  
III. Os domínios definem os tipos de dados que podem ser armazenados em um atributo, especificando restrições como tamanho máximo, formato e valores permitidos.   
IV. A utilização de domínios facilita a manutenção e o gerenciamento de bancos de dados, uma vez que as definições de tipos de dados são centralizadas e podem ser modificadas em um único local.   
V. Os domínios garantem a consistência e a integridade dos dados, evitando que valores inválidos sejam inseridos nos atributos.   
##### É correto o que se afirma em:  
- Alternativa 1: I, II e III, apenas.
- Alternativa 2: I, II e V, apenas.
- Alternativa 3: I, IV e V, apenas.
- Alternativa 4: II, IV e V, apenas.
- Alternativa 5: III, IV e V, apenas.
??
- Alternativa 5: III, IV e V, apenas.
 
---
#### Bancos de dados ou bases de dados são coleções organizadas de dados que se relacionam de forma a criar algum sentido (Informação) e dar mais eficiência durante uma pesquisa ou estudo. São de vital importância para empresas, e há duas décadas se tornaram a principal peça dos sistemas de informação. Normalmente existem por vários anos sem alterações em sua estrutura.  
Disponível em: ​https://www.devmedia.com.br/gerenciamento-de-banco-de-dados-analise-comparativa-de-sgbd-s/30788. Acessado em: mar.2022.
##### Um sistema gerenciador de banco de dados (SGBD) trata-se de uma coleção de programas que permite aos usuários criar e manter um banco de dados. Partindo desta afirmação, assinale a alternativa que contenha apenas SGBDs Não Relacionais (NoSQL):
- Alternativa 1: MongoDB, Redis, Neo4j e Riak.
- Alternativa 2: MongoDB, Access, Oracle e Redis.
- Alternativa 3: DB2, SQL Server, Riak e MongoDB.
- Alternativa 4: Oracle, PostgreSQL, MySQL, Neo4j e Riak.
- Alternativa 5: Oracle, DB2, SQL Server, PostgreSQL e MongoDB.
??
- Alternativa 1: MongoDB, Redis, Neo4j e Riak.

---
#### Nunca geramos tantos dados o quanto estamos gerando nos dias atuais. E um dos nossos grandes desafios com o volume de dados gerados é encontrar uma forma eficiente de processá-los e ainda criar informação para gerar conhecimento e, consequentemente, riqueza. E para armazenar toda essa riqueza de forma segura e confiável, utilizamos os Bancos de Dados.  
##### Considerando o contexto acima, analise as alternativas a seguir referente a definição de banco de dados: 
- Alternativa 1: Banco de dados é um computador onde posso armazenar vários arquivos para consulta futura.
- Alternativa 2: Banco de dados é uma coleção de hardwares que permite aos usuários criar e manter seus arquivos seguros.
- Alternativa 3: Banco de dados é uma coleção de dados. Os dados são fatos que podem ser gravados e alterados, e que possuem um significado implícito.
- Alternativa 4: Banco de dados é um recurso de gerenciamento e administração que utiliza ferramentas de apoio para gerir suas tarefas e apresentar falhas de hardware.
- Alternativa 5: Banco de dados se refere a capacidade de gerar valor com as informações que podemos manipular e armazenamento vitalício da informação, sem nunca sofrer qualquer alteração.
??
- Alternativa 3: Banco de dados é uma coleção de dados. Os dados são fatos que podem ser gravados e alterados, e que possuem um significado implícito.
