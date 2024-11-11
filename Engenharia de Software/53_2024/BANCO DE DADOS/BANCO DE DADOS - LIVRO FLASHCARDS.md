#Database/Livro

# Unidade 1

Transações tradicionalmente são melhor entendidas por meio do conjunto de suas propriedades ACID (Atomicidade, Consistência, Isolamento e Durabilidade). Em quais situações da vida real você consegue enxergar a necessidade de se executar operações com essas propriedades?
??
- Atomicidade se reflete, por exemplo, em transações bancárias. Enquanto o comprovante ou outra forma de confirmação da transação não é recebido por um cliente em um caixa eletrônico, a transação não é concretizada, pois esta característica visa garantir que as operações sempre ocorram por completo. (Tudo ou nada)
- Consistência se aplica a situações onde a impressão de um extrato bancário só é impresso se todos os dados que devam estar contidos nele já tenham sido processados de forma confiável, garantindo que a informação exibida é fiel aos dados reais do banco de dados. 
- Isolamento é extremamente útil em bancos de dados com acesso remoto de multiusuários como ocorre em terminais de autoatendimento de bancos onde mais de uma pessoa pode estar simultaneamente acessando os mesmos dados, como em sistemas de consulta de preços em lojas. 
- Durabilidade se refere a situações como a de transações bancárias terem a garantia de terem ocorrido de maneira completa, e sem o risco de interrupções não programadas que possam gerar a perda de informações parciais ou totais da transação por motivos diversos como interrupções na corrente elétrica, ou incidentes naturais.

Ao enumerar as vantagens de se utilizar um SBGD, fizemos uma comparação com a utilização de arquivos para armazenamento dos dados. Tendenciosamente, o SGBD apareceu como o vencedor nas comparações. Quais seriam as situações em que os arquivos seriam uma solução mais adequada? Você consegue exemplificar alguma outra situação em que uma terceira alternativa seria mais viável?
??
Quando há a necessidade do armazenamento de apenas um tipo de dado, um ar- quivo comum de texto pode resolver o problema, sem a necessidade de implemen- tação de um sistema de gerenciamento destes dados, ou em casos onde os dados armazenados sejam extremamente simples como na configuração e um maquinário. 
Uma combinação destes tipos de sistemas de armazenamento de dados em um sistema pode ocorrer devido a diferentes formas de tratamento de dados, sendo por exemplo possível a existência de arquivos de texto contendo entradas de dados vindos de um equipamento ser um SGBD que serve para alimentar um SGBD mais complexo como pode ocorrer em sistemas de monitoramento de maquinário em uma indústria, por exemplo.

Pense no SBGD como um módulo do sistema ou como uma outra aplicação a ser integrada (pois, em muitas concepções modernas, é assim que ele deve ser tratado). Uma das características dos SGBDs é o isolamento entre o programa e os dados. Quais os benefícios desse isolamento? Em que outras partes do sistema essa característica também pode trazer benefícios?
??
Uma base de dados pode ser acessada por mais de um sistema SGBD simultaneamente, e este isolamento, aumenta a consistência da base de dados, pois cada acesso de um SGBD a base funciona de forma mais segura.

# Unidade 2

A partir do estudado nesta unidade, defina Entidades Concretas e Entidades Abstratas.
??
Entidades Concretas são entendidas como objetos do mundo real que podem ser separadas e distinguíveis de outro objeto. Já as Entidades Abstratas são aquelas que não temos de maneira tangível (intangível).

Crie uma Entidade Produtos com os seguintes atributos: 
	a. Código do Produto. b. Descrição do Produto. 
	c. Unidade do Produto. 
	d. Valor do Produto. 
	e. Classificação do Produto. 
	f. Valor Custo do Produto.
??
![[Pasted image 20240919213759.png]]

Analise as frases abaixo e crie as possíveis entidades: 
	a. “o atendente matricula o aluno no curso de Administração”. 
	b. “ a secretária agenda pacientes para atendimento médico”. 
	c. “ é necessário cadastrar os produtos para realizar as vendas aos clientes”.
??
![[Pasted image 20240919213833.png]]

# Unidade 3

