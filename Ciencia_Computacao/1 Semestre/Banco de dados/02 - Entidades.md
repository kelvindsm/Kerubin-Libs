>[!quote] O que é uma entidade?
> - Em modelagem de dados relacional, uma entidade representa um objeto ou conceito do mundo real sobre qual se deseja armazenar informações.
> - É como se fosse uma "coisa" que se deseja acompanhar durante um longo tempo usando banco de dados.

# Como identificar entidades
## 1. Compreenda o sistema
- **Defina o escopo**: Qual parte do sistema você está modelando?
- **Identifique os substantivos**: Quais são os substantivos que representam os objetos principais do sistema?
- **Faça perguntas**: Quais informações você precisa armazenar sobre esses objetos? (campos/colunas)
## 2. Enumere os substantivos
- **Liste todos os substantivos**: Anote todos os substantivos que você identificou na etapa anterior.
- **Elimine duplicidades**: Remova os substantivos que representam a mesma coisa (sinônimos).
## 3. Avalie a relevância
- **Necessidade de informação**: Pergunte-se: "Preciso armazenar informações sobre esse substantivo para atender aos requisitos do sistema?", ou seja, _qual a parte do mundo real que interessa controlar?_
- **Detalhes**: Quais são os detalhes importantes sobre esse substantivo que preciso registrar?
## 4. Abstraia
- **Conceitos**: Agrupe os substantivos que representam o mesmo conceito.
- **Generalização**: Crie entidades mais genéricas para representar grupos de substantivos semelhantes.
### Exemplo de entidades
- Sistema de biblioteca:
- Sistema de e-commerce:
- Sistema de recursos humanos:
## Dicas para identificar entidades
- **Pense em termos substantivos**: Facilita a identificação de entidades
- **Seja específico**: Evite entidades muito genéricas. Aqui vale ressaltar que deve ser específico na busca e depois generalista para agrupar.
- **Considere o contexto**: A identificação das entidades depende do sistema que você está modelando e o interesse do usuário.
- **Utilize diagramas**: Um diagrama de entidade-relacionamento (DER) pode ajudar a visualizar as entidades e seus relacionamentos.
>[!info] Diagrama de Entidade-Relacionamento (DER)
> - Os atributos são representados em um DER dentro dos retângulos que representam as entidades. A chave primária é geralmente sublinhada.
> ![[Pasted image 20250104005349.png]]
### Exemplo Prático
Imagine que você está modelando um sistema para uma loja de roupas. Algumas possíveis entidades seriam: 
- Cliente: Nome, endereço, telefone, e-mail, data de nascimento. 
- Produto: Código, descrição, preço, tamanho, cor, quantidade em estoque.
- Pedido: Número do pedido, data do pedido, cliente, itens do pedido, forma de pagamento.
>[!note] Resumindo
> - A **identificação de entidades é o primeiro passo e é fundamental para a modelagem de dados relacional**. Ao compreender o sistema e identificar os objetos principais, você estará construindo uma base sólida para um banco de dados eficiente e organizado.

# Aprofundando nos Atributos em Modelagem de Dados Relacionais
## Atributos
- **Lembre-se: As entidades representam os objetos sobre os quais queremos armazenar informações;**
- *Os atributos são as características das entidades*, **são as propriedades que descrevem e individualizam cada instância (exemplar) de uma entidade**
### Tipos de atributos
- **Simples**: são indivisíveis, como o nome, a idade ou o CPF.
- **Compostos**: são formados por outros atributos mais simples, como o endereço (rua, número, bairro, cidade, estado). 
- **Multivalorados**: podem assumir múltiplos valores para uma mesma instância, como telefones ou e-mails de um cliente. 
- **Derivados**: não são armazenados diretamente, mas são calculados a partir de outros atributos, como a idade (calculada a partir da data de nascimento).
- **Chave**: identifica de forma única cada instância de uma entidade. A chave primária é a principal e não pode ter valores nulos ou repetidos.
#### Exemplo:
Considere a entidade Cliente. alguns possíveis atributos são:
- Simples: Nome, CPF, Data de Nascimento
- Composto: Endereço (Rua, Número, Bairro, Cidade, Estado)
- Multivalorado: Telefone (pode ter mais de um número) 
- Derivado: Idade (calculada a partir da Data de Nascimento) 
- Chave: CPF (neste caso, o CPF seria a chave primária) 
## Importância dos atributos
- **Definem a entidade**: Os atributos descrevem as características essenciais de uma entidade.
- **Facilitam a busca e a recuperação de dados**: Através dos atributos, podemos filtrar e ordenar os dados de forma eficiente.
- **Garante a integridade dos dados**: A definição correta dos atributos ajuda a evitar a entrada de dados inconsistentes ou inválidos.
### Considerações importantes
- **Atomicidade**: Cada atributo deve representar uma única informação.
- **Domínio**: O conjunto de valores possíveis para um atributo.
- **Nulidade**: Um atributo pode admitir ou não valores nulos, dependendo da sua natureza.
- **Dependência**: Alguns atributos podem depender de outros para existir.

