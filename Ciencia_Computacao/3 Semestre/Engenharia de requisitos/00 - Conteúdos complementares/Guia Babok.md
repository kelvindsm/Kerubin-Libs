# Guia BABOK® Versão 2.0: Corpo de Conhecimento de Análise de Negócios

## I. Definição e Conceitos Chave

>[!info] Análise de Negócios (Business Analysis)
>É o conjunto de tarefas e técnicas usadas para atuar como uma **ligação** entre as Partes Interessadas, visando:
>- Compreender a **estrutura, políticas e operações** de uma organização.
>- Recomendar **soluções** que capacitem a organização a atingir suas Metas do Negócio.
>- O analista deve desvendar as **verdadeiras necessidades** e não apenas os desejos explícitos.

### Tipos de Requisitos e Classificação
O termo **Requisito** é abrangente e descreve uma condição ou capacidade necessária para resolver um problema ou atingir um objetivo.

| Tipo de Requisito                      | Foco Principal                    | Definição                                                                                                                                      |
| :------------------------------------- | :-------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| **Requisitos do Negócio**              | Nível Estratégico (Metas)         | Metas de mais alto nível, objetivos ou necessidades da organização. Descrevem as razões do projeto e as métricas de sucesso.                   |
| **Requisitos das Partes Interessadas** | Nível Tático (Usuário)            | Necessidades de uma parte interessada específica. Servem como ponte entre os requisitos de negócio e os da solução.                            |
| **Requisitos da Solução**              | Nível Operacional (Implementação) | Características que a solução deve ter para atender aos requisitos superiores.                                                                 |
| **Requisitos de Transição**            | Nível Transitório (Migração)      | Capacidades temporárias necessárias para fazer a transição do estado atual para o futuro, mas que não serão mais necessárias após a transição. |

**Requisitos da Solução (Divisão):**
- **Requisitos Funcionais**: Descrevem o **comportamento** e a informação que a solução irá gerenciar (capacidades).
- **Requisitos Não-Funcionais**: Capturam **qualidades** e condições ambientais, como desempenho, segurança, usabilidade, manutenibilidade (também chamados de atributos de qualidade ou requisitos suplementares).

---
## II. Áreas de Conhecimento e Tarefas Detalhadas
### 1. Planejamento e Monitoramento da Análise de Negócios (Capítulo 2)

>[!note] Objetivo
>Define como a análise de negócios será executada, incluindo a abordagem, partes interessadas e o monitoramento do progresso.

- **Planejar a Abordagem da Análise de Negócios (2.1)**
- **Propósito**: Selecionar a abordagem geral (planejamento vs. mudança) e definir técnicas e entregas.
- **Abordagem Orientada ao Planejamento**: Foco em minimizar incerteza e definir a solução totalmente antes da implementação; visa **máximo controle** e **redução de risco**.
- **Abordagem Orientada à Mudança (Ágil)**: Foco na **entrega rápida e incremental** de valor de negócio, aceitando maior incerteza sobre o produto final.
- **Conduzir a Análise das Partes Interessadas (2.2)**
- **Propósito**: Identificar partes interessadas, determinar sua **influência, atitude** e **autoridade de aprovação**.
- **Técnicas**: Matriz RACI, Mapa das Partes Interessadas (Matriz Influência/Impacto e Diagrama Cebola).
- **Planejar Atividades da Análise de Negócios (2.3)**
- **Propósito**: Determinar atividades e entregas, estimar o esforço e tempo, e identificar as ferramentas de gestão.
- **Planejar a Comunicação da Análise de Negócios (2.4)**
- **Propósito**: Definir a **estrutura, cronograma, formato, público e método** para a comunicação das atividades de análise e requisitos.
- **Planejar o Processo de Gerenciamento de Requisitos (2.5)**
- **Propósito**: Definir o processo para **aprovar requisitos, gerenciar mudanças e rastrear** (rastreabilidade).
- **Elementos**: Definição do **[[Git|Repositório]]** , **Rastreabilidade** , **Atributos** dos requisitos (ex: prioridade, estabilidade) e o **Processo de Gerenciamento de Mudança**.
- **Gerenciar o Desempenho da Análise de Negócios (2.6)**
- **Propósito**: Garantir que as atividades de análise são executadas de forma eficaz e determinar as **métricas de desempenho**.

---
### 2. Elicitação (Capítulo 3)

