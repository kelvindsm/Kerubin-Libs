>[!Quote] Banco de dados
>- É como um arquivo (ou conjunto deles) organizado e eficiente, criado para armazenar grandes quantidades de informações
>- É como uma biblioteca gigante, porém digital. Invés de livros, há dados: informações sobre clientes de uma empresa ou produtos em um estoque.

# Características de um banco de dados
- Organização: dados estruturados em tabelas, facilita a busca e a recuperação de informações específicas;
- Eficiência: as operações de busca são mais eficientes que em outros métodos de armazenamento;
- Integridade: maior consistência dos dados, evitando redundâncias e informações incorretas;
- Compartilhamento: vários usuários autorizados podem acessar e modificar simultaneamente;
- Segurança: proteção de dados contra acesso não autorizado e perda de dados.
# Função dos banco de dados
- Essenciais para o funcionamento de diversos sistemas como: sistemas de gestão empresarial, sites e aplicativos, redes sociais, sistema de bancos e outros.
## Exemplos de Sistemas de gerenciamento de banco de dados:
- MySQL: popular no desenvolvimento web e aplicações de comércio eletrônico;
- PostgreSQL: conhecido pela sua robustez e flexibilidade, utilizado em diversas aplicações de grande porte; 
- Oracle Database: um dos SGBDs mais poderosos, utilizado em grandes empresas, mantêm suporte às empresas
- Microsoft SQL Server: melhor integração com as ferramentas da Microsoft.
>[!tip] Em resumo
> - o SGBD é uma ferramenta essencial para qualquer sistema que utilize um banco de dados. 
> - Ele simplifica a gestão dos dados, garantindo sua integridade, segurança e disponibilidade.

# SQL: linguagem padrão para interagir com Bancos de Dados
>[!quote] o que é SQL?
>- Significa "Structured Query Language" (Linguagem de Consulta Estruturada), é a linguagem padrão usada para interagir com banco de dados relacionais;
>- Serve como a ponte entre o usuário e e o SGBD, permitindo a execução de diversas operações, como modificação de estruturas e realização de consultas complexas.

## Importância do SQL
- Universalidade: linguagem mais utilizada e compreendida no contexto dos banco de dados;
- Facilidade de uso: sintaxe simples, acessível para pessoas com diferentes níveis de conhecimento técnico;
- Flexibilidade: permite a realização de operações básicas básicas, com inserir, atualizar e excluir dados, até consultas complexas envolvendo múltiplas tabelas, condicionais e agrupamentos
- Padronização: é padrão ANSI, garante compatibilidade entre diferentes SGBDs.
## O que se pode fazer com a SQL
- Criar e modificar estruturas: definir tabelas, colunas, índices e outras estruturas de dados;
- Inserir, atualizar e excluir dados: manipulação de dados no banco de dados;
- Consultar dados: realizar consultas complexas para extrair informações específicas.
- Gerenciar usuários e permissões: controlar o acesso aos dados
- Criar relatórios: gerar relatórios personalizados com base nos dados através de consultas
### Exemplo
```SQL
-- cria a tabela clientes, definindo primary key
CREATE TABLE clientes (
		id INT PRIMARY KEY AUTO_INCREMENT, 
		nome VARCHAR(100), 
		email VARCHAR(100));

-- insere dados na tabela clientes
INSERT INTO clientes (nome, email) VALUES ('João Silva', 'joao@email.com'); 

-- realiza uma consulta geral na tabela
SELECT * FROM clientes; 

-- atualiza o dado inserido na tabela
UPDATE clientes SET email = 'novoemail@email.com' WHERE id = 1; 

-- exclui o dado inserido na tabela
DELETE FROM clientes WHERE id = 1;
```