---
tags:
  - Concluido
---
# Gerenciamento de Processos de Negócio (BPM) e o Guia BPM CBOK

## Introdução: O Foco em Processos e Automação

O **Gerenciamento de Processos de Negócio (BPM - Business Process Management)** é a disciplina fundamental para a compreensão e otimização do funcionamento de uma organização, servindo de base para qualquer projeto de tecnologia e *Engenharia de Requisitos*.

>[!quote] Segundo Bill Gates
>- A automação aplicada a uma operação eficiente aumentará a eficiência, mas aplicada a uma operação ineficiente aumentará a ineficiência. Isso reforça a importância de entender e otimizar os processos antes de automatizá-los.

### O Guia BPM CBOK®
O **Guia para o [[BPM CBOK]]® (Business Process Management Common Body of Knowledge)** é um documento de consulta básica para profissionais.

- **Finalidade:** Identificar e fornecer uma visão geral das **Áreas de Conhecimento** que são geralmente reconhecidas e aceitas como boas práticas em BPM.
- **Estrutura:** O guia é organizado em **nove áreas de conhecimento** (ou capítulos).

---
## Conceitos de Negócio e Processo

>[!quote] Conceito de Negócio
> O termo **NEGÓCIO** refere-se a pessoas que interagem para executar um conjunto de atividades de entrega de valor a clientes e gerar retorno de investimento a partes interessadas.

- **Abrangência:** Negócio abrange todos os tipos de organizações, com ou sem fins lucrativos, incluindo as governamentais.
 
>[!quote] Conceito de Processo
>Um **Processo** é a maneira típica de realizar o trabalho em uma empresa.

- **Definição (ISO, 1990):** Conjunto de recursos e atividades inter-relacionadas que transformam **insumos (entradas)** em **produtos (saídas)**.
- **Definição (Hammer e Champy, 1994):** Um processo é um grupo de atividades realizadas numa sequência lógica com o objetivo de produzir um **bem ou serviço que tem valor** para um grupo específico de clientes.
- **Características:**
- São disparados por **eventos específicos**.
- São compostos por várias **tarefas ou atividades inter-relacionadas**.
- Apresentam um ou mais resultados que podem conduzir ao término ou à transferência de controle para outro processo.
- Não existe produto ou serviço sem um processo empresarial, e não faz sentido existir um processo que não ofereça um produto ou serviço.

### Processo de Negócio (Business Process)

O foco na perspectiva de BPM é o **Processo de Negócio**.

>[!info] Definição de Processo de Negócio
> É um trabalho **ponta a ponta ("end-to-end")** que entrega **valor aos clientes**. Essa noção de trabalho *ponta-a-ponta* é chave, pois envolve todo o trabalho cruzando limites funcionais.

- **Inter-funcionalidade:** A primeira característica importante dos processos é a **inter-funcionalidade**. A maioria dos processos importantes atravessa as fronteiras das áreas funcionais.
- **Clientes:** A segunda característica é que eles têm clientes, que podem ser internos ou externos.

---
## Processo vs. Função e Tipos de Processos
### Processo vs. Função
A **Visão por Processos** contrasta com a **Visão Tradicional (Funcional)** das organizações, que se baseia na **especialização da tarefa** e estrutura hierárquica.

| Atributos | Visão Tradicional (Função) | Visão por Processos (Processo) |
| :--- | :--- | :--- |
| **Foco** | Chefe | Cliente |
| **Relacionamento primário** | Cadeia de comando | Cliente / Fornecedor |
| **Orientação** | Hierárquica | Processo |
| **Quem toma decisão** | Gerência | Todos os participantes |
| **Estilo** | Autoritário | Participativo |

- **Funções de Negócio:** Grupo de atividades relacionadas a objetivo ou tarefa particular (Ex: vendas, finanças). Funções são contínuas e permanentes.
- **Processos de Negócio:** Focam em transações **ponta a ponta** para agregar valor ao cliente. O departamento funcional (ex: Contabilidade) suporta esses processos, mas não é o responsável pelo trabalho ponta a ponta associado ao macroprocesso.

### Tipos de Processos de Negócio
Existem três categorias básicas de processos empresariais:
1. **Processos Primários (Essenciais ou de Negócio):**
- Caracterizam a atuação da empresa e são suportados por outros processos internos.
- Resultam no **produto ou serviço** que é recebido por um **cliente externo**.
- *Exemplos:* Vendas, Desenvolvimento de produtos, Distribuição.
2. **Processos de Suporte (Secundários ou Auxiliares):**
- São centralizados na organização e **viabilizam o funcionamento coordenado** dos subsistemas.
- Garantem o **suporte adequado** aos processos de negócio.
- *Exemplos:* Orçamento empresarial, Recrutamento e seleção, Compras.
3. **Processos de Gerenciamento (Gerenciais):**
- Focalizados nos gerentes e suas relações.
- Incluem ações de **planejamento, medição e ajuste** do desempenho da organização.
- *Exemplos:* Fixação de metas, Avaliação do resultado da empresa, Planejamento estratégico.

---
## O Ciclo de Vida BPM
>[!quote] Conceito
>A prática gerencial de BPM é caracterizada como um **ciclo de vida contínuo (processo) de atividades integradas**. A maioria dos ciclos pode ser sumarizada por um conjunto gradual e interativo de atividades.
As seis atividades contínuas do ciclo de vida BPM incluem:

