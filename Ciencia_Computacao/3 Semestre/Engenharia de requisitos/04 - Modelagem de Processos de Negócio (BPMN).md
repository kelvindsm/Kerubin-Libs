---
tags:
  - Naoconcluido
---
# Modelagem de Processos de Negócio (BPMN)

## 1. Introdução à Modelagem de Processos

- **Definição de Modelagem:** Conjunto de atividades envolvidas na criação de **representações** de processos de negócio (existentes ou propostos);
- **Modelo:** Representação simplificada de algo (conceito, atividade) que pode ser matemático, gráfico, físico ou narrativo
- **Propósito:** Criar uma representação do processo de maneira **completa e precisa** sobre seu funcionamento.

### Níveis de Representação (CBOK)
| Nível                           | Características                                                             | Uso Recomendado                                           |
| ------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------- |
| **Diagrama** <br>(mais simples) | Baixa precisão, visão macro, elementos principais.                          | Entendimento rápido, alto nível.                          |
| **Mapa** (intermediário)        | Média precisão, visão abrangente, inclui atores, eventos e resultados.      | Identificação de regras, validações e papéis.             |
| **Modelo** <br>(mais detalhado) | **Alta precisão**, notação universal padronizada, inclui todos os recursos. | **Simulação** de processo e **Geração de Código** (BPMS). |

>[!tip] Modelos BPMN
> Se o objetivo **não for automatizar**, não é recomendado fazer um modelo BPMN detalhado devido ao alto custo de manutenção/desatualização.

## 2. BPMN (Business Process Model and Notation)

- É a mais poderosa e atual notação para modelar processos de negócio, sendo um padrão aberto mantido pela [[OMG]] (Object Management Group).
- **Vantagens:** Intuitiva, Simples, Flexível, Expansível e facilita a comunicação entre Negócios e TI, permitindo a automação.
- **Não é adequada para:** Organogramas, telas de sistemas ou mapas estratégicos.

>[!note] Comparação entre BPMN, Fluxograma e [[UML (Unified Modeling Language)]]
>- BPMN: Padrão OMG, útil para diversos públicos-alvo
>- Fluxograma: Símbolos simples, precursor
>- UML: Diagrama de Atividades para descrever requisitos de sistemas

>[!info] Foco do BPMN
> O BPMN aproxima a área de **Negócios** com a **Tecnologia**, permitindo que o modelo de processo seja interpretado e gere código de sistemas para automação.
> - É a mais poderosa e atual notação para modelar processos de negócio
> - **Vantagens:** intuitiva, Simples (pode evoluir de elementos básicos), Flexível, Expansível, Facilita a comunicação entre Negócios e TI
> - **Não é adequada para:** Organogramas, telas de sistemas, regras de negócio de sistemas

## 3. Elementos Fundamentais do BPMN

A modelagem BPMN é dividida em 4 categorias:

### 3.1. Objetos de Fluxo (Flow Objects)
Definem o comportamento do processo.
1.  **Eventos (Events)** (Círculo): Algo que acontece e afeta o fluxo (Início, Intermediário, Fim).
2.  **Atividades (Activities)** (Retângulo Arredondado): Trabalho a ser executado.
    - **Tarefas:** Atividade atômica (simples).
    - **Subprocessos:** Atividade não atômica, composta por outras atividades (indicado por `+`).
3.  **Decisões (Gateways)** (Losango): Controlam a divergência e convergência do fluxo.
    - **Exclusivo (X ou Losango Simples):** Apenas um caminho é seguido (OR).
    - **Paralelo (+):** Todos os caminhos são executados (AND).
    - **Inclusivo (O com Círculo):** Um **e/ou** mais caminhos podem ser seguidos, realiza sincronização de fluxos.

### 3.2. Objetos de Conexão (Connecting Objects)
Conectam os objetos de fluxo.
- **Fluxo de Sequência:** (Seta Contínua) Ordem do fluxo *dentro* de uma Piscina.
- **Fluxo de Mensagem:** (Seta Pontilhada com Círculo) Comunicação *entre* Piscinas/entidades.
- **Associação:** (Linha Pontilhada) Liga artefatos (dados/texto) aos objetos de fluxo.

### 3.3. Piscinas e Raias (Pools and Swimlanes)
Representam a organização visual das atividades em categorias visuais separadas.
- **Piscina (Pool):** Representa a organização ou entidade que contém o processo. Usada para dividir conjuntos de atividades de outras Piscinas (entidades externas);
- **Raia (Lane):** Subdivisão de uma Piscina, representando uma área organizacional, função ou papel (ex: departamento).

### 3.4. Artefatos (Artifacts)
Usados para adicionar informações adicionais.
- **Objetos de Dados:** Elementos produzidos ou requeridos por uma atividade (ex: formulários, relatórios).
- **Anotações:** Observações que agregam informações adicionais.
- **Grupo:** Agrupamento visual de atividades para documentação/análise (não afeta o fluxo)