![[Pasted image 20240919200429.png]]
Considere o exemplo de schema da figura apresentada. Crie os comandos SQL para definição e criação das tabelas.
??
```sql
CREATE TABLE aluno (
    id INT PRIMARY KEY,
    nome VARCHAR(30),
    sobrenome VARCHAR(30),
    ra DECIMAL(8),
    email VARCHAR(30)
);

CREATE TABLE professor (
    id INT PRIMARY KEY,
    nome VARCHAR(30),
    sobrenome VARCHAR(30),
    titulacao VARCHAR(30)
);

CREATE TABLE curso (
    id INT PRIMARY KEY,
    nome VARCHAR(30),
    ano DECIMAL(4)
);

CREATE TABLE matricula (
    curso_fk INT NOT NULL,
    aluno_fk INT NOT NULL,
    PRIMARY KEY (curso_fk, aluno_fk),
    FOREIGN KEY (curso_fk) REFERENCES curso(id),
    FOREIGN KEY (aluno_fk) REFERENCES aluno(id)
);

CREATE TABLE disciplina (
    id INT PRIMARY KEY,
    nome VARCHAR(30),
    curso_fk INT NOT NULL,
    professor_fk INT NOT NULL,
    FOREIGN KEY (curso_fk) REFERENCES curso(id),
    FOREIGN KEY (professor_fk) REFERENCES professor(id)
);

```

![[Pasted image 20240919200429.png]]
Elabore consultas SQL para selecionar: 
	a. O nome de todos os alunos matriculados no curso com nome = ‘Banco de Dados’. 
	b. A titulação do professor da disciplina com nome = ‘SQL’. 
	c. O Nome, sobrenome e RA de todos os alunos matriculados nas disciplinas lecionadas pelo professor com nome ‘Edson’.
	d.  Todos os atributos de todos os cursos com ano > 1990.
??
```sql
-- a
SELECT aluno.nome FROM aluno, curso, matricula WHERE curso.nome = 'Banco de Dados' AND curso.id = matricula.curso_fk AND matricula.aluno_fk = aluno.id;

-- b
SELECT professor.titulacao FROM professor, disciplina WHERE disciplina.nome = 'SQL' AND disciplina.professor_fk = professor.id;

-- c
SELECT aluno.nome, aluno.sobrenome, aluno.ra 
FROM aluno, matricula, curso, disciplina, professor 
WHERE matricula.aluno_fk = aluno.id 
  AND matricula.curso_fk = curso.id 
  AND disciplina.curso_fk = curso.id 
  AND disciplina.professor_fk = professor.id 
  AND professor.nome = 'Edson';

-- d
SELECT id, nome, ano FROM curso WHERE ano>1990;

```

![[Pasted image 20240919200429.png]]
Elabore comandos de modificação de dados para incluir, modificar e remover linhas das diferentes tabelas desse schema.
??
```sql
INSERT INTO aluno (id, nome, sobrenome, ra, email) VALUES ('1', 'João', 'Silva', '100000', 'jao@email.com'); 

UPDATE curso SET ano = '2016' WHERE nome = 'Banco de Dados'; 

DELETE FROM professor WHERE id = '5';
```

# Unidade 4

![[Pasted image 20240919200756.png]]
Considere o exemplo de schema da figura apresentada. Crie os comandos SQL para definição e criação das tabelas.
??
```sql
CREATE TABLE plano (
    id INT PRIMARY KEY,
    nome VARCHAR(30),
    valor DECIMAL(7,2)
);

CREATE TABLE beneficiario (
    id INT PRIMARY KEY,
    nome VARCHAR(30),
    sobrenome VARCHAR(30),
    altura DECIMAL(3,2),
    plano_fk INT,
    FOREIGN KEY (plano_fk) REFERENCES plano(id)
);

CREATE TABLE dependente (
    id INT PRIMARY KEY,
    nome VARCHAR(30),
    sobrenome VARCHAR(30),
    beneficiario_fk INT NOT NULL,
    FOREIGN KEY (beneficiario_fk) REFERENCES beneficiario(id)
);
```

