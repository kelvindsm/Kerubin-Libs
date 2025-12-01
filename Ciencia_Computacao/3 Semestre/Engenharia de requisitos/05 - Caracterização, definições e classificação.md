---
tags:
  - Concluido
---
# Caracterização da Engenharia de Requisitos: Definições e Classificação

## Engenharia de Requisitos (ER): Definição e Propósito

A **Engenharia de Requisitos (ER)** é uma sub-área da [[01 - Conceitos fundamentais de engenharia de software|Engenharia de Software (ES)]] que estuda o processo de produção e gerência dos requisitos que o software deverá atender.
- **Estabelecimento:** A ER foi estabelecida como disciplina independente em 1993, com a criação do IEEE International Symposium on Requirements Engineering.
- **Objetivo da ER:** <mark style="background: #FFB8EBA6;">Fornecer métodos, procedimentos e ferramentas que deem suporte adequado às tarefas de produção e gerência dos requisitos do sistema.</mark>

### O Custo da ER Inadequada
Organizações que <mark style="background: #FF5582A6;">trabalham sem um processo formal de ER tendem a identificar requisitos rapidamente e iniciar a codificação</mark> (processo **"codifica-remenda"**).
- **Consequências:** Estes projetos frequentemente estouram o prazo e o orçamento.
- **Retrabalho:** O esforço e o custo do retrabalho são maiores do que os investimentos em ER, que busca desenvolver o projeto certo da primeira vez.

>[!info] Por que a ER é Necessária?
> A ER adequada agrega valor no processo de desenvolvimento e evolução de um sistema:
> - Reduzindo o risco de desenvolver o sistema errado.
> - Melhorando a compreensão do problema.
> - Sendo base para a estimativa de esforço e custo de desenvolvimento.
> - Sendo pré-requisito no teste de sistema.

- **Sintomas de ER Inadequada:** Requisitos não especificados, sem clareza ou incorretos. Isso ocorre devido à pressa para a construção, problemas de comunicação, e o pressuposto de que os requisitos são evidentes por si mesmos.

## Estrutura da Engenharia de Requisitos

A [[01 - Contextualização da engenharia de requisitos|Engenharia de Requisitos]] engloba dois processos principais:
1. **Produção de Requisitos**.
2. **Gerência de Requisitos**.
### 1. Processo de Produção de Requisitos
Visa definir os requisitos do software conforme as necessidades de negócio do cliente.
- **Etapas Sequenciais (Produção):**
1. Elicitação (Identificação das Fontes de Informação).
2. Análise e Negociação (Análise dos Requisitos).
3. Definição dos Requisitos (Documentação).
4. Verificação e Validação (Protótipo do Sistema).
### 2. Processo de Gerência de Requisitos
Visa garantir que os requisitos sejam controlados e mantidos ao longo do ciclo de vida do projeto.
- **Atividades Chave (Gerência):**
	- Controle de Mudança (Gerência).
	- Gerência de Configuração.
	- Rastreabilidade.
	- [[12 - Processo de Gerenciamento de Requisitos|Qualidade de Requisitos]].
## Documento e Tipos de Requisitos
### Definição e Abordagens de Requisitos
- **[[10 - Requisitos de usabilidade|Requisito de Software]]:** "Uma ação a ser executada por um sistema, possuindo características e condições próprias e que devem ser atendidas conforme as necessidades de negócio do usuário".
- **Foco:** Requisitos descrevem **"o que o sistema deve fazer"** e **"o que ele não deve fazer"**, mas não dizem **"como fazer"**. O comportamento deve ser perceptível por um observador externo.
### Tipos de Documentos de Requisitos
A documentação deve ser adaptada ao público-alvo, existindo dois documentos principais:

