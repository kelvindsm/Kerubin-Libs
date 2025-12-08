---
tags:
  - Concluido
---
# Engenharia de Requisitos: Visão Geral e Contextualização na Engenharia de Software
## Introdução e Contexto
A **Engenharia de Requisitos (ER)** é uma disciplina fundamental para a [[Engenharia de Software]]. Seu papel principal é servir como ponte, convertendo as necessidades do cliente em **requisitos de software**.
### O Papel do Analista/Engenheiro de Requisitos
O **Analista/Engenheiro de Requisitos** tem o papel crucial de **transformar necessidades em solução de software**. Ele atua como intermediário no fluxo de desenvolvimento:
>[!info] Fluxo do Processo
> - O **Cliente** passa suas necessidades.
> - O **Analista/Engenheiro de Requisitos** atende às necessidades e converte as necessidades em *Requisitos de Software*.
> - O **Desenvolvedor** converte os requisitos de software em **Código**, usando uma [[Linguagem de Programação]].
> - O software é entregue, atendendo às necessidades.

- O processo de **Análise do Problema** e elaboração de uma **Proposta de Solução** é fundamental, culminando no **Software para Automação do Processo**. O software essencialmente **automatiza as tarefas de um processo de negócio**.
### Comunicação: Negócio (Problema) vs. Software (Solução)
O processo de comunicação é essencial para ligar o lado do **Negócio** (Problema) ao lado do **Software** (Solução). O desafio reside no fato de que **Clientes** e **Técnicos** vivem em "Mundos Diferentes":

| Clientes (Negócio)                          | Técnicos (Solução)                                         |
| :------------------------------------------ | :--------------------------------------------------------- |
| Dominam o **problema** (sua necessidade)    | Dominam a **solução técnica**                              |
| Conhecem as **regras do negócio**           | Sabem como colocar em programas as regras de negócio       |
| Têm necessidades que evoluem constantemente | Preferem congelar as expectativas e documentar requisições |
| Usam a **linguagem de negócio**             | Usam a **linguagem da tecnologia**                         |

>[!tip] Artefatos Chave na Comunicação
> - O lado do Negócio gera **Necessidades** e **Regras**.
> - O lado do Software gera **Visão**, **Especificação de Requisitos de Software (ERS)** e **Modelo de Domínio**.

### Análise de Negócios segundo BABOK v2
A **Análise de Negócio** (Business Analysis) é fundamental para **compreender o Negócio**. Segundo o **BABOK v2**:

>[!info] Definição de Análise de Negócio
> - É o conjunto de tarefas e técnicas utilizadas para atuar como um **elo de ligação** entre as partes interessadas (stakeholders).
> - Objetiva entender a estrutura, as políticas e as operações de uma organização, bem como os problemas envolvidos.
> - A finalidade é recomendar soluções que permitam que a organização alcance seus objetivos.

---
## Sistemas de Informação (SI)
Um **Sistema de Informação (SI)** é um conjunto de componentes inter-relacionados que coletam, manipulam e disseminam dados e informação, proporcionando um mecanismo de *feedback* para atender a um objetivo (Stairs e Reynolds, 2002).

>[!note] História do SI
> - Os sistemas de informação surgiram antes mesmo da informática.
> - Organizações se baseavam em técnicas de arquivamento e recuperação de informação.
> - Existia a figura do "arquivador", responsável por organizar, registrar, catalogar e recuperar dados.

### Três Dimensões do SI
Para entender [[Sistemas de Informação (SI)]] baseados em computador, é crucial entender as três dimensões inter-relacionadas:
- **Organização:** Sistema formal cujo objetivo é produzir produtos ou prestar serviços.
- **Pessoas (Stakeholders):** Interagem diretamente com o SI, usando as informações geradas para o processo de tomada de decisão.
- **Tecnologia da Informação (TI):** Conjunto de recursos tecnológicos e computacionais para a geração e uso da informação.
### Fluxo e Objetivo do SI
O objetivo do SI é **transformar Dados em Informação** por meio de um **PROCESSO**.
>[!info] Fluxo Lógico do SI
> 1. **Coleta** (dados)
> 2. **Manipula** (dados)
> 3. **Organiza e Recupera** (dados)
> 4. **Dissemina** (informação)
> 5. **Feedback** (mecanismo de retorno)

O processo de **Análise do Problema** e elaboração de uma **Proposta de Solução** é fundamental, culminando no **Software para Automação do Processo**. O software essencialmente **automatiza as tarefas de um processo de negócio**.

---
## Crise do Software e o Surgimento da ES
A disciplina de Engenharia de Software foi criada em reação à **"Crise do Software"** no início dos anos 70.
>[!question] A Crise do Software
> - Projetos estourando o orçamento e o prazo.
> - Software de baixa qualidade e difícil de manter.
> - Software não satisfazendo os requisitos.
> - A Engenharia de Software era praticamente inexistente.

A necessidade de sanar as deficiências de desenvolvimento, causada pelo aumento da complexidade dos processos e da tecnologia, levou à criação da **Engenharia de Software**.

