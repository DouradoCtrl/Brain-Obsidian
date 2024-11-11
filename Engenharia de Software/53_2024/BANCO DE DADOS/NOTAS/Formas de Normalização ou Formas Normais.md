Formas normais são regras específicas aplicadas ao design de bancos de dados relacionais. Evita redundâncias ou anomalias.

 >Há algumas regras para normalização do banco de dados. Cada regra é chamada de "forma normal". Se a primeira regra for observada, diz-se que o banco de dados está na "primeira forma normal ". Se as três primeiras regras forem observadas, o banco de dados será considerado na "terceira forma normal". Embora outros níveis de normalização sejam possíveis, a terceira forma normal é considerada o nível mais alto necessário para a maioria dos aplicativos. (MICROSOFT, 2023)

Se somente se, a primeira regra for observada -> Classifica como 1NF
Se somente se, as duas primeiras forem observadas -> Classifica como 2NF
Se somente se, as três primeiras regras forem observadas -> Classifica com 3NF

## Primeira Forma Normal (1NF)
---
**Chat GPT Explicação:** 
- Cada coluna deve conter valores não divisíveis (atômicos), cada registro deve ser único.
- Eliminar grupos de repetição, garantindo que cada cédula da tabela tenha um único valor

**Microsoft Explicação:** 
- Eliminar grupos repetidos em **tabelas individuais**
- Crie uma tabelas separada para cada conjunto de dados relacionados.
- Identifique cada conjunto de dados relacionados com uma chave primária

```sql
--- Exemplo fornedores (Microsoft, 2023)
CREATE TABLE Itens (
    ItemID INT PRIMARY KEY,
    NomeItem VARCHAR(100)
);

CREATE TABLE Fornecedores (
    FornecedorID INT PRIMARY KEY,
    NomeFornecedor VARCHAR(100)
);
```
## Segunda Forma Normal (2NF)
---
**Chat GPT Explicação:** 
- A tabela deve estar na 1NF e todos os atributos não-chave devem depender totalmente da chave primária.
- Eliminar dependências parciais, onde um atributo não-chave depende apenas de parte da chave primária composta.

**Microsoft Explicação:** 
- Crie tabelas separadas para conjunto de valores que se aplicam a vários registros
- Relacione essas tabelas com uma chave estrangeira
- Os registros devem depender somente da chave primária de uma tabela

> Exemplo: Considere o endereço de um cliente em um sistema de contabilidade. O endereço é necessário para a tabela Clientes, mas também para as tabelas Pedidos, Envio, Faturas, Contas a Receber e Coleções. Em vez de armazenar o endereço do cliente como uma entrada separada em cada uma dessas tabelas, armazene-o em um só lugar, na tabela Clientes ou em uma tabela Endereços separada.

```sql
--- Exemplo 1 fornedores (Microsoft, 2023)
CREATE TABLE InventarioFornecedores (
    ItemID INT,
    FornecedorID INT,
    PreçoFornecedor DECIMAL(10, 2),
    PRIMARY KEY (ItemID, FornecedorID),
    FOREIGN KEY (ItemID) REFERENCES Itens(ItemID),
    FOREIGN KEY (FornecedorID) REFERENCES Fornecedores(FornecedorID)
);

-- Exemplo 2 Sistema de contabilidade (Microsoft, 2023)
CREATE TABLE Clientes (
    ClienteID INT PRIMARY KEY,
    NomeCliente VARCHAR(100),
    EndereçoID INT,  -- Endereço principal do cliente
    FOREIGN KEY (EndereçoID) REFERENCES Endereços(EndereçoID)
);

CREATE TABLE Endereços (
    EndereçoID INT PRIMARY KEY,
    ClienteID INT,
    Endereço VARCHAR(255),
    Cidade VARCHAR(100),
    Estado VARCHAR(50),
    CEP VARCHAR(20),
    FOREIGN KEY (ClienteID) REFERENCES Clientes(ClienteID)
);

CREATE TABLE Pedidos (
    PedidoID INT PRIMARY KEY,
    ClienteID INT,
    EndereçoID INT,  -- Endereço onde o pedido será enviado
    DataPedido DATE,
    FOREIGN KEY (ClienteID) REFERENCES Clientes(ClienteID),
    FOREIGN KEY (EndereçoID) REFERENCES Endereços(EndereçoID)
);

CREATE TABLE Faturas (
    FaturaID INT PRIMARY KEY,
    PedidoID INT,
    EndereçoID INT,  -- Endereço para cobrança
    DataFatura DATE,
    ValorTotal DECIMAL(10, 2),
    FOREIGN KEY (PedidoID) REFERENCES Pedidos(PedidoID),
    FOREIGN KEY (EndereçoID) REFERENCES Endereços(EndereçoID)
);

CREATE TABLE ContasReceber (
    ContaID INT PRIMARY KEY,
    FaturaID INT,
    EndereçoID INT,  -- Endereço associado à cobrança
    DataVencimento DATE,
    Valor DECIMAL(10, 2),
    FOREIGN KEY (FaturaID) REFERENCES Faturas(FaturaID),
    FOREIGN KEY (EndereçoID) REFERENCES Endereços(EndereçoID)
);

CREATE TABLE Envios (
    EnvioID INT PRIMARY KEY,
    PedidoID INT,
    EndereçoID INT,  -- Endereço de envio
    DataEnvio DATE,
    FOREIGN KEY (PedidoID) REFERENCES Pedidos(PedidoID),
    FOREIGN KEY (EndereçoID) REFERENCES Endereços(EndereçoID)
);

CREATE TABLE Coleções (
    ColeçãoID INT PRIMARY KEY,
    ClienteID INT,
    EndereçoID INT,  -- Endereço associado à coleção
    DataColeção DATE,
    FOREIGN KEY (ClienteID) REFERENCES Clientes(ClienteID),
    FOREIGN KEY (EndereçoID) REFERENCES Endereços(EndereçoID)
);

```
## Terceira Forma Normal (3NF)
---
 **Chat GPT Explicação:** 
 - A tabela deve estar na 2NF e não deve haver dependências transitivas entre atributos não-chave.
 - Garantir que todos os atributos não-chave dependam diretamente da chave primária e não de outros atributos não-chave

**Microsoft Explicação:** 
- Elimine os campos que não dependem da chave primária
- Verifique se não existe um [[dependência transitiva]]

```sql
-- Tabela de Livros
CREATE TABLE Books (
    BookID INT PRIMARY KEY,
    Title VARCHAR(255),
    PublicationYear INT
);

-- Tabela de Autores
CREATE TABLE Authors (
    AuthorID INT PRIMARY KEY,
    AuthorName VARCHAR(255)
);

-- Tabela de Edições
CREATE TABLE Editions (
    EditionID INT PRIMARY KEY,
    BookID INT,
    Edition VARCHAR(255),
    FOREIGN KEY (BookID) REFERENCES Books(BookID)
);

-- Tabela de Relação entre Livros e Autores
CREATE TABLE BookAuthors (
    BookID INT,
    AuthorID INT,
    PRIMARY KEY (BookID, AuthorID),
    FOREIGN KEY (BookID) REFERENCES Books(BookID),
    FOREIGN KEY (AuthorID) REFERENCES Authors(AuthorID)
);
```