![[Pasted image 20240919200756.png]]
Elabore consultas SQL para:
	a. Selecione todos os beneficiários que possuem dependentes com o mesmo nome utilizando uma condição de JOIN. 
	b. Execute a mesma consulta anterior utilizando uma subquery. 
	c. Execute a mesma consulta anterior utilizando uma cláusula EXISTS. 
	d. Selecione o beneficiário que contém dependente que possui a maior
??
```sql
-- a
SELECT beneficiario.nome FROM beneficiario INNER JOIN dependente ON beneficiario.nome = dependente.nome;

-- b
SELECT beneficiario.nome FROM beneficiario WHERE nome IN ( SELECT nome FROM dependente WHERE beneficiario.nome = dependente.nome);

-- c
SELECT beneficiario.nome FROM beneficiario WHERE EXISTS ( SELECT * FROM dependente WHERE beneficiario.nome = dependente.nome );

-- d
SELECT nome FROM beneficiario WHERE ( SELECT MAX(altura) from dependente );
```

![[Pasted image 20240919200756.png]]
Utilizando a cláusula de GROUP BY, elabore consultas para:
	a. Agrupe os beneficiários por nome e selecione o sobrenome e a altura de cada um deles. 
	b. Selecione todos os beneficiários que contêm mais de um dependente com o mesmo sobrenome. 
	c. Selecione todos os planos que contêm mais de um beneficiário com altura > 1.75.
??
```sql
-- a
SELECT sobrenome, altura FROM beneficiario GROUP BY nome;

-- b
SELECT beneficiario.nome FROM beneficiario WHERE ( SELECT COUNT(*) FROM dependente WHERE dependente.beneficiario_fk=beneficiario.id and dependente.sobrenome=beneficiario.sobrenome GROUP BY beneficiario.nome) > 1

-- c
SELECT plano.nome FROM plano WHERE ( SELECT COUNT(*) FROM benefi- ciario WHERE beneficiario.altura > 1.75 AND beneficiario.plano_fk = plano.id );
```

# Unidade 4
> Apenas Executar um SQL como SCRIPT no gerenciador de um sistema de banco de dados

## Excluir Tabelas;
---
```sql
DROP TABLE VENDA; 
DROP TABLE VENDA_ITENS; 
DROP TABLE PRODUTOS; 
DROP TABLE CLIENTES; 
DROP TABLE VENDEDOR;
```

## Criar Tabelas;
---
```sql
CREATE TABLE PRODUTOS ( 
	PROD_CHAVE INTEGER PRIMARY KEY, 
	PROD_DESCRI VARCHAR(60), 
	PROD_VPRECO NUMERIC(18,4), 
	PROD_UNIDAD VARCHAR(5), 
	PROD_FAMILI VARCHAR(10) 
);

CREATE TABLE CLIENTES ( 
	CLI_CHAVE INTEGER PRIMARY KEY, 
	CLI_TIPOPESSOA CHAR(1), 
	CLI_STATUS VARCHAR(15), 
	CLI_BAIRRO VARCHAR(30), 
	CLI_ESTADO CHAR(2), 
	CLI_PAIS VARCHAR(6), 
	CLI_INSCRESTADUAL VARCHAR(25), 
	CLI_CEP VARCHAR(9), 
	CLI_CIDADE VARCHAR(35), 
	CLI_CNPJ_CPF VARCHAR(18), 
	CLI_ENDERE VARCHAR(60), 
	CLI_RAZAOSOCIAL VARCHAR(60), 
	CLI_NOMEFANTASIA VARCHAR(30), 
	CLI_EMAIL VARCHAR(60) 
);

CREATE TABLE VENDEDOR ( 
	VEN_CHAVE INTEGER PRIMARY KEY, 
	VEN_NOME VARCHAR(30), 
	VEN_CNPJ_CPF VARCHAR(18), 
	VEN_TIPOPESSOA CHAR(1), 
	VEN_INSCRESTADUAL VARCHAR(25), 
	VEN_STATUS VARCHAR(15), 
	VEN_EMAIL VARCHAR(60), 
	VEN_VPERCENT_COMIS NUMERIC(5,4) 
);

CREATE TABLE VENDA ( 
	VDA_CHAVE INTEGER PRIMARY KEY, 
	VDA_DMOVTO DATE, 
	VDA_VDINHEIRO NUMERIC(18,2), 
	VDA_VCARTAO NUMERIC(18,2), 
	VDA_VCHEQUE NUMERIC(18,2), 
	VDA_VPRAZO NUMERIC(18,2), 
	VDA_VOUTROS NUMERIC(18,2), 
	VDA_VTOTAL NUMERIC(18,2), 
	VDA_VRECEB NUMERIC(18,2), 
	VDA_VTROCO NUMERIC(18,2), 
	VDA_CODCLI_CLI INTEGER, 
	VDA_CODVEN_VEN INTEGER, 
	VDA_VDESC NUMERIC(18,2), 
	FOREIGN KEY (VDA_CODCLI_CLI) REFERENCES VENDA(CLI_CHAVE), 
	FOREIGN KEY (VDA_CODVEN_VEN) REFERENCES VENDEDOR(VEN_CHAVE)
);

CREATE TABLE VENDA_ITENS ( 
	VDI_CHAVE_VDA INTEGER, 
	VDI_NSEQUEN INTEGER, 
	VDI_CODPRO_PROD INTEGER, 
	VDI_QQUANTI NUMERIC(18,2), 
	VDI_VPREUNI NUMERIC(18,2), 
	VDI_VALORITEM NUMERIC(18,2), 
	VDI_PERCENTDESC NUMERIC(5,2), 
	VDI_QTDEDEVOLV NUMERIC(18,2), 
	VDI_DESCPROD VARCHAR(255), 
	PRIMARY KEY(VDI_CHAVE_VDA,VDI_NSEQUEN), 
	FOREIGN KEY (VDI_CHAVE_VDA) REFERENCES VENDA(VEN_CHAVE), 
	FOREIGN KEY (VDI_CODPRO_PROD) REFERENCES PRODUTOS (PROD_CHAVE)
);

```