>[!example] Consequências da Má Qualidade
> - **Ariane 5 (1996):** Foguete explodiu após 40 segundos devido a um *bug* de software, resultando em um prejuízo de US$ 500 milhões.
> - **Boeing 737 MAX 8 (2018/2019):** Dois acidentes resultaram em vítimas fatais. O sistema MCAS fez uma leitura errada do ângulo do avião, sem a opção de divergência para os pilotos.
### Qualidade de Software
- A **Qualidade de Software** refere-se à medida em que um software atende aos requisitos especificados, satisfaz as necessidades do usuário e opera de maneira confiável.
- Segundo Roger Pressman:
>[!quote] Definição de Qualidade de Software
> "Conformidade aos **requisitos funcionais** e de desempenho, explicitamente declarados, a padrões de desenvolvimento claramente documentados e a características implícitas que são esperadas de todo o software profissionalmente desenvolvido."

---
## Conceito e Elementos da Engenharia de Software
### Conceito Detalhado
A [[Engenharia de Software (ES)]] é definida como uma:
>[!info] Definição de ES (Pressman)
> "Disciplina tecnológica e gerencial preocupada com a produção sistemática de produtos de software, que são desenvolvidos e/ou modificados dentro do tempo e custo estimados, conforme os requisitos definidos e especificados."

**Diferença entre Ciência da Computação e ES:**
- A **Ciência da Computação** está relacionada com teorias e fundamentos.
- A **Engenharia de Software** está relacionada com a prática e o desenvolvimento de software.
### Elementos Fundamentais
A Engenharia de Software abrange métodos, ferramentas e procedimentos que possibilitam o controle do processo de desenvolvimento.
- **MÉTODO (Técnica):** Procedimento formal para produzir um resultado.
    - Exemplos incluem modelos de ciclo de vida como **Cascata**, **Espiral** e **Ágil**.
- **FERRAMENTA:** Instrumento ou sistema automatizado para realizar uma tarefa da melhor maneira.
    - Incluem IDEs, sistemas de controle de versão, e ferramentas de gerenciamento como **Jira**, **Trello** e **GitLab**.
- **PROCEDIMENTO:** Combinação de ferramentas e técnicas para produzir um resultado específico.
    - Incluem a análise de requisitos, design, implementação, teste e manutenção, garantindo qualidade e confiabilidade.

---
## O Processo de Construção de Software
O processo de software é um conjunto sequencial de atividades, objetivos, transformações e eventos que integram estratégias para o cumprimento da evolução de software (Pressman).
>[!note] Definição de Processo
> "Uma sequência de etapas que envolvem atividades, restrições e recursos para alcançar um resultado desejado."
### Etapas Genéricas de Construção
Cada estágio do ciclo de vida é um processo ou uma coleção de processos.

| Tarefas (Disciplinas)                                                           | Profissional              | Artefatos                                |
| :------------------------------------------------------------------------------ | :------------------------ | :--------------------------------------- |
| **[[04 - Modelagem de Processos de Negócio (BPMN)\|Modelagem do Negócio]]**     | Analista de Negócio       | **Documento de Análise de Negócio**      |
| **[[07 - O Processo Completo de Vida do Requisito\|Elicitação de Requisitos]]** | Analista de Requisitos    | **Documento de Definição de Requisitos** |
| **Análise e Projeto**                                                           | Analista de Sistemas      | Modelagem dos Requisitos/Especificação   |
| **Protótipo**                                                                   | UX/Designer               | Validação (representação gráfica)        |
| **Implementação/Codificação**                                                   | Programador/Desenvolvedor | **Programa (código)**                    |
| **Testes**                                                                      | Analista de Testes        | Roteiros de Teste                        |
| **Implantação**                                                                 | Analista de Homologação   | Documento de Implantação                 |
| **Manutenção**                                                                  | Equipe técnica            | Manual do Sistema                        |
### Foco da Engenharia de Requisitos
A **Engenharia de Requisitos** tem seu foco logo após a Análise de Negócio e é crítica para a definição do sistema.
>[!note] Engenharia de Requisitos
> - As tarefas de um processo de negócio são as referências para os *Requisitos de Software*.
> - A partir do processo mapeado e entendido, as tarefas, regras e lógica passam a ser fonte de referência para a identificação, definição e gerência dos requisitos do software.
> - Todas as mudanças em requisitos devem ser observadas a partir de mudanças nos processos e regras de negócio.
### Abordagens de Ciclo de Vida do Software
1. **Modelo Caótico:** Codifica-remenda (*"Programação Orientada a Gambiarra - POG"*).
2. **Modelos Tradicionais:**
    - [[Modelo Cascata]].
    - [[Modelo em Espiral]].
3. **Modelo Iterativo/Adaptativo:**
    - **[[RUP (Rational Unified Process)]]:** É um processo iterativo e adaptativo, organizado e consistente. A disciplina de **Requisitos** é mais intensa nas fases de **Iniciação** e **Elaboração**.
    - **[[SCRUM]]:** É um *framework* ágil, iterativo e incremental. O **Product Backlog é a principal fonte de requisitos para a Sprint**.
### O Sucesso em Projetos de Software
>[!tip] Fatores de Sucesso
> - O sucesso de um projeto de software é proporcional à **qualidade gerencial** que investimos nele.
> - É proporcional à **capacidade de entendimento do negócio**.

---