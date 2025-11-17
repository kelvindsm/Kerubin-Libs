# Principais funções agregadoras
### COUNT()
- Conta o número de registros.
```sql title:"Exemplo"
SELECT COUNT(*) AS total_empregados FROM tb_empregado;
```

- <mark style="background: #FFB8EBA6;">O COUNT( * ) é uma função agregadora que conta o número total de linhas em uma tabela, independentemente de haver valores NULL</mark> em alguma coluna. O asterisco ( * ) significa que estamos contando todas as linhas, sem considerar colunas específicas.
### SUM()
- Soma os valores de uma coluna.
```sql title:"Exemplo"
SELECT SUM(salario) FROM tb_cargo;
```
### AVG()
- Calcula a média dos valores.
```sql title:"Exemplo"
SELECT AVG(salario) AS salario_médio FROM tb_cargo;

-- Para arredondar o valor em 2 casas decimais
SELECT ROUND(AVG(salario), 2) AS salario_medio FROM tb_cargo;
```
### MAX()
- Retorna o valor máximo.
```sql title:"Exemplo"
SELECT MAX(salario) AS maior_salario FROM tb_cargo;
```
### MIN()
- Retorna o valor mínimo
```sql title:"Exemplo"
SELECT MIN(salario) AS menor_salario FROM tb_cargo;
```

## GROUP BY
- <mark style="background: #FF5582A6;">As funções agregadoras podem ser usadas com GROUP BY para agrupar os dados antes da agregação.</mark> Por exemplo, para calcular o número de empregados por departamento:

```sql title:"Exemplo: Usando GROUP BY para retornar o total de empregados em cada departamento"
SELECT
	d.nm_departamento, COUNT(e.matricula) AS total_empregados
FROM
	tb_empregado e
		JOIN
	tb_departamento d ON e.fk_departamento = d.id_departamento
GROUP BY d.nm_departamento;
```

```sql title:"Exemplo: média salarial por departamento"
SELECT
	d.nm_departamento, ROUND(AVG(c.salario), 2) AS salario_medio
FROM
	tb_empregado e
		JOIN
	tb_cargo c ON e.fk_cargo = c.id_cargo
		JOIN
	tb_departamento d ON e.fk_departamento = d.id_departamento
GROUP BY d.nm_departamento;
```

![[Pasted image 20250318151904.png|200]]

## HAVING
- Diferente do WHERE, que filtra linhas antes da agregação, <mark style="background: #FFB86CA6;">HAVING filtra os resultados já agrupados.</mark>

![[Pasted image 20250318152034.png]]

```sql title:"Exemplo: mostrar apenas departamentos onde a média salarial seja maior que 5.000"
SELECT
	d.nm_departamento, ROUND(AVG(c.salario), 2) AS salario_medio
FROM
	tb_empregado e
		JOIN
	tb_cargo c ON e.fk_cargo = c.id_cargo
		JOIN
	tb_departamento d ON e.fk_departamento = d.id_departamento
GROUP BY d.nm_departamento
HAVING AVG(c.salario) > 5000;
```

>[!note] Sobre o exemplo acima
> - <mark style="background: #FFB86CA6;">O AVG(c.salario) é calculado primeiro para cada departamento,</mark> **considerando todos os salários** (sem filtrar os salários abaixo de 5.000).
> - Depois que a média é calculada, <mark style="background: #FFB86CA6;">o HAVING remove os departamentos cuja média salarial seja menor ou igual a 5.000. </mark>
>
> - **Resultado: A média é calculada com todos os salários e depois somente os departamentos com média acima de 5.000 são mantidos.**
> - ![[Pasted image 20250318152717.png|250]]

- Para filtrar funcionários com salário acima de 5.000 anates da agregação, sua-se WHERE
```SQL title:"Exemplo"
SELECT
	d.nm_departamento, ROUND(AVG(c.salario), 2) AS salario_medio
FROM
	tb_empregado e
		JOIN
	tb_cargo c ON e.fk_cargo = c.id_cargo
		JOIN
	tb_departamento d ON e.fk_departamento = d.id_departamento
WHERE
	c.salario > 5000
GROUP BY d.nm_departamento;
```

>[!note] Sobre o exemplo acima
>- <mark style="background: #FFB86CA6;">O WHERE filtra os dados antes da agregação, ou seja, apenas funcionários com salário acima de 5.000 são considerados antes de calcular a média.</mark>
>- Isso significa que **os salários abaixo de 5.000 são excluídos antes da média ser calculada.**
>- O AVG(c.salario) será calculado somente sobre os salários já filtrados. Resultado: **A média salarial exclui todos os funcionários que ganham 5.000 ou menos.**