## Excluir Entidades;
---
```sql
DELETE FROM VENDA_ITENS; 
DELETE FROM VENDA; 
DELETE FROM PRODUTOS; 
DELETE FROM CLIENTES; 
DELETE FROM VENDEDOR;
```

## Comandos de transação;
---
```sql
BEGIN; -- Inicia uma nova transação
ROLLBACK; -- Desfaz todas as operações realizadas na transação atual
COMMIT; -- Salva permanentemente as alterações feitas na transação
```

## Inserir Entidades;
---
```sql
INSERT INTO VENDEDOR (
    VEN_CHAVE, 
    VEN_NOME, 
    VEN_CNPJ_CPF, 
    VEN_TIPOPESSOA, 
    VEN_INSCRESTADUAL, 
    VEN_STATUS, 
    VEN_EMAIL, 
    VEN_VPERCENT_COMIS
) 
VALUES 
    (1, 'MARIA DAS GRAÇAS', 
    '302.027.591-13', 
    'F', 
    'ISENTO', 
    'ATIVO', 
    'vendas@hotmail.com', 
    1.5
);

INSERT INTO VENDEDOR (
    VEN_CHAVE, 
    VEN_NOME, 
    VEN_CNPJ_CPF, 
    VEN_TIPOPESSOA, 
    VEN_INSCRESTADUAL, 
    VEN_STATUS, 
    VEN_EMAIL, 
    VEN_VPERCENT_COMIS
) 
VALUES 
    (2, 'MALU REPRESENTAÇÃO', 
    '48.825.337/0001-64', 
    'J', 
    'ISENTO', 
    'ATIVO', 
    'comercial@malurepresenta.com.br', 
    2.0
);

INSERT INTO VENDA (
    VDA_CHAVE, 
    VDA_DMOVTO, 
    VDA_VDINHEIRO, 
    VDA_VCARTAO, 
    VDA_VCHEQUE, 
    VDA_VPRAZO, 
    VDA_VOUTROS, 
    VDA_VTOTAL, 
    VDA_VRECEB, 
    VDA_VTROCO, 
    VDA_CODCLI_CLI, 
    VDA_CODVEN_VEN, 
    VDA_VDESC
) 
VALUES 
    (1, '2015-01-23', 0, 0, 0, 0, 0, 10900, 10900, 0, 1, 1, 0);


INSERT INTO VENDA (
    VDA_CHAVE, 
    VDA_DMOVTO, 
    VDA_VDINHEIRO, 
    VDA_VCARTAO, 
    VDA_VCHEQUE, 
    VDA_VPRAZO, 
    VDA_VOUTROS, 
    VDA_VTOTAL, 
    VDA_VRECEB, 
    VDA_VTROCO, 
    VDA_CODCLI_CLI, 
    VDA_CODVEN_VEN, 
    VDA_VDESC
) 
VALUES 
    (2, '2015-02-15', 0, 0, 0, 0, 0, 4800, 5000, 0, 2, 2, 200);

INSERT INTO VENDA_ITENS (
    VDI_CHAVE_VDA, 
    VDI_NSEQUEN, 
    VDI_CODPRO_PROD, 
    VDI_QQUANTI, 
    VDI_VPREUNI, 
    VDI_VALORITEM, 
    VDI_PERCENTDESC, 
    VDI_QTDEDEVOLV, 
    VDI_DESCPROD
) 
VALUES 
    (1, 1, 1, 5, 200, 1000, 0, 0, 'NOBREAK');

INSERT INTO VENDA_ITENS (
    VDI_CHAVE_VDA, 
    VDI_NSEQUEN, 
    VDI_CODPRO_PROD, 
    VDI_QQUANTI, 
    VDI_VPREUNI, 
    VDI_VALORITEM, 
    VDI_PERCENTDESC, 
    VDI_QTDEDEVOLV, 
    VDI_DESCPROD
) 
VALUES 
    (1, 2, 1, 9, 1000, 9000, 0, 0, 'NOTEBOOK');

INSERT INTO VENDA_ITENS (
    VDI_CHAVE_VDA, 
    VDI_NSEQUEN, 
    VDI_CODPRO_PROD, 
    VDI_QQUANTI, 
    VDI_VPREUNI, 
    VDI_VALORITEM, 
    VDI_PERCENTDESC, 
    VDI_QTDEDEVOLV, 
    VDI_DESCPROD
) 
VALUES 
    (1, 3, 1, 100, 9.00, 900, 0, 0, 'SABAO EM PÓ');

INSERT INTO VENDA_ITENS (
    VDI_CHAVE_VDA, 
    VDI_NSEQUEN, 
    VDI_CODPRO_PROD, 
    VDI_QQUANTI, 
    VDI_VPREUNI, 
    VDI_VALORITEM, 
    VDI_PERCENTDESC, 
    VDI_QTDEDEVOLV, 
    VDI_DESCPROD
) 
VALUES 
    (2, 1, 1, 5, 1000, 5000, 0, 0, 'NOTEBOOK');
```

