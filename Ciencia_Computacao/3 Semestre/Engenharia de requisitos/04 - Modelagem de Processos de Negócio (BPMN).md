---
tags:
  - Concluido
---
# Modelagem de Processos de Negócio: Hierarquia e Notação BPMN
## Introdução à Modelagem de Processos
>[!quote] Conceito de modelagem de processos
> - A **Modelagem de Processos de Negócio** é o conjunto de atividades envolvidas na criação de representações de processos de negócio existentes (*As Is*) ou propostos (*To Be*). 
> - Ela visa prover uma perspectiva **ponta a ponta** ou de porções específicas (primários, de suporte ou de gerenciamento).

**Propósito da Modelagem:**
 - Criar uma representação do processo de maneira **completa e precisa** sobre seu funcionamento.
- **Permite expressar processos em vários níveis de detalhe**, desde uma visão contextual abstrata até uma visão detalhada.
### O que é um Modelo?
>[!quote] Definição
>- Um **modelo** é uma representação simplificada de uma coisa, um conceito ou uma atividade. Pode ser matemático, gráfico, físico, narrativo ou uma combinação desses tipos.

- **Utilidades em Negócios:** Organização, Descoberta (aprendizagem), Previsão (estimativas), Explicação (ensino), Verificação (validação) e Controle (restrições, objetivos).
- **Conteúdo do Modelo de Processos:** Inclui ícones que representam atividades, eventos, decisões, condições e outros elementos.

---
## Diagrama x Mapa x Modelo de Processos
- Diagramas, mapas e modelos são utilizados de formas complementares, representando diferentes estágios de desenvolvimento, cada qual agregando mais informações e utilidade.

| Tipo de Representação | Nível de Detalhe        | Propósito e Características                                                                                                                                           |
| :-------------------- | :---------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Diagrama**          | Visão macro/superficial | Retrata elementos principais, omite detalhes menores. Entendimento rápido das principais atividades do processo.                                                      |
| **Mapa**              | Visão abrangente        | Maior precisão e detalhe do que o diagrama. Agrega informações sobre atores, eventos e resultados (Ex: usa **Raias** para responsabilidades).                         |
| **Modelo**            | Mais detalhado/completo | Representação completa e precisa de um determinado estado do negócio (atual ou futuro) e dos respectivos recursos envolvidos (pessoas, informação, automação, tempo). |

>[!tip] Alerta sobre Modelagem Detalhada
> - Se você não deseja **automatizar**, não faça um **modelo** do processo.
> - Devido ao nível muito detalhado, o modelo tende a ficar desatualizado rapidamente.
> - **Vantagem do Modelo:** Capacidade de **simulação** manual ou automatizada do processo, gerando informações úteis sobre o desempenho.

| Diagrama ou Mapa de Processo                   | Modelo de Processos                                                    |
| :--------------------------------------------- | :--------------------------------------------------------------------- |
| Notação ambígua e baixa precisão               | **Convenção padronizada** e precisão tão precisa quanto necessária     |
| Ícones "inventados" ou vagamente definidos     | Ícones **objetivamente definidos e padronizados**                      |
| Não é adequado para importação por um **BPMS** | **Pode ser importado por um BPMS** (Business Process Management Suite) |

---
## Notações de Modelagem de Processos

>[!quote] Definição
>- **Notação** é um conjunto padronizado de símbolos e regras que determinam o significado desses símbolos, permitindo a comunicação padronizada.
>	- **Vantagens de Notações Padrão:** Consistência, importação e exportação de modelos entre ferramentas, e geração de aplicações a partir de modelos.
### Principais Notações