1. **Planejamento:**
	- Começa com o desenvolvimento de um plano e uma **estratégia dirigida a processos**.
	- **Objetivo:** Assegurar uma compreensão sólida de como o processo se relaciona com seu ambiente externo.
	- Envolve identificar papéis, metas de desempenho e metodologias.
2. **Análise:**
	- Visa **entender os atuais processos organizacionais** (As Is) no contexto das metas e objetivos desejados.
	- Assimila informações de planos estratégicos, modelos de processo e medições de desempenho.
3. **Desenho e Modelagem:**
	- Foca no **desenho intencional** de como o trabalho **ponta-a-ponta** ocorrerá para entregar valor aos clientes.
	- Envolve a modelagem do processo (Modelo **To Be**) e a criação de especificações de processos.
	- O desenho fornece planos e diretrizes sobre a aplicação de fluxos, regras e a interação de aplicações e tecnologias.
4. **Implementação (Implantação):**
	- É a realização do desenho aprovado em **procedimentos e fluxos de trabalho documentados, testados e operacionais**.
	- Inclui a implementação de políticas e procedimentos novos ou revisados.
	- Pequenos ajustes podem ocorrer, mas a implementação assume que as especificações estão completas.
5. **Monitoramento e Controle:**
	- É o monitoramento formal e planejado da execução do processo e o rastreamento dos resultados.
	- Provê **informações-chave de desempenho** através de métricas relacionadas às metas e ao valor para a organização.
	- A análise dos dados de desempenho pode resultar em atividades de melhoria ou redesenho.
6. **Refinamento:**
	- Trata de **ajustes e melhorias pós-implementação** com base nos indicadores e informações-chave de desempenho obtidas no monitoramento.

Os processos de negócio ao longo do ciclo de vida são habilitados ou restringidos por fatores primários como **valores, crenças, liderança e cultura**.

---
## Medição e Desempenho
A prática de Gestão por Processos requer a **medição e supervisão do desempenho do processo**.
- **Princípio:** "Não se gerencia o que não se mede, não se mede o que não se define, não se define o que não se entende e não há sucesso no que não se gerencia" (William Edwards).

### Dimensões do Desempenho:
1. **Extensão com que as metas de processo são alcançadas** (**Eficácia** - Fazer as coisas certas...).
2. **Eficiência e eficácia das atividades de processo** (**Eficiência** - Fazer bem as coisas...).

A medição fornece *feedback* valioso para outras atividades primárias, como análise, desenho e transformação de processos. As métricas podem incluir custos, tempo de conclusão de tarefas, e alertas sobre variações (gargalos e atrasos).

---
## Mapeamento de Processos
O **[[04 - Modelagem de Processos de Negócio (BPMN)|Mapeamento de Processos]]** é fundamental para a identificação dos processos essenciais e para uma análise sistêmica das organizações.
### Elementos do Mapeamento
O mapeamento de processos tipicamente possui os seguintes elementos:
- **Raia** (Swimlane).
- **Stakeholders** envolvidos.
- **Início e Fim** de cada processo.
- **Atividades** de cada um.
- **Regras** para execução das atividades.
- **Sequência** das atividades.
### O Uso do Fluxograma
O **Fluxograma** (diagramação lógica) é uma ferramenta inestimável e simples para entender o funcionamento interno e os relacionamentos entre os processos.
- **Definição:** Método para descrever graficamente um processo existente ou proposto, usando símbolos simples, linhas e palavras.
- **Importância:** Mostra como os elementos se relacionam, permite comparação com o processo real, determina como melhorar a atividade e facilita a comunicação.
- **Símbolos Básicos:** Início/Fim (círculo), Sentido da Atividade (seta), Atividade (retângulo), Tomada de Decisão (diamante).
### Hierarquia de Processos
O entendimento da hierarquia dos processos contribui para a melhor gestão e compreensão da organização.
- **Processos Empresariais:** Processo crítico para o andamento do negócio e a satisfação do cliente.
- **Processos:** Conjunto de atividades que iniciam e terminam com o Cliente externo.
- **Sub-Processos:** Grupos de atividades que envolvem um ou mais departamentos.
- **Atividades:** Ações realizadas nos processos e/ou sub-processos. Trabalho tipicamente executado por um departamento ou pessoa.
- **Tarefas:** Ações realizadas nas atividades. É o nível mais granular.

>[!note] Regras
> São condições que norteiam ou permitem desvios na execução das atividades de um determinado processo.

---
## Sessões de Mapeamento
Uma sessão de mapeamento é uma reunião de trabalho realizada com pessoas-chave que dominam o processo em análise.
- **Objetivo Principal:** Definir e criticar o processo, identificar regras de trabalho e oportunidades de melhorias.
- **Participantes:** Gestores envolvidos e colaboradores de perfil diferenciado na execução das atividades.
### Fases de uma Sessão de Mapeamento
1. **Fase 1 - Mapeamento em Grupo:**
	- Foco gerencial ou operacional.
	- **Objetivo:** Identificar características e necessidades do processo sob a visão de cada papel envolvido e atingir o **consenso** entre os participantes.
2. **Fase 2 - Mapeamento Individual:**
	- Foco mais operacional.
	- **Objetivos:** Detalhar, especificar, exemplificar e **validar** as informações apresentadas no mapeamento em grupo.
	- Aspectos operacionais e particularidades são identificados e documentados pelo analista de processos.

---