>[!note] Resumo
> - Os atributos são fundamentais para a modelagem de dados, pois definem as características das entidades e permitem que os dados sejam armazenados e manipulados de forma eficiente e precisa. 
> - Ao escolher e definir os atributos, é importante considerar a natureza dos dados, os requisitos do sistema e as regras de negócio.

---
# Exercício Prático de Modelagem de Dados: Uma Biblioteca 
 
## Cenário: 
 Você está trabalhando em um projeto para criar um sistema de gerenciamento para uma biblioteca. O sistema precisa armazenar informações sobre livros, autores, clientes e empréstimos. 
 
## Tarefa: 
1. Identifique as entidades: Quais são os objetos principais sobre os quais você precisa armazenar informações? 
2. Defina os atributos: Quais são as características relevantes de cada entidade? 
 
## Resposta: 
### Entidades Identificadas:  
- Livro: Representa um livro da biblioteca. 
- Autor: Representa um autor de livros. 
- Aluno: Representa um cliente da biblioteca.
- Empréstimo: Representa um empréstimo de um livro a um aluno. 
 
### Atributos: 
- Livro: ISBN (chave primária), título, autor(es), editora, ano de publicação, gênero, quantidade na biblioteca. 
- Autor: ID (chave primária), nome, nacionalidade. 
- Aluno: CPF (chave primária), nome, endereço, telefone, e-mail. 
- Empréstimo: Número do empréstimo (chave primária), data de empréstimo, data de devolução prevista, livro (chave estrangeira para a tabela Livro - iremos detalhar no futuro), cliente (chave estrangeira para a tabela Cliente - iremos detalhar no futuro). 
 
### Explicação: 
- Chaves primárias: São os atributos que identificam de forma única cada registro em uma tabela (ISBN para Livro, ID para Autor, CPF para Aluno, Número do empréstimo para Empréstimo). 
### Observações: 
- Este é um exemplo simplificado. Dependendo da complexidade da livraria, você pode precisar adicionar mais entidades e atributos. 
- A escolha dos atributos depende das informações que você deseja armazenar e das funcionalidades que o sistema deve oferecer.
## No MySQL Workbench

1. Criação de um novo banco de dados para a livraria e entrar no banco de dados:
```mysql title:"Criando o banco de dados"
DROP DATABASE IF EXISTS livraria;

CREATE DATABASE livraria;

USE livraria;
```

2. Criação da tabela para entidade livro:
```mysql title:"Criando a tabela para entidade livro"
DROP TABLE IF EXISTS livro;

CREATE TABLE livro(
	isbn CHAR(17) NOT NULL PRIMARY KEY,
	titulo VARCHAR(100) NOT NULL,
	editora VARCHAR(50) NOT NULL,
	ano_publicacao YEAR NOT NULL,
	genero ENUM('Narrativo', 'Lírico', 'Dramático', 'Histórico', 'Outros') NOT NULL,
	qtd_estoque INT NOT NULL);
```

3. Para inserir três livros para testes iniciais
```mysql title:"Inserindo livros para testar o banco de dados"
INSERT INTO livro VALUES
(978-85-123-4567-8', 'Bancos de Dados Relacionais: Uma Abordagen Prática', 'Editora Ática', 2023, "Outros", 4), 
('978-85-987-6543-2', 'SQL para Todos: Dominando a Linguagem de Consulta de Dados', 'Editora Saraiva', 2022, 'Outros', 5), 
('978-85-321-6549-8', 'Modelagem de Dados: Do Conceito à Implementação', 'Editora Pearson', 2021, 'Outros', 7);
```

4. Execução de algumas consultas aos dados:
```mysql title:"Consultas ao banco de dados"
SELECT FROM livro;

SELECT * FROM livro WHERE isbn = '978-85-987-6543-2';

SELECT titulo, UPPER(editora) as maiusculo, CONCAT(qtd_estoque,
em estoque') as estoque FROM livro;
```
---