## Adicionar atributos (colunas);
---
```sql
ALTER TABLE PRODUTOS ADD PROD_DTVENCIMENTO DATE; 
ALTER TABLE PRODUTOS ADD PROD_DESCRCOMPLETA VARCHAR(255); 
ALTER TABLE PRODUTOS ADD PROD_PRECOVENDA NUMERIC(18,4); 

ALTER TABLE CLIENTES ADD CLI_FONECONTATO VARCHAR(14); 
ALTER TABLE CLIENTES ADD CLI_CONTATO VARCHAR(30); 
ALTER TABLE CLIENTES ADD CLI_COMPLEMENTOEND VARCHAR(30); 

ALTER TABLE VENDEDOR ADD VEN_FONECONTATO VARCHAR(14); 
ALTER TABLE VENDEDOR ADD VEN_ENDERECO VARCHAR(60); 
ALTER TABLE VENDEDOR ADD VEN_ESTADO VARCHAR(2);

ALTER TABLE VENDA ADD VDA_STATUS CHAR(1); 
ALTER TABLE VENDA ADD VDA_CFOP VARCHAR(7); 
ALTER TABLE VENDA ADD VDA_DTENVIO DATE; 

ALTER TABLE VENDA_ITENS ADD VDI_PERCENTICMS NUMERIC(5,4); 
ALTER TABLE VENDA_ITENS ADD VDI_TOTALICMS NUMERIC(18,4); 
ALTER TABLE VENDA_ITENS ADD VDI_VALORIPI NUMERIC(18,4);
```