>[!note] Objetivo
>Se reunir ativamente com as partes interessadas para **elucidar, extrair e tornar visível** a informação referente às suas necessidades.

- **Preparar a Elicitação (3.1)**: Garantir que todos os recursos (pessoas, instalações, equipamentos) e materiais de apoio estejam agendados e organizados.
- **Conduzir a Atividade de Elicitação (3.2)**: Executar a técnica de elicitação (entrevistas, workshops, etc.) para extrair informações. O analista deve rastrear requisitos em relação aos objetivos de negócio para **evitar o desvio de escopo**.
- **Documentar os Resultados da Elicitação (3.3)**: Registrar a informação provida pelas partes interessadas em um formato estruturado (Requisitos [Declarados]).
- **Confirmar Resultados da Elicitação (3.4)**: Validar se os requisitos declarados estão alinhados à compreensão do problema e às intenções das partes interessadas.

---
### 3. Gerenciamento e Comunicação dos Requisitos (Capítulo 4)

>[!note] Objetivo
>Assegurar um **entendimento compartilhado** dos requisitos e gerenciar o escopo e as mudanças.

- **Gerenciar o Escopo e os Requisitos da Solução (4.1)**: Obter e manter **consenso** e a **aprovação** dos requisitos pelas partes interessadas com autoridade. Isto pode resultar no estabelecimento de uma **Linha de Base**.
- **Gerenciar Rastreabilidade dos Requisitos (4.2)**: Criar e manter relacionamentos entre requisitos, objetivos de negócio, entregas e componentes da solução. Essencial para **análise de impacto** e gerenciamento de mudanças.
- **Manter Requisitos para Reutilização (4.3)**: Gerenciar o conhecimento sobre requisitos após a implementação, tornando-os disponíveis (mantidos e reusáveis) para **iniciativas futuras**.
- **Preparar o Pacote de Requisitos (4.4)**: Selecionar e estruturar um conjunto de requisitos no **formato apropriado** (documentação formal, modelos, apresentação) para um público específico.
- **Comunicar Requisitos (4.5)**: Usar conversas, documentos e apresentações para levar as partes interessadas a uma **compreensão comum** do escopo e da situação atual dos requisitos.

---
### 4. Análise Corporativa (Capítulo 5)

>[!note] Objetivo
>Identificar uma necessidade do negócio, definir a solução e justificar o investimento. É aqui que os [[Requisitos do Negócio]] são definidos.

- **Definir a Necessidade do Negócio (5.1)**: Identificar o **problema ou oportunidade** e o **Resultado Desejado** (benefícios). Um bom objetivo deve ser **SMART** (eSpecífico, Mensurável, Alcançável, Relevante, Temporal).
- **Avaliar Gaps (Lacunas) de Capacidades (5.2)**: Comparar as capacidades atuais da corporação (processos, pessoas, tecnologia) com as capacidades requeridas para atender à necessidade do negócio.
- **Determinar a Abordagem da Solução (5.3)**: Identificar e avaliar alternativas para criar ou adquirir as novas capacidades requeridas (ex: comprar software de prateleira, desenvolver customizado, mudar processos).
- **Definir o Escopo da Solução (5.4)**: Determinar quais **novas capacidades** uma iniciativa entregará, definindo as fronteiras da solução e os componentes incluídos/excluídos.
- **Definir o Business Case (5.5)** : Descrever a **justificativa** para o investimento em termos de **custos vs. valor/benefícios**. Inclui a **Avaliação do Risco** inicial e a forma como os resultados serão medidos.

---
### 5. Análise de Requisitos (Capítulo 6)

>[!note] Objetivo
>Analisar os requisitos declarados para definir as capacidades detalhadas da solução, verificando sua qualidade e validando seu valor.

