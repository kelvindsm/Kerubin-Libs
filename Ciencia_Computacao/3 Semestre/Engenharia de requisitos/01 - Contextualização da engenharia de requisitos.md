---
tags:
  - Naoconcluido
---

# Engenharia de Requisitos: Visão Geral e Contextualização na Engenharia de Software

## Introdução e Papel do Analista de Requisitos

- O **Analista/Engenheiro de Requisitos** atua como elo de ligação entre o **Cliente** (que domina o problema e as regras de negócio) e o **Desenvolvedor** (que domina a solução técnica).
- Seu papel é transformar as **necessidades** do cliente em **Requisitos de Software** que, por sua vez, são convertidos em código pelo desenvolvedor.
- A [[Comunicação]] é o ponto focal entre o **Negócio** (necessidades e regras) e o **Software** (visão, [[Especificação de Requisitos de Software|ERS]] e [[Modelo de Domínio]]).

>[!info] Mundos Diferentes (Cliente vs. Técnico)
> - **Clientes:** Dominam o problema (sua necessidade), conhecem as regras do negócio, usam a linguagem de negócio, e suas necessidades evoluem constantemente.
> - **Técnicos:** Dominam a solução técnica, sabem como colocar em programas as regras de negócio, usam a linguagem da tecnologia, e preferem congelar expectativas para documentar requisições.

## Sistemas de Informação (SI)

- Sistemas de informação surgiram antes mesmo da informática, baseados em arquivamento e recuperação de informações.
- **Definição de SI:** É um conjunto de componentes inter-relacionados que coletam, manipulam e disseminam dados e informação, proporcionando um mecanismo de feedback para atender a um objetivo.
- Os sistemas evoluíram para acompanhar os **Processos de Negócios**.
- O **Objetivo do SI** é transformar **Dados** em **Informação** através de um **PROCESSO**.

### Dimensões de um SI
- Um sistema de informação baseado em computador deve ser entendido por suas três dimensões:
    - **Organização:** Um sistema formal cujo objetivo é produzir produtos ou prestar serviços.
    - **Pessoas (Stakeholders):** Interagem diretamente com o SI, utilizando as informações geradas para algum processo de tomada de decisão da organização.
    - **Tecnologia da Informação (TI):** Conjunto de recursos tecnológicos e computacionais para a geração e uso da informação.

### Fluxo e Construção do SI
- **Fluxo Básico do SI:** Coleta (dados) $\rightarrow$ Manipula (dados) $\rightarrow$ Organiza e Recupera (dados) $\rightarrow$ Disseminação (informação) + **Feedback**.
- **Etapas para Solução de SI:**
    1. Descrição do Processo
    2. [[Mapeamento do Processo]]
    3. Análise do Problema
    4. Proposta de Solução
    5. Software para [[Automação de Processo|Automação do Processo]]

## Engenharia de Software (ES)

- Surgiu em resposta à "Crise do Software" (início dos anos 70), caracterizada por projetos que estouravam orçamento e prazo, software de baixa qualidade, não satisfazendo requisitos e sendo mal gerenciado.
- **Definição de ES:** Disciplina tecnológica e gerencial preocupada com a produção sistemática de produtos de software, desenvolvidos ou modificados dentro do tempo e custo estimados, conforme os requisitos definidos e especificados.
- **Qualidade de Software:** Refere-se à medida em que um software atende aos requisitos especificados, satisfaz as necessidades do usuário e opera de maneira confiável.

### Elementos Fundamentais e Objetivos da ES
- **Conceito:** A ES é a ciência que estuda o processo de construção de um determinado produto utilizando diversas tecnologias.
- **Elementos Fundamentais:**
    - **Método:** Procedimento formal para produzir um resultado (técnica). Inclui modelos de ciclo de vida, como o modelo em cascata, modelo em espiral, modelo ágil, entre outros.
    - **Ferramenta:** Instrumento ou sistema automatizado para realizar uma tarefa da melhor maneira. São softwares utilizados para apoiar e facilitar as atividades da ES, como IDEs e sistemas de controle de versão.
    - **Procedimento:** Combinação de ferramentas e técnicas para produzir um resultado específico. Referem-se aos métodos e passos específicos que os desenvolvedores seguem durante o ciclo de vida.
- **Objetivos da ES:**
    - Aplicação de teoria, modelos, formalismos, técnicas e ferramentas da ciência da computação.
    - Aplicação de métodos, técnicas e ferramentas para o gerenciamento do processo de desenvolvimento.
    - Produção da **documentação formal** destinada à comunicação.

### Etapas Genéricas de Construção de Software (Ciclo de Vida)
- **Etapas Genéricas:** Modelagem de Negócios $\rightarrow$ Requisitos $\rightarrow$ Análise e Design $\rightarrow$ Implementação $\rightarrow$ Testes $\rightarrow$ Implantação.
- O processo começa pelo **entendimento dos processos de negócio** envolvidos, pois "Software é automação de processo de negócio!".

>[!tip] Engenharia de Requisitos no Ciclo
> - A [[Engenharia de Requisitos]] está na fase de **Requisitos**.
> - As **tarefas** de um processo são as referências para os requisitos de software. O processo descrito, mapeado e entendido, torna-se a fonte de referência para a identificação, definição e gerência dos requisitos.

## Modelos de Processo de Software

- O **processo de software** é um conjunto sequencial de atividades, objetivos, transformações e eventos que integram estratégias para o cumprimento da evolução de software.

### Tipos de Modelos de Ciclo de Vida
- **[[Modelo Cascata]]:** Linear e sequencial (Levantamento de Requisitos $\rightarrow$ Análise $\rightarrow$ Projeto $\rightarrow$ Codificação $\rightarrow$ Testes $\rightarrow$ Implantação).
- **[[Modelo em Espiral]]:** Modelo de processo de software que engloba planejamento, análise de risco, engenharia e avaliação.
- **[[RUP (Rational Unified Process)]]:** É um processo iterativo e adaptativo de desenvolvimento, tradicional, organizado e consistente.
- **[[Modelos Ágeis]] (ex: Scrum):** Desenvolvem o software em ciclos curtos e incrementais.
    - **Scrum:** É um *framework* ágil, iterativo e incremental. Ajuda a gerar valor por meio de soluções adaptativas para problemas complexos.

### Técnicas e Disciplinas na Construção de Software
- **Prototipação:** Abordagem baseada numa visão evolutiva do desenvolvimento de software. Envolve a produção de versões iniciais (protótipos) para realizar verificações e experimentações. "Para o usuário, a interface é o sistema".
- **Projeto de Software:** Representa a **solução técnica** às necessidades de negócio e requisitos identificados. Deve conter as soluções técnicas necessárias (modelagem de requisitos, especificações, arquitetura, etc.).
- **Codificação de Software:** Traduz os requisitos de software em ações a serem executadas em uma linguagem de programação.
- **Testes de Software:** Verificação para garantir que o software atende aos requisitos.
- **Implantação:** Fase do ciclo de vida que corresponde textualmente à passagem do software para a produção.
- **Manutenção:** Conjunto de atividades realizadas após a entrega do sistema para garantir seu bom funcionamento e atender às necessidades em constante evolução dos usuários (correção de erros, adaptação, melhorias).