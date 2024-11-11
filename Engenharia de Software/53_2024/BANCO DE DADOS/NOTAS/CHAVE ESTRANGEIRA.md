> Campo que aponta para a chave primária de outra tabela. 
> **Objetivo:** Garantir integridade dos dados referenciais

- Permite o relacionamento entre tabelas
  
```sql
  CREATE TABLE Clientes (
    ClienteID INT PRIMARY KEY, -- Chave primária
    Nome VARCHAR(100),
    Endereco VARCHAR(255)
);
```

```sql
CREATE TABLE Pedidos (
    PedidoID INT PRIMARY KEY, -- Chave primária
    DataPedido DATE,
    ClienteID INT, -- Chave estrangeira
    FOREIGN KEY (ClienteID) REFERENCES Clientes(ClienteID)
);
```