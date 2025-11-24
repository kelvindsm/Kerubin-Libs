---
tags:
  - Naoconcluido
---
# Engenharia de Requisitos: Caracterização, Definições e Classificação

## 1. Caracterização da Engenharia de Requisitos (ER)

- A **ER** é uma sub-área da [[Engenharia de Software]] que estuda o processo de produção e gerência dos requisitos que o software deverá atender.
- O objetivo da ER é fornecer **métodos, procedimentos e ferramentas** para dar suporte adequado às tarefas de produção e gerência de requisitos do sistema.
- Foi estabelecida como disciplina independente em 1993, quando da criação do IEEE International Symposyum on Requirements Engineering (RE'93).
- A ER busca desenvolver o projeto certo da primeira vez, pois o **custo do retrabalho** é maior do que o investimento em ER.
    - A prática de "codifica-remenda" (identificar requisitos rapidamente e iniciar a codificação) frequentemente causa estouro de prazo e orçamento.

>[!info] Processos de ER (IEEE, 1998)
> São processos de aquisição, refinamento e verificação das necessidades dos usuários, por meio de técnicas sistemáticas e repetíveis, para assegurar que os requisitos sejam **completos, consistentes, relevantes** e que atendam às necessidades do cliente.

### Princípios Fundamentais da ER
1.  **Orientação para o valor:** Requisitos são um meio para atingir um fim, não o fim em si.
2.  **Stakeholders:** A ER busca a satisfação dos desejos e necessidades das partes interessadas.
3.  **Entendimento Compartilhado:** O desenvolvimento de sistemas é impossível sem uma base comum de entendimento.
4.  **Evolução:** A mudança de requisitos não é um acidente, mas o caso normal.
5.  **Validação:** Requisitos não validados são inúteis.

## 2. Processos da Engenharia de Requisitos

A Engenharia de Requisitos engloba dois processos principais:

### Processo I: Produção de Requisitos
Visa definir os requisitos do software conforme as necessidades de negócio.
- **Etapas:**
    1.  **Elicitação:** Identificação das fontes de informação. Foca em entender o domínio do problema e da solução.
    2.  **Análise e Negociação:** Análise dos requisitos para identificá-los e resolvê-los.
    3.  **Definição (Documentação):** Documentação dos requisitos de forma clara e objetiva.
    4.  **Verificação e Validação:** Verificação com o cliente (pode envolver a [[Prototipação]]).

### Processo II: Gerência de Requisitos
Visa garantir que os requisitos sejam gerenciados durante todo o ciclo de vida:
- **Atividades:**
    - Controle de Mudança.
    - Gerência de Configuração.
    - [[Rastreabilidade]].
    - Qualidade de Requisitos.

## 3. Definições e Classificação dos Requisitos

### Requisito de Software
- **Conceito:** Ação a ser executada por um sistema, com características e condições próprias que devem ser atendidas conforme as necessidades de negócio do usuário.
- **Foco:** Descreve **"o que"** o sistema deve ou não deve fazer, sem dizer **"como"** fazer.
- **Forma Correta de Requisito:** Deve ser expresso em termos do comportamento do sistema, perceptível por um observador externo.
    - *Exemplo Correto:* "O sistema deve exibir os clientes com pagamento em atraso."

### Hierarquia e Tipos de Requisitos
Os requisitos são organizados em uma pirâmide hierárquica (Domínio do Problema $\rightarrow$ Domínio da Solução):
1.  **Requisitos do Negócio:** Metas, objetivos, premissas, restrições e custos.
2.  **Requisitos de Usuário:** Objetivos, funcionalidades e prioridade da perspectiva do usuário.
3.  **Requisitos do Sistema:** Detalhamento da solução (Ações, Dados, Regras de Negócio, Qualidade, Interface).

### Classificação do requisito da solução
- **Requisitos Funcionais (RF):** Dizem respeito a um resultado ou comportamento fornecido por uma função do sistema.
    - *Ex.:* O sistema deve permitir realizar saque.
- **Requisitos de Qualidade (RQ) (Não Funcionais):** Questões de qualidade não cobertas pelos RFs (desempenho, segurança, confiabilidade).
- **Restrições:** Requisitos que limitam o espaço da solução além do necessário.

### Tipos Específicos de Requisitos do Software
- **Requisitos de Dados (RD):** Descrevem os atributos (dados) do requisito funcional (podem ser alterados sem modificar a execução do RF).
    - *Ex.:* O sistema deve exibir os dados de Nome do Produto, Descrição, Quantidade, Preço e Foto ao visualizar o produto.
- **Regras de Negócio / Execução (RN):** Define a condição necessária para que um requisito funcional seja executado (se modificadas, alteram a execução do RF).
    - *Ex.:* Quando o cliente realizar o saque, então o sistema deve verificar se o saldo é positivo.
### Sentenças de Requisitos (Sintaxe) 
- **RF (Sentença Funcional):** O sistema deve + verbo + objeto | frase verbal) + complemento de agente | nulo).
- **RN (Sentença Condicional):** Quando ou Se o (agente + verbo + objeto) + então o sistema deve (verbo + objeto | frase verbal).
---