| Documento                              | Perspectiva   | Características                                                                                                                                              |
| :------------------------------------- | :------------ | :----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Definição dos Requisitos**           | Cliente       | Lista o que o cliente espera; compreensível ao cliente; busca consenso entre cliente e analista.                                                             |
| **Especificação dos Requisitos (ERS)** | Desenvolvedor | Redefine os requisitos em termos técnicos; compreensível para o projetista; envolve modelagem. Inclui termos técnicos, modelo de dados e lógica do processo. |
### Hierarquia de Requisitos (A Pirâmide)
Os requisitos são organizados em níveis, do mais alto (negócio) ao mais baixo (sistema):
1. **Requisitos do Negócio (Necessidades):** Metas de nível mais alto, objetivos ou problemas da organização.
2. **Requisitos de Usuário (Características):** O que os usuários / *stakeholders* querem de sua perspectiva (objetivos, funcionalidades, prioridade, ambiente).
3. **Requisitos de Sistema (Solução):** O que o sistema deve fazer. São a base para o desenvolvimento.
## Classificação Detalhada dos [[03 - Casos de uso e Requisitos Não Funcionais|Requisitos de Software]]
Os [[12 - Processo de Gerenciamento de Requisitos|Requisitos de Software]] são definidos em linguagem estruturada e podem ser classificados em quatro tipos inter-relacionados:
### 1. Requisitos Funcionais (RF)
- Descrevem o **comportamento e as ações** que o sistema ou componente deve ser capaz de executar.
- Inclui requisitos de dados ou de interação com o ambiente.
- **Exemplo:** "O sistema deve permitir ao cliente visualizar os produtos".
### 2. Requisitos de Dados (RD)
- Descrevem os **atributos (dados)** do requisito funcional.
- Podem ser alterados sem modificar a realização do requisito funcional.
- **Exemplo:** "O sistema deve exibir os dados de Nome do Produto, Descrição, Quantidade, Preço e Foto ao visualizar o produto".
### 3. Regras de Negócio / Execução (RN)
- Definem a **condição necessária** para que um requisito funcional (Ação) possa ser executado pelo software.
- Se modificadas, alteram a forma de execução do requisito funcional.
- **Exemplo:** "Quando o cliente realizar o saque então o sistema deve verificar se o saldo é positivo".
### 4. Requisitos de Qualidade / Não Funcionais (RQ)
- Incluem limitações no **produto** (desempenho, confiabilidade, segurança) e limitações no **processo de desenvolvimento** (métodos e padrões).
- Dizem respeito a questões de qualidade que não são cobertas por requisitos funcionais.
#### Características de Qualidade ([[06 - Qualidade de Software e norma ISO 25000|ISO/IEC 25010]])
A norma ISO/IEC 25010 (substituindo a ISO/IEC 9126) define 8 características principais:
- **Adequação Funcional:** (Corresponde à funcionalidade).
- **Eficiência de Desempenho:** Tempo de resposta, utilização de recursos e capacidade.
- **Compatibilidade:** Interoperabilidade.
- **Usabilidade:** Adequação, erros do usuário, estética, proteção, facilidade de uso.
- **Confiabilidade:** Maturidade, disponibilidade, recuperabilidade.
- **Segurança:** Integridade, autenticidade, responsabilidade.
- **Manutenibilidade:** Testabilidade, modificabilidade.
- **Portabilidade:** Adaptabilidade.
---
## Sentenças de Requisitos (Templates)
A forma como os requisitos são escritos é crucial para sua clareza.
### Template para Funcionais e de Dados
- **Estrutura:** O sistema deve + **verbo + objeto | frase verbal** + **complemento de agente | nulo**.
- **Exemplo (RF):** O sistema deve emitir recibo de compra.
- **Exemplo (RD):** O sistema deve cadastrar nome, end, e-mail, tel do cliente.
### Template para Regras de Negócio
- **Estrutura:** Quando ou Se o **agente + verbo + objeto | frase verbal** + então o sistema deve **verbo + objeto | frase verbal**.
- **Exemplo (RN):** Quando o cliente visualizar os produtos (carrinho) o sistema deve permitir alteração de quantidade de itens.
---