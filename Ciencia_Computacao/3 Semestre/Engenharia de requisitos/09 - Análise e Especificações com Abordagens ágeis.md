---
tags:
  - Emprogresso
  - NaoRevisado
---
# Análise e Especificação de Requisitos: Modelagem UML e Abordagens Ágeis (SCRUM)

## 1. Abordagens Ágeis: O Framework SCRUM

O [[Scrum]] é um **framework leve** que ajuda a gerar valor por meio de soluções adaptativas para problemas complexos. É iterativo e incremental, baseado no empirismo e *lean thinking*.

### Pilares e Valores do Scrum
O Scrum se apoia em três pilares e cinco valores.

| Pilares | Definição | Valores |
| :--- | :--- | :--- |
| **Transparência** | Clareza sobre processos, requisitos de entrega e status. | Comprometimento, Coragem, Foco, Respeito, Abertura. |
| **Inspeção** | Constante avaliação de tudo o que está sendo feito. | |
| **Adaptação** | Ajuste do processo e do produto às mudanças. | |

### Papéis, Eventos e Artefatos (3-5-3)

| Papéis (Time Scrum) | Eventos (Cerimônias) | Artefatos (Requisitos) |
| :--- | :--- | :--- |
| **[[Product Owner (PO)]]** | **Sprint** (2 a 4 semanas, duração constante) . | **[[Backlog do Produto]]** (repositório de todos os requisitos) . |
| **[[Scrum Master (SM)]]** | **Planejamento da Sprint** (Max. 8h para Sprint de 4 sem.). | **Backlog da Sprint** (itens selecionados para o Incremento) . |
| **Desenvolvedores** (Time auto-gerenciado, multidisciplinar) . | **Reunião Diária** (Daily Scrum - 15 min.). | **Incremento** (item "Pronto" e potencialmente entregável) . |

>[!tip] Foco dos Artefatos
> - **Backlog do Produto:** Contém todos os requisitos (funcionais e não funcionais). É priorizado pelo PO e está em constante evolução.
> - **Backlog da Sprint:** O escopo **não deve ser alterado** durante a Sprint.
> - **Incremento:** Nasce quando um item atende à **[[Definição de Pronto (DoD)]]**.

## 2. Especificação Ágil: Histórias de Usuário

As Histórias de Usuário (User Stories) são a forma padrão de expressar requisitos em ambientes ágeis.

- **Conceito:** Representa uma funcionalidade ou característica do produto "narrada" pelo ponto de vista do usuário.

### Componentes de uma História de Usuário (3 C's)
1. **Cartão (*Card*):** A afirmação concisa que segue a "voz do usuário".
- **Formato:** Como um [**ator**], eu quero/preciso [**ação**] para [**funcionalidade / valor**].
2. **Conversação (*Conversation*):** A discussão verbal e colaborativa que ocorre durante o projeto, complementada por documentação.
3. **Confirmação (*Confirmation*):** Os **testes de aceitação** que serão usados para demonstrar que a história foi implementada corretamente.

### Critérios de Qualidade INVEST (Bill Wake)
Um acrônimo para lembrar as características de uma boa história:

- **I**ndependent: Não deve haver dependência entre as histórias.
- **N**egotiable: A essência é capturada, não os detalhes, permitindo flexibilidade.
- **V**aluable: Deve ter valor para o cliente.
- **E**stimable: Deve ser possível estimar o esforço.
- **S**mall: Boas histórias são pequenas, representando, no máximo, algumas semanas de trabalho.
- **T**estable: Boas histórias são testáveis, o que ajuda a clareza.

### Priorização de Itens (MoSCoW e Matriz)
O [[Product Owner (PO)]] prioriza o backlog. A prioridade de um item diminui conforme ele desce na lista (Baixa prioridade $\rightarrow$ Alto Nível).

1. **Matriz Benefício x Esforço/Custo:**
- **Alto Benefício / Baixo Esforço:** FAÇA JÁ.
- **Alto Benefício / Alto Esforço:** FAÇA.
- **Baixo Benefício / Baixo Esforço:** EVITE FAZER.
- **Baixo Benefício / Alto Esforço:** NÃO FAÇA.
2. **Técnica MoSCoW:** Must have, Should have, Could have, Will not have.

## 3. Técnicas Ágeis de Descoberta

Para descobrir e detalhar as funcionalidades do produto, são utilizadas técnicas focadas na perspectiva e experiência do usuário:

