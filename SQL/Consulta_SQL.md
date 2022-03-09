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
   * [SELECT](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#select)
   * [WHERE](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#where)
   * [LIMIT](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#limit)
   * [ORDER BY](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#order-by)
   * [LIKE](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#like)
   * [AND](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#and)
   * [OR](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#or)
   * [BETWEEN](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#between)
   * [NOT](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#not)
   * [IN](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#in)
   * [DISTINCT](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#distinct)
   * [GROUP BY](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#group-by)
   * [HAVING](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#having)
   * [CASE](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#case)
   * [JOINs](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#joins)
      * [INNER JOIN](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#inner-join)
      * [LEFT JOIN](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#left-join)
      * [RIGHT JOIN](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#right-join)
      * [FULL JOIN](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#full-join)
      * [CROSS JOIN](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#cross-join)
    * [UNION](https://github.com/luisreimberg/Cheat-Sheet/blob/main/SQL/Colinha_SQL.md#union)

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

## **SELECT**

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
## **WHERE**
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

## **LIMIT**

O comando LIMIT limita o número de linhas exibida. Ele sempre deve ficar no final da consulta.
```
USE nome_banco_de_dados;
SELECT lista_de_campos FROM nome_tabela LIMIT numero_linhas;
```
Exemplo:
```
USE sucos;
SELECT CPF, NOME FROM tbcliente LIMIT 5;
```

## **ORDER BY**
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

## **LIKE**
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

## **DISTINCT**
A cláusula DISTINCT elimina as linhas repetidas da consulta.
```
USE nome_banco_de_dados;
SELECT DISTINCT lista_de_campos FROM nome_tabela;
```
Exemplo:
```
SELECT DISTINCT EMBALAGEM, TAMANHO FROM tabela_de_produtos
WHERE SABOR = 'LARANJA'
```
Irá retornar o tipo de embalagem e o tamanho dos sucos de laranja, sem a repetição desses valores. O comando funciona de forma semelhante ao comando unique do Python (Pandas).

## **GROUP BY**
O comando GROUP BY agrupa linhas baseado em semelhanças entre elas. Por exemplo, em uma tabela de vendas no ano eu quero saber o total de receita que obtive por cliente. O comando GROUP BY vai agrupar o total de vendas por cliente. O comando também pode ser utilizado junto com funções de agregação:

FUNÇÃO | DESCRIÇÃO
--------- | ------
SUM | SOMA
MAX | MÁXIMO
MIN | MÍNIMO
AVG | MÉDIA
COUNT | CONTAGEM DE OCORRÊNCIAS

Ao utilizar uma função, logo após é necessário utilizar o comando **AS** (alias) para nomear a coluna agrupada.

Na prática funciona desta forma:
```
USE nome_banco_de_dados;
SELECT coluna_1, SUM(coluna_2) AS nome_coluna_agrupada FROM nome_tabela GROUP BY coluna_1;
```
Irá retornar os valores unicos da coluna_1 e a soma dos valores da coluna_2.

Exemplos:
```
SELECT BAIRRO, SUM(LIMITE_DE_CREDITO) AS LIMITE FROM tabela_de_clientes 
GROUP BY BAIRRO;
```
Retornará todos os bairros, na coluna LIMITE terá o limite de crédito total de cada bairro.
```
SELECT ESTADO, BAIRRO, SUM(LIMITE_DE_CREDITO) AS LIMITE FROM tabela_de_clientes 
WHERE CIDADE = 'RIO DE JANEIRO' 
GROUP BY ESTADO, BAIRRO 
ORDER BY BAIRRO;
```
Aparecerá na primeira coluna o ESTADO, na segunda coluna os BAIRROS ORDENADOS da CIDADE do RIO DE JANEIRO e na terceira coluna com nome LIMITE, o valor com o LIMITE TOTAL de CADA BAIRRO.

## **HAVING**
O HAVING é uma condição (filtro) que se aplica ao resultado de uma agregação.

```
USE nome_banco_de_dados;
SELECT coluna_1, SUM(coluna_2) AS nome_coluna_agrupada FROM nome_tabela GROUP BY coluna_1
HAVING SUM(nome_coluna_agrupada) > 10
```
O comando HAVING vai filtrar o resultado agrupado e será exibido somente os resultados maior que 10.

Exemplos:
```
SELECT ESTADO, SUM(LIMITE_DE_CREDITO) AS SOMA_LIMITE FROM tabela_de_clientes
GROUP BY ESTADO HAVING SUM(LIMITE_DE_CREDITO) > 900000;
```

```
SELECT EMBALAGEM, MAX(PRECO_DE_LISTA) AS MAIOR_PRECO, MIN(PRECO_DE_LISTA) AS MENOR_PRECO FROM tabela_de_produtos
GROUP BY EMBALAGEM HAVING SUM(PRECO_DE_LISTA) <= 80;
```

```
SELECT EMBALAGEM, MAX(PRECO_DE_LISTA) AS MAIOR_PRECO, MIN(PRECO_DE_LISTA) AS MENOR_PRECO FROM tabela_de_produtos
GROUP BY EMBALAGEM HAVING SUM(PRECO_DE_LISTA) <= 80 AND MAX(PRECO_DE_LISTA) >= 5;
```

## **CASE**
Fazemos um teste em um ou mais campos e, dependendo do resultado, teremos um ou outro valor.

```
SELECT X,
CASE
    WHEN Y >= 8 AND Y <= 10 THEN 'OTIMO'
    WHEN Y >= 7 AND Y < 8 THEN 'BOM'
    WHEN Y >= 5 AND Y <= 7 THEN 'MEDIO'
    ELSE 'RUIM'
END
FROM nome_tabela
```
Irá classificar a nota de cliente em ótimo, bom e médio.

Exemplos:
```
SELECT NOME_DO_PRODUTO, PRECO_DE_LISTA,
CASE 
    WHEN PRECO_DE_LISTA >= 12 THEN 'PRODUTO CARO'
    WHEN PRECO_DE_LISTA >= 7 AND PRECO_DE_LISTA < 12 THEN 'PRODUTO EM CONTA'
    ELSE 'PRODUTO BARATO' 
END AS STATUS_PRECO 
FROM tabela_de_produtos;
```
Classificação de produtos em: PRODUTO CARO, PRODUTO EM CONTA E PRODUTO BARATO.

```
SELECT EMBALAGEM,
CASE 
   WHEN PRECO_DE_LISTA >= 12 THEN 'PRODUTO CARO'
   WHEN PRECO_DE_LISTA >= 7 AND PRECO_DE_LISTA < 12 THEN 'PRODUTO EM CONTA'
   ELSE 'PRODUTO BARATO' 
END AS STATUS_PRECO, AVG(PRECO_DE_LISTA) AS PRECO_MEDIO
FROM tabela_de_produtos
GROUP BY EMBALAGEM, 
CASE 
    WHEN PRECO_DE_LISTA >= 12 THEN 'PRODUTO CARO'
    WHEN PRECO_DE_LISTA >= 7 AND PRECO_DE_LISTA < 12 THEN 'PRODUTO EM CONTA'
    ELSE 'PRODUTO BARATO' 
END
ORDER BY EMBALAGEM
```
Esse código foi bem mais complexo. Para facilitar o entendimento, o comando acima vai aparecer a classificação e agrupamento da seguinte forma:

![image](https://user-images.githubusercontent.com/94421216/156492476-c2f7768d-5c62-478e-9fa7-f319aaaa406f.png)

## **JOINs**
Possibilidade de unir uma ou mais tabelas através de campos em comuns. Existem vários tipos de JOINs.

## **INNER JOIN**
Retorna somente quando temos chaves correspondentes
```
SELECT lista_de_campos FROM nome_tabela_A
INNER JOIN nome_tabela_B
ON A.campo_em_comum = B.campo_em_comum
```
Exemplo:
```
SELECT tabela_de_vendedores.BAIRRO,
tabela_de_vendedores.NOME,
tabela_de_clientes.BAIRRO,
tabela_de_clientes.NOME FROM tabela_de_vendedores 
INNER JOIN tabela_de_clientes
ON tabela_de_vendedores.BAIRRO = tabela_de_clientes.BAIRRO
```
Uniu os vendedores e clientes através do bairro.

![image](https://user-images.githubusercontent.com/94421216/156686774-a493e199-0333-4080-832d-32e8f748cf99.png)

## **LEFT JOIN**
Retorna todos da tabela da esquerda e somente os correspondentes da tabela da direita
```
SELECT lista_de_campos FROM nome_tabela_A
LEFT JOIN nome_tabela_B
ON A.campo_em_comum = B.campo_em_comum
```
Exemplo:
```
SELECT tabela_de_vendedores.BAIRRO,
tabela_de_vendedores.NOME, DE_FERIAS,
tabela_de_clientes.BAIRRO,
tabela_de_clientes.NOME FROM tabela_de_vendedores 
LEFT JOIN tabela_de_clientes
ON tabela_de_vendedores.BAIRRO = tabela_de_clientes.BAIRRO
```
Uniu os vendedores e clientes através do bairro, e também retornou um vendedor do bairro Copacabana onde não há clientes no bairro. Ou seja, retornou todos os valores selecionados da **tabela 1** e os valores correspondentes da **tabela 2**. 

![image](https://user-images.githubusercontent.com/94421216/156687546-6aea48cd-f4a6-4c48-b0fe-963e568fe2b7.png)


## **RIGHT JOIN**
Retorna todos da tabela da direita e somente os correspondentes da direita
```
SELECT lista_de_campos FROM nome_tabela_B
RIGHT JOIN nome_tabela_A
ON A.campo_em_comum = B.campo_em_comum
```
Exemplo:
```
SELECT tabela_de_vendedores.BAIRRO,
tabela_de_vendedores.NOME, DE_FERIAS,
tabela_de_clientes.BAIRRO,
tabela_de_clientes.NOME FROM tabela_de_vendedores 
RIGHT JOIN tabela_de_clientes
ON tabela_de_vendedores.BAIRRO = tabela_de_clientes.BAIRRO;
```
Também uniu os vendedores e clientes através do bairro. Porém, note que para vários clientes não existe um vendedor no mesmo bairro. Em outras palavras, retornou todos os valores selecionados da **tabela 2** e os valores correspondentes da **tabela 1**.

![image](https://user-images.githubusercontent.com/94421216/156688764-b5d6bdd3-1f80-4af8-88de-ad62e8ea8587.png)

## **FULL JOIN**
Retorna todos os registros de todas as tabelas
```
SELECT lista_de_campos FROM nome_tabela_B
FULL JOIN nome_tabela_A
ON A.campo_em_comum = B.campo_em_comum
```
Exemplo:
```
SELECT tabela_de_vendedores.BAIRRO,
tabela_de_vendedores.NOME, DE_FERIAS,
tabela_de_clientes.BAIRRO,
tabela_de_clientes.NOME FROM tabela_de_vendedores 
FULL JOIN tabela_de_clientes
ON tabela_de_vendedores.BAIRRO = tabela_de_clientes.BAIRRO;
```
Irá retornar **todos** os registros da **tabela 1** e **tabela 2**. 

Específicamente o MySQL, que é o Software que estou utilizando, não permite o comando FULL JOIN (por mais que o FULL JOIN esteja no padrão ANSI). Neste caso, existe uma forma de simular o FULL JOIN combinado o LEFT e RIGHT JOIN com o UNION.

```
SELECT tabela_de_vendedores.BAIRRO,
tabela_de_vendedores.NOME, DE_FERIAS,
tabela_de_clientes.BAIRRO,
tabela_de_clientes.NOME FROM tabela_de_vendedores 
LEFT JOIN tabela_de_clientes
ON tabela_de_vendedores.BAIRRO = tabela_de_clientes.BAIRRO
UNION
SELECT tabela_de_vendedores.BAIRRO,
tabela_de_vendedores.NOME, DE_FERIAS,
tabela_de_clientes.BAIRRO,
tabela_de_clientes.NOME FROM tabela_de_vendedores 
RIGHT JOIN tabela_de_clientes
ON tabela_de_vendedores.BAIRRO = tabela_de_clientes.BAIRRO;
```
![image](https://user-images.githubusercontent.com/94421216/156693094-d7d213af-4931-46a9-885a-6910d76e945d.png)

## **CROSS JOIN**
Retorna um produto cartesiano das duas tabelas.

```
SELECT lista_de_campos FROM nome_tabela_A, nome_tabela_B
```

🧐 Sim, não precisa escrever CROSS JOIN para executar o comando 🤓

Exemplo:
```
SELECT tabela_de_vendedores.BAIRRO,
tabela_de_vendedores.NOME, DE_FERIAS,
tabela_de_clientes.BAIRRO,
tabela_de_clientes.NOME FROM tabela_de_vendedores, tabela_de_clientes;
```
Irá retornar a análise combinatória da tabela 1 e tabela 2.

![image](https://user-images.githubusercontent.com/94421216/156694280-5632b2b3-8042-4eb5-b68c-00a48dc6064f.png)


## **UNION**
Faz a união de duas ou mais tabelas. Como padrão ele não vai repetir linhas iguais, como o comando DISTINCT. Para que a união respeite as linhas iguais é necessário utilizar o comando UNION ALL.

Observação: O UNION tem uma restrição. Para que ocorra a união as colunas e tipo de colunas das tabelas precisam ser iguais.

```
SELECT lista_de_campos FROM nome_tabela_A
UNION
SELECT lista_de_campos FROM nome_tabela_B
```

Exemplo:
```
SELECT BAIRRO, NOME, 'CLIENTE' AS TIPO FROM tabela_de_clientes
UNION
SELECT BAIRRO, NOME, 'VENDEDOR' AS TIPO FROM tabela_de_vendedores;
```

![image](https://user-images.githubusercontent.com/94421216/156693700-6909786a-2bbc-4f63-a46b-4b73f866932e.png)
