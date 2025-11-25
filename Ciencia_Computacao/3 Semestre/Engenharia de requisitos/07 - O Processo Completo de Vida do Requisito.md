---
tags:
  - Naoconcluido
---
# Engenharia de Requisitos: O Processo Completo de Vida do Requisito

## 1. O Processo de Produção (Desenvolvimento) de Requisitos

A [[Engenharia de Requisitos]] (ER) abrange a criação e manutenção da documentação de requisitos, sendo um ciclo contínuo de atividades. A falta de um processo de ER leva à prática de "codifica-remenda" e estouros de **prazo e orçamento**.

### Fases do Desenvolvimento de Requisitos
A produção de requisitos se concentra em quatro etapas principais: Elicitação, Análise, Especificação e Validação.
1.  **Elicitação (Descoberta):**
    - **Definição:** É a busca **ativa e proativa** para a descoberta dos requisitos (o que deve ser feito).
    - **Foco:** Investigação e compreensão do contexto, onde o analista deve adotar uma postura proativa.
    - **Timing:** Em projetos ágeis, requisitos podem emergir em diversos momentos (*[[Product Backlog]]*), mas a descoberta tardia gera custos adicionais e retrabalho.
2.  **Análise:**
    - **Objetivo:** Aprofundar o entendimento, buscando **conflitos** (Ex: funcional vs. desempenho) e definindo a **prioridade**.
    - **Atividades:** Decomposição de requisitos de alto nível e definição de **atributos** (volatilidade, risco, impacto na arquitetura).
3.  **Especificação (Documentação):**
    - **Objetivo:** Representar os requisitos de forma que eles possam ser **verificados** e **validados** posteriormente.
    - **Dilema:** A quantidade de especificação depende da **complexidade, criticidade e risco** do produto. Para produtos disruptivos, começa-se com o **MVP** (Minimum Viable Product).
4.  **Validação (Consenso):**
    - **Objetivo:** Garantir a **compreensão correta e comum** dos requisitos, confirmando que o produto irá **satisfazer as necessidades do negócio**.
    - **Métodos:** Revisões, *workshops* de validação, uso de **protótipos funcionais**, e especificação de **[[Casos de Teste]]**.

### 1.1. Fontes de Informação e Stakeholders
As fontes de informação variam conforme o tipo de produto.
- **Fontes Primárias:**
    - **Stakeholders:** Pessoas ou organizações que influenciam (usuários, clientes, patrocinadores).
    - **Documentos:** Leis, regulamentos, normas e padrões.
    - **Sistemas em Operação:** Sistemas legados ou concorrentes que informam novas funcionalidades.
- **Mapeamento de Personas:** Útil para caracterizar um representante genérico de uma classe de usuários e garantir o foco na interface e usabilidade.

## 2. Processo de Gerenciamento de Requisitos (GR)

- **Definição:** Atividade de administrar os requisitos ao longo do tempo, focando em estabelecer e manter o **acordo** entre usuários e a equipe de projeto, à medida que os requisitos se modificam.
- **Volatilidade:** Requisitos são **voláteis** devido a: legislação, erros, e novas necessidades do cliente.
- **[[Rastreabilidade]]:** Foco essencial do GR. Permite traçar a fonte do requisito e sua ligação com os artefatos seguintes (código, teste), facilitando a análise de impacto da mudança.

### Atributos do Requisito (Propriedades para Gerência)
Atributos são propriedades cruciais para priorização e análise de risco:

| Atributo | Foco | Tipos de Valores |
| :--- | :--- | :--- |
| **Estabilidade** | Chance do requisito mudar (Volatilidade) | Alta, Média, Baixa |
| **Prioridade** | Importância para o negócio ou viabilidade técnica | Mandatório, Altamente Desejável, Opcional |
| **Impacto na Arquitetura** | Quão crítico é o requisito na estrutura do sistema | Alto, Médio, Baixo |
| **Risco** | Grau de impacto no projeto caso o requisito não seja implementado | Alto, Médio, Baixo |

### Restrições (Requisitos Não Implementáveis)
- **Definição:** Requisitos sobre os quais a equipe **não tem gestão**, mas que influenciam o *modo* como o produto será implementado.
- **Tipos:**
    - **Tecnológicas:** Ex: Linguagens de programação ou hardware obrigatórios.
    - **Processos de Desenvolvimento:** Ex: Ciclo de vida ou métodos obrigatórios.
    - **Aspectos do Projeto:** Prazos, custos e recursos.