**Atividade de Estudo: Normalização em [[BANCO DE DADOS|Banco de dados]]**
  
**Objetivo**: esta atividade tem como objetivo incentivar a pesquisa e a compreensão dos conceitos de [[Normalização em bancos de dados relacionais]]. Através desta atividade, você deverá explorar o que é a normalização, os diferentes níveis de formas normais e a importância da normalização para a integridade e eficiência dos dados.

  
**1. Pesquisa sobre o conceito de normalização em bancos de dados relacionais. Em sua pesquisa, busque responder às seguintes questões**:  
  
• [[Normalização do banco de dados|O que é normalização?]]
• [[Quais são os objetivos da normalização?]]  
• [[Formas de Normalização ou Formas Normais|Quais são as principais formas normais (1FN, 2FN, 3FN)?]]  
  
**2. Pesquise sobre a aplicação da normalização, buscando responder às seguintes questões**:  
  
• Explique o motivo de a normalização ser importante no design de banco de dados.  
• Descreva como a normalização pode ajudar a evitar problemas de redundância e inconsistência de dados.  
  
**Critérios de Avaliação**:  
  
• Demonstração de uma compreensão clara e completa dos conceitos de normalização.  
• Qualidade e profundidade da pesquisa realizada, com referências bem citadas.    
• Clareza e organização do relatório.  
    
**Dicas para realizar a atividade**:  
  
Durante as aulas, o professor fornecerá dicas que podem ser utilizadas para a confecção das suas atividades. Assim, é de suma importância participar das aulas ao vivo ou assisti-las posteriormente.  
Assista às aulas conceituais da disciplina.  
   
**Orientações**:  
  
Plágios e cópias indevidas serão penalizados com descontos na nota, podendo chegar a zero.  
Não são permitidas correções parciais no decorrer do módulo, pois a interpretação da atividade também faz parte da avaliação.  
Atenção ao prazo de entrega da atividade. Sugerimos que envie sua atividade antes do prazo final para evitar transtornos e lentidão nos servidores. Evite o envio de atividade em cima do prazo.  
   
**Boa atividade!**

# Resposta
---
## 1.1
Segundo a microsoft **normalização** é organizar os dados de um banco de dados. O ato de normalizar é criar tabelas com base em regras projetadas para diminuir a redundância, dependências inconsistentes e deixar o banco de dados mais leve. Além de organizar os dados em tabelas eficientes, ela torna o banco de dados mais seguro, uma vez que, para ter acesso a determinado dado, a tabela precisa referenciar uma chave estrangeira para a chave primária. Dessa forma, você pode ter controle sobre qual tabela pode ter acesso a qual tipo de dado. A normalização também torna o banco de dados mais flexível e facilita na criação do banco de dados.

## 1.2
De acordo com a microsoft, o objetivo principal é evitar uma redundância de dados e alguma dependência inconsistente que pode tornar o banco de dados desordenado.

## 1.3
A normalização é dividida em seis regras, mas as mais importantes são a 1NF, 2NF e 3NF.

**Primeira Forma Normal (1NF):**  
Para criar uma tabela na primeira forma normal, é necessário que as colunas contenham valores atômicos, ou seja, cada registro deve ser único. O objetivo dessa primeira regra é justamente eliminar a redundância nos dados, garantindo que cada célula da tabela tenha um valor único. Cada tabela deve ser estritamente separada por categoria e finalidade.

**Segunda Forma Normal (2NF):**  
Para converter uma tabela da 1NF para a 2NF, é necessário relacionar essas tabelas separadas com uma chave estrangeira, permitindo o compartilhamento de dados entre elas. Os registros dessas tabelas devem depender somente da chave primária.

**Terceira Forma Normal (3NF):**  
Como sugerido pela Alura, para que uma tabela esteja na 3NF, é preciso fazer uma abstração maior da 2NF, eliminando os campos que não dependem da chave primária e colocando-os em uma nova tabela que dependa da chave primária. Dessa forma se elimina qualquer dependência transitiva que exista nessas tabelas.

## 2.1
Supondo que você precise criar um banco de dados em SQL para um projeto de fidelização de pontos dos clientes, onde a cada fatura paga será somada uma pontuação referente ao pagamento, teremos três tabelas principais: `login`, `cliente` e `faturas`. Dentro dessas três tabelas, eu colocaria o campo `cliente` como `varchar(60)` triplicado em todas. Contudo, futuramente, se for necessário excluir um cliente porque ele cancelou o contrato, e você apagar apenas o registro da tabela de `login` para que o mesmo não tenha mais acesso ao sistema, o cliente ainda continuará pontuando no restante da aplicação. Isso gera dados desnecessários no banco de dados, o que pode futuramente atrapalhar o desempenho e a clareza das informações e também dificultar a manutenibilidade do banco de dados.

Supondo que você tivesse criado uma chave estrangeira que relacionasse essas três tabelas ao `cliente`, você poderia apagar os registros das tabelas com base na chave estrangeira e no atributo `código do cliente`, eliminando assim a redundância do banco de dados e facilitando a manutenção e a clareza das informações.

Caso queira saber, temos alguns exemplos parecidos nas referências abaixo.

Curiosidade: Esse exemplo citado é um exemplo prático de um projeto que estou desenvolvendo para a empresa a qual trabalho.

### O que é normalização ?

# Referência
---
1. **MICROSOFT.** Database normalization description. _Microsoft Learn_. Disponível em: [https://learn.microsoft.com/pt-br/office/troubleshoot/access/database-normalization-description](https://learn.microsoft.com/pt-br/office/troubleshoot/access/database-normalization-description). Acesso em: 24 ago. 2024.

2. **SOUZA, Brenda; PUIG, Luis Ezequiel.** Normalização de banco de dados: Estrutura. _Alura_. Disponível em: [https://wwrocópio na Redew.alura.com.br/artigos/normalizacao-banco-de-dados-estrutura?srsltid=AfmBOoqxDBpGvgjnP_n7xXaTt_inXnt4eS-c6xqr-3eJSzimR20nZmF1](https://www.alura.com.br/artigos/normalizacao-banco-de-dados-estrutura?srsltid=AfmBOoqxDBpGvgjnP_n7xXaTt_inXnt4eS-c6xqr-3eJSzimR20nZmF1). Acesso em: 24 ago. 2024.

3. **Procópio, Fábio.** _Normalização de Banco de Dados_. Disponível em: [https://www.youtube.com/watch?v=O2DFpgZbCTc](https://www.youtube.com/watch?v=O2DFpgZbCTc). Acesso em: 24 ago. 2024.

4. **MAIA, Daniel.** _Normalização de Banco de Dados - 1FN, 2FN e 3FN_. Disponível em: [https://www.youtube.com/watch?v=c_WGssorPYc](https://www.youtube.com/watch?v=c_WGssorPYc). Acesso em: 24 ago. 2024.

5. **MATOS, Léo.** _3 Formas Normalização: -1FN -2FN -3FN | Tabela do Banco de Dados | Concurso Banco do Brasil_. Disponível em: [https://youtu.be/__fBDQcESgs?si=1-dxnI3al8cunt0C](https://youtu.be/__fBDQcESgs?si=1-dxnI3al8cunt0C). Acesso em: 24 ago. 2024.