---
tags:
  - EngRequisitos
  - NaoRevisado
---
# Engenharia de Requisitos - Processo de Gerenciamento de Requisitos

## O Processo da Engenharia de Requisitos (ER)

A Engenharia de Requisitos é um processo cíclico que envolve várias etapas interligadas. O **[[07 - O Processo Completo de Vida do Requisito|Gerenciamento]]** é uma atividade que atua como base para todas as etapas.
### Etapas do Processo de ER
1.  **Elicitação**: Investigação, busca e descoberta dos requisitos.
2.  **Análise**: Avaliação de possíveis **conflitos**, identificação das relações com o contexto e definição dos requisitos.
3.  **Especificação**: Documentação e detalhamento das especificações dos requisitos.
4.  **Validação**: Validação dos requisitos em relação aos propósitos do produto de software.
5.  **Produção ou Desenvolvimento**.
6.  **Gerenciamento**: Atividade que administra os requisitos ao longo do tempo, permeando todo o processo de ER.
## O Papel do Gerenciamento de Requisitos (GR)
Os requisitos de sistemas de software são **voláteis** e estão sempre mudando. O Gerenciamento de Requisitos (GR) é o enfoque sistemático para a elicitação, organização e documentação dos requisitos, e um processo que estabelece e **mantém o acordo** entre usuários e a equipe de projeto à medida que os requisitos se modificam.
### Por Que o GR é Crítico
- É preciso manter o **acompanhamento dos requisitos** e as ligações entre os requisitos dependentes para avaliar o impacto das mudanças.
- Alterações precisam ser conduzidas de forma **ordenada** para evitar a perda de controle sobre o prazo e o custo do desenvolvimento.
- Estatisticamente, **51% dos recursos financeiros** gastos em projetos são desperdiçados devido ao GR ineficiente.
### Atividades de Gerenciamento (Contabilidade em ER)
As atividades de GR visam garantir a qualidade e a eficiência do processo.
- **Organizar**: Identificar cada requisito de forma única e registrar metadados (autor, data, fonte, status, etc.).
- **Armazenar e Encontrar**: Armazenar os requisitos de forma que possam ser sistematicamente pesquisados.
- **Rastreabilidade**: Ajuda a responder de onde vêm os requisitos, quão interdependentes são e onde serão implementados/testados.
- **Mudanças**: Estabelecer e implementar um **processo formal** para alterar os requisitos existentes.
- **Priorizar**: Definir quais requisitos são importantes e o grau dessa importância.
## Subáreas do Gerenciamento de Requisitos
Os principais aspectos do Gerenciamento de Requisitos incluem: Gerenciamento de Mudanças, Gerenciamento de Configuração, Gerência da Qualidade de Requisitos e Rastreabilidade.
### 1. Gerenciamento de Mudanças
Os requisitos são, inevitavelmente, **incompletos e inconsistentes**. O Gerenciamento de Mudanças (GM) trata as alterações de forma controlada.
#### Fontes de Mudança e Riscos
- **Fatores de Mudança**: Mudanças de legislação, novas necessidades do cliente, erros na elicitação, novas percepções de *stakeholders* (concorrentes), ou aumento de demanda no mercado.
- **Riscos da Mudança**: Pode introduzir **defeitos**, atrasar o projeto, exigir mais esforço/custo do que o calculado ou levar à insatisfação do usuário.
#### O Processo de Controle de Mudanças
O processo de controle de mudanças permite que todas as mudanças sejam **rastreadas** e garante que nenhuma solicitação seja perdida. O GM facilita a tomada de decisão e o controle de custos e prazos.
- A habilitação da mudança (ou processo de controle) exige que uma organização designe uma **autoridade de mudança** para decidir sobre as alterações.
- **Abordagem Sequencial**: A autoridade de mudança é frequentemente designada para a gestão do projeto, um Comitê ou um **Conselho de Controle de Mudanças (CCM)**.
- **Abordagem Iterativa (Ágil)**: A autoridade de mudança geralmente é o **Product Owner**, que adiciona uma mudança aceita como um novo item no *product backlog*.
### 2. Gerenciamento de Configuração
Uma **Configuração** é um conjunto consistente de itens (produtos de trabalho) logicamente relacionados que contêm requisitos. O objetivo é deixar claro quais requisitos são ou foram válidos em uma determinada situação.
#### Propriedades de uma Configuração Correta
- **Logicamente Conectada**: Conjunto de requisitos unido em vista de um certo objetivo.
- **Consistente**: O conjunto não tem conflitos internos e pode ser integrado.
- **Única**: A configuração e seus requisitos constituintes são identificados de forma clara e única.
- **Imutável**: É composta de requisitos selecionados, cada um com uma **versão específica que nunca será alterada nesta configuração**.
- **Base para Restauração (*Rollback*)**: Permite o retorno a uma configuração anterior se ocorrerem efeitos indesejados.
#### Linha de Base (*Baseline*)
É uma configuração **estável**, validada e sob gestão controlada de mudanças que sinaliza um **marco** ou ponto de avaliação no projeto.
- Exemplo: Configuração que é válida na liberação em produção de uma determinada *release*.
- O *backlog* da *sprint* em um projeto ágil serve como *baseline* no início da próxima iteração.
#### Controle de Versão
- Requer uma **identificação única** para cada versão de um produto de trabalho.
- Requer uma **descrição clara** de cada mudança, vinculada ao número da versão.
- **Numeração**: Tipicamente composta por **Versão** (aumentada em atualizações substantivas, começa em 1 após aprovação) e **Incremento** (aumentado a cada mudança visível).
### 3. Gerenciamento da Qualidade dos Requisitos (GQR)
O GQR define o **padrão de produção e verificação da qualidade** dos requisitos. É um processo sistemático que visa **prevenir e eliminar defeitos**.
- **Objetivo**: Evitar defeitos em cada fase antes de passar para a fase seguinte.
- A qualidade dos requisitos deve ser assegurada em **todas as etapas** (elicitação, análise, especificação, validação e gerenciamento).
#### Metadados e Atributos dos Requisitos
Os requisitos precisam ser completamente e corretamente identificados e descritos. Metadados (dados sobre dados) tornam os produtos de trabalho gerenciáveis.
- **Atributos Recomendados (ISO 29148)**:
    - **Identificação**: Identificador único e imutável (impossível sem ele).
    - **Prioridade para os *stakeholders***: Prioridade acordada do ponto de vista dos *stakeholders*.
    - **Dependências**: Relações com outros requisitos (ex: requisito de baixa prioridade deve ser implementado por depender de outro de alta).
    - **Risco**: Potencial da implementação levar a problemas (custos extras, atrasos).
    - **Fonte**: Origem do requisito.
    - **Justificativa**: Razão pela qual o requisito é necessário.
    - **Dificuldade**: Estimativa do esforço para implementar.
    - **Tipo**: Funcional, de qualidade ou de restrição.