- **Priorizar Requisitos (6.1)**: Determinar a importância relativa dos requisitos (baseado em valor, risco, dificuldade de implementação, etc.) para focar os esforços. **Análise MoSCoW** (Must, Should, Could, Won’t) é uma técnica comum.
- **Organizar Requisitos (6.2)**: Criar um conjunto coeso de **Modelos de Requisitos** (como Diagramas de Fluxo de Dados ou Modelos de Classes) e identificar inter-relacionamentos e dependências.
- **Especificar e Modelar Requisitos (6.3)**: Analisar os desejos expressos usando **declarações textuais, matrizes e diagramas** para estruturar e aperfeiçoar a compreensão.
- **Definir Suposições e Restrições (6.4)**: Identificar fatores que se acredita serem verdadeiros (Suposições) ou limitações impostas (Restrições) que afetam as soluções viáveis, mas não são requisitos em si.
- **Verificar Requisitos (6.5)**: Garantir que os requisitos foram definidos **corretamente** e atendem aos padrões de qualidade (coesão, completude, consistência, **testabilidade**, etc.).
- **Validar Requisitos (6.6)**: Garantir que os requisitos entregam **valor para o negócio** e estão alinhados às metas e objetivos. Garante que a **solução correta** será construída.

---
### 6. Avaliação e Validação da Solução (Capítulo 7)

>[!note] Objetivo
>Garantir que as soluções encontradas atendam à necessidade do negócio e facilitar o sucesso de sua implementação.

- **Avaliar Solução Proposta (7.1)**: Determinar o quanto as soluções propostas atendem aos requisitos aprovados, ranqueando as opções e identificando capacidades adicionais.
- **Alocar Requisitos (7.2)**: Distribuir os requisitos nos **componentes da solução** (pessoas, processos, software) e nas **liberações** (fases/iterações) para maximizar o valor.
- **Avaliar a Prontidão Organizacional (7.3)**: Avaliar o efeito da nova solução na organização (cultural, operacional, técnico) e se ela está preparada para a mudança.
- **Definir Requisitos de Transição (7.4)**: Definir capacidades temporárias (ex: conversão de dados, treinamento) necessárias para a transição entre a solução existente e a nova.
- **Validar a Solução (7.5)**: Garantir que a **solução entregue** atende à necessidade do negócio e identificar a resposta mais apropriada para os **defeitos identificados**.
- **Avaliar o Desempenho da Solução (7.6)**: Avaliar soluções em funcionamento para entender o **valor que entregam** em relação aos requisitos do negócio e identificar oportunidades de melhoria.

---
## III. Competências Fundamentais (Capítulo 8)

| Categoria                                         | Descrição                                                                                     | Exemplos de Habilidades                                                                     |
| :------------------------------------------------ | :-------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| **Pensamento Analítico e Resolução de Problemas** | Habilidade para gerar novas ideias e avaliar situações de forma crítica.                      | Pensamento Criativo , Tomada de Decisão , Pensamento Sistêmico.                             |
| **Habilidades de Interação**                      | Foco na mediação e colaboração eficaz com as partes.                                          | Facilitação e Negociação , Liderança e Influência , Trabalho em Equipe.                     |
| **Habilidades de Comunicação**                    | Capacidade de expressar e documentar ideias de forma eficaz e apropriada para o público.      | Comunicações Verbais , Ensino (adaptando a estilos de aprendizado) , Comunicações Escritas. |
| **Conhecimento de Negócios**                      | Compreensão do ambiente operacional e estratégico no qual a análise é feita.                  | Princípios de Negócios , Conhecimento de Mercado e da Organização.                          |
| **Características Comportamentais**               | Qualidades pessoais que sustentam a confiança e o profissionalismo.                           | Ética , Confiabilidade , Organização Pessoal.                                               |
| **Aplicativos de Software**                       | Proficiência no uso de ferramentas para documentação, modelagem e rastreamento de requisitos. | Processadores de texto, Planilhas , Ferramentas de Gerenciamento de Requisitos (RMs).       |

---
## IV. Técnicas Chave (Capítulo 9)
As técnicas mudam a forma como as tarefas são executadas.
- **Modelagem**: Diagrama de Fluxo de Dados (DFD) , Modelagem de Dados (DER/Classes) , Modelagem de Processos (Fluxograma/UML) , Diagramas de Estados.
- **Análise Estratégica/Decisão**: *Análise SWOT* (Forças, Fraquezas, Oportunidades, Ameaças) , *Análise de Decisão* (árvores, análise financeira) , [[Análise de Riscos]] (tolerância, avaliação, resposta). 
- **Elicitação Colaborativa**: *Workshop de Requisitos* , [[Brainstorming]] , *Grupos Focais* , *Entrevistas* , *Observação* (passiva/ativa).
- **Documentação/Estrutura**: *Cenários e Casos de uso* , *Histórias do Usuário* , Definição dos *Critérios de Aceite e Avaliação* (testabilidade).
---