| Notação                                            | Descrição                                                                                                                                                                       |
| :------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **[[BPMN (Business Process Model and Notation)]]** | Padrão criado pelo Object Management Group (**OMG**). Útil para apresentar modelos para públicos diferentes, possibilita simulação e automação.                                 |
| **Fluxograma**                                     | Padrão ANSI (simples e limitado). Facilita entendimento rápido do fluxo. Usado para capturar fluxos rapidamente onde os detalhes não são críticos.                              |
| **[[UML (Unified Modeling Language)]]**            | Padrão do OMG. Conjunto de notações técnicas orientado à descrição de **Requisitos de Sistemas de Informação**. Diagramas de Atividades UML podem modelar processos de negócio. |
| **EPC (Event-driven Process Chain)**               | Desenvolvido como parte da estrutura ARIS. Útil para modelar conjuntos complexos de processos, usando eventos como "gatilhos".                                                  |
| **SIPOC**                                          | Usado em Lean Six Sigma. Enfatiza as fontes de entradas (Supplier) e o alvo das saídas (Customer).                                                                              |
## BPMN: Business Process Model and Notation
>[!info] Sobre BPNM
>O **[[BPMN (Business Process Model and Notation)|BPMN]]** é a mais poderosa e atual notação para modelar processos de negócio. É um padrão aberto mantido pelo OMG.
### Vantagens Chave do BPMN
- **Padrão e Comunicação:** Uso e entendimento difundido. Reduz a distância de entendimento entre a área de **Negócios** e a **Tecnologia** (TI).
- **Flexibilidade:** Versatilidade para modelar diversas situações e pode evoluir de elementos básicos (fluxograma) para complexos.
- **Automação:** Suportado por **ferramentas BPMS** , com possibilidade de interpretação do modelo e geração de código de sistemas.
### Componentes de um Diagrama BPMN (4 Categorias)
O Diagrama de Processos de Negócio em BPMN é composto por quatro categorias básicas de elementos:
#### 1. Objetos de Fluxo (Flow Objects)
Elementos principais que definem o comportamento do processo.

- **Atividades (Activity):** Passos lógicos, termo genérico para trabalho executado. Podem ser:
	- **Tarefa (Task):** Atômica. Ex: *User Task* (usuário com sistema), *Service Task* (automática), *Manual Task*, *Script Task*.
	- **Subprocesso:** Não atômica, composta por uma série de outras atividades. Distinguido por uma pequena cruz no centro inferior.
	- **Modos de Execução:** Normal, Sequencial (em *loop*), ou Em Paralelo (múltiplas instâncias).
	![[Pasted image 20251127131244.png|center|350]]
- **Eventos (Event):** Algo que acontece ou pode acontecer em um processo. Afetam o fluxo e têm uma causa (*trigger*) ou um impacto (*result*).
	- **Início:** Círculo simples. Indica onde o processo/subprocesso se inicia. Ex: Timer (ciclo de tempo ou data específica), Mensagem (recebida).
	![[Pasted image 20251127140046.png|center|350]]
	- **Intermediário:** Círculo duplo. Usado para expressar esperas ou tratar *timeouts*.
	![[Pasted image 20251127140234.png|center|350]]
	- **Fim:** Círculo mais forte (hachurado).
	 ![[Pasted image 20251127140327.png|center|350]]
- **Decisões (Gateway):** Controlam o fluxo de sequência (divergência e convergência).
	![[Pasted image 20251127140424.png|center|350]]
- **Exclusivo (X ou Diamante Vazio):** Apenas **um** caminho é seguido, com base em uma condição a ser testada.
- **Paralelo (+):** Divide o fluxo em caminhos paralelos. Semanticamente funciona como um **"e (AND)**, onde **todos** os caminhos são executados.
- **Inclusivo (O com marcador):** **Um e/ou mais** caminhos são seguidos. Semanticamente funciona como **"e/ou"**, e realiza a sincronização dos fluxos.
- **Complexo (*):** Usado para modelar sincronização complexa quando nenhuma outra combinação de *gateways* é suficiente.

#### 2. Objetos de Conexão (Connecting Objects)
Representam a forma como os objetos de fluxo se conectam.
- **Fluxo de Sequência (Seta contínua):** Representa a **ordem do fluxo** dentro de uma mesma Piscina (Pool). O tempo (e dependência) é no sentido esquerda para direita.
- **Fluxo de Mensagem (Seta pontilhada):** Troca de mensagens entre **diferentes Piscina (Pool)s** (entidades/participantes).
- **Associação (Linha pontilhada):** Liga artefatos (dados, textos) aos objetos do fluxo para documentação.
#### 3. Piscina e Raias (Pool and Swimlanes)
Forma de organização das atividades em categorias visuais separadas.
- **Piscina (Pool):** Representa a **organização em si** ou uma entidade responsável (participante). Atua como um contêiner, separando um conjunto de atividades de outras piscinas.
- **Raia (Lane):** Subdivisão de uma **Piscina**. Representa uma **função, departamento** ou um papel desempenhado por colaboradores.
- **Fase ou Milestone (Subdivisão horizontal):** Usado para indicar fases do processo ou períodos de tempo.
#### 4. Artefatos (Artifacts)
Usados para colocar informações adicionais no processo (documentação).
- **Objetos de Dados (Data Object):** Elementos produzidos ou requeridos por uma atividade (formulários, documentos, bases de dados).
- **Anotações:** Observações que agregam informações relevantes para o entendimento do processo.
- **Grupo:** Forma visual de agrupar atividades para documentação ou análise, sem afetar o fluxo.
---