# **SQL Cheat Sheets - Princípais Comandos e Configurações**

![image](https://user-images.githubusercontent.com/94421216/155864598-5f513fe3-7297-4120-ab75-b9a7d35a4d46.png)


# índice
1. [Banco de Dados](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#banco-de-dados)
    * [Criar Banco de Dados](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#criar-banco-de-dados-simples-com-configura%C3%A7%C3%A3o-padr%C3%A3o)
    * [Excluir Banco de Dados](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#excluir-banco-de-dados)
2. [Tabela](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#tabela)
    * [Criar Tabela](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#criar-tabela)
    * [Excluir Tabela](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#excluir-tabela)
    * [Selecionar Tabela](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#selecionar-tabela)
    * [Incluir Registro](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#incluir-registro-em-uma-tabela)
    * [Editar Registro](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#editando-registro-dentro-da-tabela)
    * [Excluir Registro](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#excluindo-registro-dentro-da-tabela)
3. [Configurando colunas](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#configurando-colunas)
    * [Criar Coluna](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#criar-coluna)
    * [Definir Coluna Como Chave Primária](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#alterando-uma-coluna-para-chave-prim%C3%A1ria-n%C3%A3o-permite-registro-duplicado-naquela-coluna)
4. [Seleção]()
   *[]()
   *[]()
   *[]()
   *[]()
   *[]()

# Banco de Dados
## **Criar banco de dados simples (com configuração padrão)**
```diff
 CREATE DATABASE nome_banco_de_dados; 
```

Também é possível criar o banco de dados através do assistente (No MySQL é em: Navigator > botão direito > Create Schema)


## **Excluir banco de dados**
```diff
DROP DATABASE nome_banco_de_dados; 
```
Também é possível excluir o banco de dados através do assistente (No MySQL: clicar com o botão direito no banco de dados > Drop Schema)

# Tabela
## **Criar tabela**
```diff
USE nome_banco_de_dados;
CREATE TABLE nome_tabela (Nome_coluna data_type);
```

Exemplo:
```diff
CREATE TABLE tbCliente
(CPF VARCHAR(11), 
NOME VARCHAR(100),
ENDERECO1 VARCHAR(150),
IDADE SMALLINT,
SEXO VARCHAR(1),
LIMITE_CREDITO FLOAT,
PRIMEIRA_COMPRA BIT(1));
```

A especificação do tipo de dado vai variar de acordo com os dados que serão inseridos na coluna. Para consultar mais detalhes [clique aqui](https://www.w3schools.com/sql/sql_datatypes.asp)


## **Excluir tabela**
```diff
USE nome_banco_de_dados;
DROP TABLE nome_tabela;
```

## **Selecionar tabela**
```diff
USE nome_banco_de_dados;
SELECT * FROM nome_tabela;
```

## **Incluir registro em uma tabela**
```diff
USE nome_banco_de_dados;
INSERT INTO nome_tabela (coluna1, coluna2, coluna3, coluna4)
VALUES (valor1, valor2, valor3, valor4);
```
Para visualizar a inclusão
```diff
SELECT * FROM nome_banco_de_dados;
```
Exemplo:
```diff
USE sucos;
INSERT INTO tbproduto (PRODUTO, NOME, EMBALAGEM, TAMANHO, SABOR, PRECO_LISTA) 
VALUES('1040107', 'Light - 350 ml - Melância', 'Lata', '350 ml','Melância', 4.56);
SELECT * FROM tbproduto;
```

## **Editando registro dentro da tabela**
```diff
USE nome_banco_de_dados;
UPDATE nome_tabela SET nome_coluna = 'novo_valor', nome_coluna2 = 'novo_valor_2'
WHERE coluna_referencial = 'referencia';
```
Exemplo:
```diff
USE sucos;
UPDATE tbproduto SET EMBALAGEM = 'Lata', PRECO_LISTA = 2.46
WHERE PRODUTO = '544931';
```

## **Excluindo registro dentro da tabela**
```diff
USE nome_banco_de_dados;
DELETE FROM nome_tabela WHERE coluna_referencia = 'referencia';
```

Exemplo:
```diff
USE sucos;
DELETE FROM tbproduto WHERE PRODUTO = '1078680';
```
# Colunas

## **Criar coluna**
Para criar uma coluna em uma tabela existente, basta seguir:
```diff
USE nome_banco_de_dados;
ALTER TABLE nome_tabela ADD COLUMN (nome_nova_coluna data_type);
```
## **Alterar coluna para chave primária**
Ao alterar uma coluna para chave primária não será possível adicionar valores iguais na coluna. Normalmente é utilizada para registros únicos: CPF, Código de produto, Registro de entrada, Número de nota fiscal, etc.
```diff
USE nome_banco_de_dados;
ALTER TABLE nome_tabela ADD PRIMARY KEY (nome_coluna);
```
Exemplo:
```
USE sucos;
ALTER TABLE tbproduto ADD PRIMARY KEY (PRODUTO);
```

# Seleção

## **Seleção simples**

O comando SELECT permite recuperar os dados de um objeto do banco de dados, como uma tabela, view e, em alguns casos, uma stored procedure (alguns bancos de dados permitem a criação de procedimentos que retornam valor). A sintaxe mais básica do comando é:
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela;
```
Exemplo:
```
USE sucos;
SELECT CPF, NOME FROM tbcliente;
SELECT * FROM tbclientes;
```
## **Seleção limitando o número de linhas**
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela LIMIT numero_linhas;
```
Exemplo:
```
USE sucos;
SELECT CPF, NOME FROM tbcliente LIMIT 5;
```

## **Seleção com filtro**
O comando WHERE permite ao SQL passar condições de filtragem.
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela
WHERE condição;
```
Exemplo:
```
USE sucos;
SELECT CPF, NOME, IDADE FROM tbcliente
WHERE IDADE = 30;

SELECT CPF, NOME, IDADE FROM tbcliente
WHERE ESTADO = 'SP' OR UF = 'RJ';
```
## **FILTRO DE TEXTO**
Para busca parcial de string, o SELECT fornece o operador LIKE.
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela
WHERE condição LIKE '%TEXTO%';
```
Exemplo:
```
USE sucos;
SELECT CPF, NOME FROM tbcliente
WHERE NOME LIKE '%SILVA%';

SELECT CPF, NOME FROM tbcliente
WHERE NOME LIKE 'MARIA%';
```

Uma observação: em alguns bancos de dados, a máscara de filtro não é representada por %. Consulte a referência do banco para verificar o caractere correto.

Por padrão, a SQL diferencia caixa baixa de caixa alta. Para eliminar essa diferença, utiliza a função UPPER. Veja abaixo:

```
USE sucos;
SELECT CPF, NOME FROM tbcliente
WHERE UPPER(NOME) LIKE 'MARIA %SILVA%'
```

## **ORDENAR**
A ordenação pode ser definida com o comando ORDER BY.
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela
ORDER BY condição;
```

Exemplo:
```
USE sucos;
SELECT CPF, NOME FROM tbcliente
ORDER BY NOME;
```

A utilização da palavra DESC garante uma ordenação invertida
```
USE sucos;
SELECT CPF, NOME FROM tbcliente
ORDER BY ESTADO DESC
