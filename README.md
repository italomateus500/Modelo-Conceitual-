-- TABELA CLIENTE
CREATE TABLE Cliente (
    ID_Cliente INT PRIMARY KEY,
    Nome VARCHAR(100),
    CPF VARCHAR(14),
    Endereco VARCHAR(150)
);

-- TABELA PEDIDO
CREATE TABLE Pedido (
    ID_Pedido INT PRIMARY KEY,
    Data DATE,
    Valor_Total DECIMAL(10,2),
    ID_Cliente INT,
    FOREIGN KEY (ID_Cliente) REFERENCES Cliente(ID_Cliente)
);

-- TABELA PRODUTO
CREATE TABLE Produto (
    ID_Produto INT PRIMARY KEY,
    Nome VARCHAR(100),
    Preco DECIMAL(10,2)
);

-- RELACIONAMENTO CONTÉM (Pedido e Produto)
CREATE TABLE Pedido_Produto (
    ID_Pedido INT,
    ID_Produto INT,
    Quantidade INT,
    PRIMARY KEY (ID_Pedido, ID_Produto),
    FOREIGN KEY (ID_Pedido) REFERENCES Pedido(ID_Pedido),
    FOREIGN KEY (ID_Produto) REFERENCES Produto(ID_Produto)
);



![image](https://github.com/user-attachments/assets/2a2957d7-d029-46a4-ad04-20032b3f7dd7)

