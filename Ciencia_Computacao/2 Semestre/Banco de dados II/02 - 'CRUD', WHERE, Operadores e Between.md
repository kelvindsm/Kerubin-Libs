# CREATE

```sql title:"Exemplo: Criando o banco de dados"
-- Criando o banco de dados
CREATE DATABASE db_ibge; 
USE db_ibge; 
```

```sql title:"Exemplo: Criando a tabela tb_regioes"
CREATE TABLE tb_regioes(
	id INT NOT NULL PRIMARY KEY, 
	nome VARCHAR(40) NOT NULL, 
	sigla VARCHAR(2) NOT NULL);
```

```sql title:"Exemplo: Criando a tabela associativa tb_estados"
CREATE TABLE tb_estados(
	id INT NOT NULL PRIMARY KEY,
	nome VARCHAR(60) NOT NULL,
	sigla VARCHAR(2) NOT NULL,
	id_regiao INT DEFAULT NULL,
	FOREIGN KEY (id_regiao) REFERENCES tb_regioes (id) 
);
```

>[!Info] Chave estrangeira
> - FOREING KEY: referencia uma tabela e a chave primária dela.

## INSERT

```sql title:"Exemplo: fazer insert na tabelaa tb_regiao"
insert into tb_regioes(id, nome, sigla) VALUES
	(1, 'Norte', 'N'),
	(2, 'Nordeste', 'NE'),
	(3, 'Sudeste', 'SE'),
	(4, 'Sul', 'S'),
	(5, 'Centro-Oeste', 'CO');
```

```sql title:"Exemplo: fazer insert na tabela tb_estados"
insert into tb_estados(id,nome,sigla,id_regiao) Values
	(11, 'Rondônia', 'RO', 1),
	(12, 'Acre', 'AC', 1),
	(13, 'Amazonas', 'AM', 1),
	(14, 'Roraima', 'RR', 1),
	(15, 'Pará', 'PA', 1),
	(16, 'Amapá', 'AP', 1),
	(17, 'Tocantins', 'TO', 1);
```
# SELECT
- Escolher colunas (campos) da tabela para apresentar na query (consulta)
```SQL
SELECT 
	nome_coluna1, nome_coluna2, ..., nome_colunaN  
FROM 
	nome_tabela; 
	
SELECT * FROM nome_tabela ;
```

### DISTINCT
- Retornar apenas valores distintos (diferentes)
```SQL
SELECT DISTINCT 
	nome_coluna1, nome_coluna2, ..., nome_colunaN 
	FROM nome_tabela;
```

### Where
- Filtra apenas os registros que atendem a uma condição especificada
```SQL destaque:7
SELECT 
	nome_coluna1, nome_coluna2, ..., nome_colunaN  
FROM 
	nome_tabela WHERE condição;

-- Exemplo
SELECT * FROM ClientesWHERE Pais='Mexico';
```

## Operadores
### AND, OR, IN
#### AND
- Exibir um registro se todas as condições separadas por AND forem verdadeiras.
```sql title:"Usando AND" destaque:3
SELECT nome_coluna1, nome_coluna2, ..., nome_colunaN  
	FROM nome_tabela  
WHERE condição1 AND condição2;

-- Exemplo
SELECT * FROM Clientes WHERE Pais='Alemanha' AND Cidade='Berlin';
```
#### OR
- Exibir um registro se alguma das condições separadas por OR for TRUE.
```sql title:"Usando OR" destaque:3
SELECT nome_coluna1, nome_coluna2, ..., nome_colunaN  
	FROM nome_tabela  
WHERE condição1 OR condição2;
```

#### IN
- Especificar vários valores em uma cláusula WHERE
```sql title:"Usando IN"
SELECT nome_coluna1, nome_coluna2, ..., nome_colunaN  
	FROM nome_tabela
WHERE nome_coluna IN (valor1, valor2, ..., valor3);

-- Exemplo: Selecionar todos os clientes cujo país seja Alemanha, França ou Inglaterra.
SELECT * FROM Clientes WHERE Pais IN('Alemanha', 'França', 'Inglaterra');
```

##### NOT - não
- Pode ser associado na cláusula IN - ``{sql icon} NOT IN`` - não dentro.
```sql title:"Selecione o nome dos estados e a sigla, que o id da região não seja 11 e 12*/"
SELECT * FROM tb_estados WHERE id NOT IN(11,12) ORDER BY id;
```
## ORDER BY
- Ordenar a apresentação dos dados
```sql
SELECT nome_coluna1, nome_coluna2, ..., nome_colunaN  FROM nome_tabela ORDER BY nome_coluna ASC | DESC; 

--Exemplo 
SELECT * FROM Clientes ORDER BY Pais;
```

## LIKE
- Condição para seleção de linhas; Filtra linhas (registros) da tabela usando textos
```sql
SELECT nome_coluna1, nome_coluna2, ..., nome_colunaN  
	FROM nome_tabela  
WHERE nome_coluna LIKE padrão;

-- Exemplo: Selecionar todos os clientes cujo nome comece com a letra 'a'.
SELECT * FROM Clientes WHERE ClienteNome LIKE 'a%';
```

```sql title:"Condição para seleção de linhas"
-- Encontra qualquer valor que comece com "a".
WHERE CustomerName LIKE 'a%'

-- Encontra todos os valores que terminam com "a".
WHERE CustomerName LIKE '%a';

-- Encontra quaisquer valores que tenham "ou" em qualquer posição
WHERE CustomerName LIKE '%ou%'

-- Encontra qualquer valor que tenha "r" na segunda posição
WHERE CustomerName LIKE '\_r%';

-- Encontra qualquer valor que comece com "a" e tenha pelo menos 2 caracteres de comprimento
WHERE CustomerName LIKE 'a\_%';

-- Encontra qualquer valor que comece com "a" e tenha pelo menos 3 caracteres de comprimento.
WHERE CustomerName LIKE 'a \_\_%';

-- Encontra qualquer valor que comece com "a" e termine com "o".
WHERE C¾µøacøNa³p LIKE 'a%o'
```

## BETWEEN
- Significa ENTRE - é semelhante ao usar AND para a faixa de valores. Usado para selecionar valores dentro de um determinado intervalo
```sql
SELECT nome_coluna1, nome_coluna2, ..., nome_colunaN 
	FROM nome_tabela 
WHERE nome_coluna BETWEEN valor1 AND valor2;

-- Exemplo: Selecionar produtos com preço fora do intervalo de 10 a 20.
SELECT * FROM Produtos WHERE Preco NOT BETWEEN 10 AND 20;
```

---
# Update
- Atualiza valores armazenados na tabela
```sql title:"Usando UPDATE"
UPDATE nome_tabela 
	SET nome_coluna1 = valor1,
		nome_coluna2 = valor2,
		...,
		nome_colunaN = valorN
WHERE condição

-- Exemplo: Atualizar nome e cidade do usuário com id_usuario 1.
UPDATE Usuarios
	SET nome = 'Ana Maria',
		cidade = 'Sobradinho'
WHERE id_usuario = 1;
```

# DELETE
- Exclui todos os registros. É possível excluir todas as linhas de uma tabela sem afetar sua estrutura.
```sql
DELETE FROM tb_estados WHERE nome='Amazonas';
```

