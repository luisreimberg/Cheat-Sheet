# **SQL CHEAT SHEETS - PRINCIPAIS COMANDOS**

A ideia de criar este repositório surgiu durante meus estudos de SQL pela plataforma da [Alura](https://www.alura.com.br/). O objetivo foi sintetizar os principais comandos SQL e consultá-los sempre que for necessário. E claro, também ajudar as pessoas que estão aprendendo sobre SQL, assim como eu! 😁

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
3. [Colunas](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#configurando-colunas)
    * [Criar Coluna](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#criar-coluna)
    * [Definir Coluna Como Chave Primária](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#alterando-uma-coluna-para-chave-prim%C3%A1ria-n%C3%A3o-permite-registro-duplicado-naquela-coluna)
4. [Seleção](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#sele%C3%A7%C3%A3o)
   * [Seleção Simples](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#sele%C3%A7%C3%A3o-simples)
   * [Limitando a seleção](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#sele%C3%A7%C3%A3o-limitando-o-n%C3%BAmero-de-linhas)
   * [Filtro](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#sele%C3%A7%C3%A3o-com-filtro)
   * [Filtro de Texto](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#filtro-de-texto)
   * [Ordenação](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#ordenar)
   * [AND]
   * [OR]
   * [BETWEEN]
   * [NOT]
   * [IN]

# Créditos
Agradecimentos especiais a [Alura](alura.com.br) por organizar e facilitar o aprendizado de milhares de estudantes, ao [Professor Victorino](https://www.linkedin.com/in/victorino-vila-1a160/) por ministrar as aulas de forma didática, objetiva e com ótimos exemplos e ao [Site DEVMidia](https://www.devmedia.com.br/sql-select-guia-para-iniciantes/29530) que me ajudou com alguns filtros SQL que estão neste guia. Obrigado!

# BANCO DE DADOS
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

# TABELA
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

A especificação do tipo de dado vai variar de acordo com os dados que serão inseridos na coluna. Para consultar mais detalhes [clique aqui](https://www.w3schools.com/sql/sql_datatypes.asp).


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

## **Editar registro dentro da tabela**
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

## **Excluir registro dentro da tabela**
```diff
USE nome_banco_de_dados;
DELETE FROM nome_tabela WHERE coluna_referencia = 'referencia';
```

Exemplo:
```diff
USE sucos;
DELETE FROM tbproduto WHERE PRODUTO = '1078680';
```
# COLUNAS

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

# SELEÇÃO

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
```

## **AND**
O operador AND (E) mostra um registro se todas as condições forem verdadeiras.
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela 
WHERE A AND B;
```
Exemplo:
```
USE sucos;
SELECT * FROM tabela_de_produtos 
WHERE SABOR = 'Manga' AND TAMANHO = '470 ml'
```
Irá retornar os sucos de sabor manga que o tamanho seja de 470 ml.

## **OR**
O operador OR (OU) mostra um registro se pelo menos uma das condições for verdadeira.
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela 
WHERE A OR B;
```
Exemplo:
```
SELECT * FROM tabela_de_produtos WHERE SABOR = 'Manga'
OR TAMANHO = '470 ml';
```
Irá retornar os sucos com o sabor manga e os demais sucos com tamanho de 470 ml.

## **BETWEEN**
O comando BETWEEN é utilizado para selecionar um determinado range de registros em uma tabela.
```
USE nome_banco_de_dados;
SELECT campos FROM tabela WHERE campo BETWEEN 0 AND 1;
```
Exemplo:
```
SELECT * FROM tabela_de_produtos WHERE PRECO_DE_LISTA BETWEEN 19.00 AND 25.80;
```
Irá retornar os produtos com valores entre 19.00 e 25.80

## **NOT**
o operador NOT inverte o estado lógico.
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela 
WHERE A OR B;
```
Exemplo:
```
SELECT * FROM tabela_de_produtos WHERE NOT (SABOR = 'Manga'
AND TAMANHO = '470 ml');
```
Irá retornar os sucos que o sabor não é manga com tamanho de 470 ml.

## **IN**
O operador IN é utilizado quando desejamos consultar uma tabela, filtrando o valor de um de seus campos a partir de uma lista e possibilidades. Enquanto o operador de comparação de igualdade (=) avalia se os dois valores são iguais, o IN permite verificar se o valor de um campo se encontra em uma lista. Sua sintaxe é a seguinte:
```
USE nome_banco_de_dados;
SELECT campos FROM tabela WHERE campo IN (valor1, valor2, valor3);
```
Exemplo:
```
SELECT * FROM tabela_de_clientes WHERE CIDADE IN ('Rio de Janeiro', 'São Paulo')
AND IDADE >= 20;
```
Irá retornar os cliente que estão na cidade Rio de Janeiro e São Paulo e com idade maior ou igual a 20 anos.