### Personas e Jornada do Usuário
- **[[Persona (Análise)]]:** Uma ideia fictícia do cliente ideal, criada com base em dados reais, que representa um segmento de usuário da solução.
- **Componentes:** Apelido/Nome, Perfil, Comportamentos e Necessidades/Dores.
- **[[Jornada do Usuário (Customer Journey)]]:** Descreve o percurso de um usuário por uma sequência de passos dados para alcançar um objetivo.
- **Elementos:** Ações realizadas, Emoções/Pensamentos, Dores/Ganhos e Pontos de Contato com o sistema (Canais).

### Mapa de Empatia
Representação visual que aprofunda o conhecimento sobre o usuário, organizando-o a partir de seis perguntas-chave:

- O que ele **PENSA E SENTE** (preocupações e aspirações).
- O que ele **VÊ** (ambiente, amigos, mercado).
- O que ele **ESCURA** (amigos, chefe, influenciadores).
- O que ele **FALA E FAZ** (atitude em público, comportamento).
- **FRAQUEZAS** (medos, frustrações).
- **GANHOS** (desejos e necessidades).

## 4. Especificação com Modelagem UML

A [[UML (Unified Modeling Language)]] é uma linguagem gráfica de modelagem utilizada para : visualizar, especificar, construir e documentar artefatos de sistemas complexos.

- **Princípio:** Um modelo é uma simplificação (representação) da realidade, usado para compreender melhor o sistema.

### A. Diagrama de Casos de Uso (UCD)
Principal modelo para a **visão funcional** (requisitos) do sistema.

- **Objetivo:** Descrever um modelo funcional do sistema, identificando os usuários e representando o sistema segundo a sua visão.
- **Ator:** Quem ou o que interage com o sistema. Representa um **papel**, não um usuário individual.
- **Caso de Uso:** Uma sequência de ações que o sistema executa, gerando um **resultado de valor** para um ator. Foca em **O QUE** o sistema faz, e não **COMO**.
- **Casos de Uso CRUD:** Funções semelhantes (Create, Read, Update, Delete) são geralmente combinadas em um caso de uso que ofereça todos os recursos de manutenção (Ex: UC Manter Usuário).
- **Relacionamentos:**
- **Generalização/Herança:** Atores ou Casos de Uso mais especializados herdam o comportamento de generalizados.
- **Inclusão (`<<include>>`):** Indica um comportamento **obrigatório** (rotina comum) que será executado pelo Caso de Uso base.
- **Extensão (`<<extend>>`):** Indica um comportamento **opcional** que só é inserido se uma condição for verdadeira.

### B. Especificação de Caso de Uso
É a **descrição narrativa textual** das interações, complementando o diagrama.

- **Fluxo Principal (Básico):** A descrição da sequência **usual** de passos e o caminho ideal.
- **Fluxos Alternativos:** Descrevem o que acontece quando o ator opta por um caminho diferente para alcançar o objetivo (Ex: Opções exclusivas).
- **Fluxos de Exceção:** Descrevem o que acontece quando algo **inesperado/inválido** ocorre, levando ao cancelamento ou retorno a um passo anterior.
- **Regras para Escrita:** Deve ser escrito do ponto de vista do usuário, usando sua terminologia e evitando jargões técnicos.

### C. Diagrama de Classes (DCD)
Principal artefato para a **visão estática e estrutural** do sistema.

- **Objetivo:** Visualizar as classes, seus **atributos** e **métodos**, e como se relacionam.
- **Modelo de Domínio:** Representa classes conceituais do mundo real (domínio do problema), não componentes de software.
- **Modelo de Análise:** Representação dos componentes de software, acrescentando classes específicas da solução (domínio da solução), contendo atributos e métodos de todas as classes.

#### Composição da Classe
Uma classe tem três compartimentos: Nome, Atributos (Propriedades) e Métodos (Operações).

- **Atributos (Propriedades):**
- **Visibilidade:** `+` (Público), `-` (Privado), `#` (Protegido), `~` (Pacote).
- **Estático (Sublinhado):** O valor é comum a todos os objetos da classe.
- **Métodos (Operações):**
- **Notação:** Visibilidade + Nome (Lista de Parâmetros) : Tipo de Retorno {Restrições}.

#### Relacionamentos
- **Associação:** Vínculo estrutural entre classes para troca de informações. Inclui navegabilidade ($\rightarrow$) e multiplicidade (`1..*`, `0..1`).
- **Agregação (Losango vazio):** Relacionamento todo-parte, onde a **parte pode existir sem o todo**.
- **Composição (Losango preenchido):** Vínculo **mais forte** (exclusivo). Se o todo é destruído, a parte também o é.
- **Generalização (Herança):** Relação de especialização/generalização. Elementos especializados (filhos) herdam do elemento generalizado (pai).
- **Realização:** Um classificador especifica um contrato que outro classificador garante executar (Ex: Classe implementa uma Interface).