#### Priorização dos Requisitos
É o nível de importância atribuído a um requisito de acordo com determinados critérios.
- **Passos**: Definir metas, critérios de avaliação, *stakeholders* envolvidos e a técnica de priorização.
- **Técnicas de Priorização**:
    - **Ad Hoc**: Especialistas atribuem prioridades com base em sua experiência (Ex: Top-10, MOSCOW, Análise Kano).
    - **Analíticas**: Usam processo sistemático, onde especialistas atribuem pesos a múltiplos critérios (benefício, custo, risco, esforço) para calcular prioridades ponderadas (Ex: Matriz GUT, Benefício x Esforço).
### 4. Rastreabilidade dos Requisitos
A **Rastreabilidade** é o conjunto de **ligações** entre as fontes dos requisitos, os requisitos propriamente ditos e outros artefatos (componentes, casos de teste). Sem rastreabilidade adequada, a ER é dificilmente viável.
#### Tipos de Rastreabilidade
1.  **Rastreabilidade Retroativa (Pré-especificação)**: Qual foi a **origem** de um determinado requisito? Que fontes (stakeholders, documentos, legislação) foram analisadas durante a elicitação?
2.  **Rastreabilidade Progressiva (Pós-especificação)**: Onde este requisito é **utilizado**? Quais produtos (módulos, casos de teste, manuais) se baseiam nele?
3.  **Rastreabilidade entre Requisitos**: Que requisitos **dependem** de outros requisitos? O requisito é um refinamento de um requisito de nível superior?
#### Documentação da Rastreabilidade
Em projetos complexos, deve ser documentada explicitamente.
- Uso de atributos específicos (Ex: **Fonte**).
- Desenvolvimento de uma **Matriz de Rastreabilidade** em planilha ou tabela de banco de dados.
- Uso de *hyperlinks* no estilo Wiki na documentação textual.
- Visualização das relações em um gráfico de rastreamento.
---