### Usando WHERE e HAVING ao mesmo tempo
- Isso acontece quando precisamos filtrar os dados antes da agregação (WHERE) e também filtrar os grupos resultantes.

>[!example] Exemplo usando db_company
>- Vamos supor que queremos analisar os departamentos, mas queremos excluir estagiários do cálculo antes da agregação e depois exibir apenas os departamentos onde o salário médio é maior que R$ 6.000,00.

```sql title:"Solução"
SELECT
	d.nm_departamento, ROUND(AVG(c.salario), 2) AS salario_medio
FROM
	tb_empregado e
		JOIN
	tb_cargo c ON e.fk_cargo = c.id_cargo
		JOIN
	tb_departamento d ON e.fk_departamento = d.id_departamento
WHERE
	c.nm_cargo <> 'Estagiário'
GROUP BY d.nm_departamento
HAVING AVG(c.salario) > 6000
```

- WHERE: <mark style="background: #FFB86CA6;">filtra registros individuais antes da agregação</mark> (removendo os estagiários)
- HAVING: <mark style="background: #FFB86CA6;">Filtra os grupos depois da agregação</mark> (removemos departamentos com média salarial menor que R$ 6.000,00).

# Subqueries (subconsultas)
>[!quote] Definição
>- **Uma subquery (subconsulta) é uma consulta SQL aninhada dentro de outra consulta.** <mark style="background: #FFF3A3A6;">Ela é usada para obter um conjunto de dados que será processado pela consulta principal.</mark>
>
>>[!note] As subqueries permitem realizar operações mais avançadas, como: 
>>- Filtragem de dados baseada em cálculos;
>>- Comparações com agregações (AVG(), SUM(), MAX(), etc.);
>>- Retorno de valores específicos para serem usados em WHERE, SELECT ou FROM.

## Tipos de subqueries
### Subquery no SELECT (Recuperando Dados de Outra Tabela)
- Usada para trazer informações complementares de outra tabela.
```SQL title:"Mostrar o nome do empregado e seu salário atual, sem usar JOIN"
SELECT e.nome, 
	(SELECT c.salario
	FROM tb_cargo c 
	WHERE c.id_cargo = e.fk_cargo) AS salario 
FROM tb_empregado e;
```

>[!note] Explicação
>
>>Consulta principal (SELECT externo)
>- Busca os nomes dos empregados da tabela tb_empregado (e.nome);
>- Para cada empregado, precisa buscar o salário correspondente.
>
>>Subquery (SELECT interno)
>- **Para cada linha da consulta principal, a subquery é executada.**
>- <mark style="background: #FFF3A3A6;">A subquery busca o salário na tabela tb_cargo (c.salario), onde o cargo do empregado (e.fk_cargo) corresponde ao ID do cargo (c.id_cargo).</mark>
>- Isso significa que o salário retornado depende do cargo do empregado.

### Subquery no WHERE (Filtragem de Dados)
- Usada para buscar um valor específico dentro de outra consulta.
```sql title:"Encontrar todos os empregados que ganham mais do que a média salarial da empresa"
SELECT nome, fk_cargo, fk_departamento
	FROM tb_empregado
WHERE fk_cargo IN(
	SELECT id_cargo
		FROM tb_cargo
	WHERE salario > (SELECT AVG(salario) FROM tb_cargo)
);
```

>[!note] Explicação
>- A subquery **(SELECT AVG(salario) FROM tb_cargo) calcula a média dos salários**;
>- A subquery **(SELECT id_cargo FROM tb_cargo WHERE salario > média) retorna os cargos acima da média.**
>- <mark style="background: #FFF3A3A6;">A consulta principal retorna os empregados que pertencem a esses cargos.</mark>

### Vantagens e desvantagens das Subqueries
>[!check] Vantagens
>- Facilitam consultas complexas sem a necessidade de várias tabelas na consulta principal;
>- Substituem JOINs em alguns casos, tornando o código mais legível;
>- Permitem usar funções agregadoras (AVG(), SUM(), etc.) dentro de filtros.

>[!fail] Desvantagens
>- Podem ser menos eficientes que JOINs, pois algumas subqueries são executadas repetidamente;
>- Dificultam a otimização em bancos de dados grandes, podendo aumentar o tempo de execução; 
>- Em algumas situações, um JOIN é mais rápido e deve ser preferido.