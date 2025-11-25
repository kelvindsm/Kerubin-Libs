---
tags:
  - Naoconcluido
---
# Síntese Detalhada da Aula 09: Análise e Especificações com Abordagens Ágeis

## 1. Introdução ao Framework SCRUM e Abordagens Ágeis

### 1.1. Frameworks Ágeis
O movimento ágil engloba diversos *frameworks* e metodologias.
* **Exemplos Notáveis:** **[[Scrum]], [[XP]] (Extreme Programming), [[Kanban]],[[ Lean]], DSDM, Crystal, FDD, [[ScrumBan]] e AUP.**
* **[[Scrum]]:** É um *framework* **leve**, iterativo e incremental, projetado para ajudar pessoas e times a gerar valor por meio de soluções adaptativas para problemas complexos. É baseado no **empirismo** e **[[Lean Thinking]]** (foco em minimizar desperdícios).

### 1.2. Pilares do Scrum (Empirismo)
O Scrum baseia-se no controle empírico de processo, que exige três pilares para gerenciar o risco e a adaptação:
1.  **Transparência:** Os processos, os requisitos de entrega e o status do projeto devem ser claros e visíveis para todos os envolvidos (*stakeholders* e equipe).
2.  **Inspeção:** Os artefatos e o progresso do trabalho devem ser inspecionados frequentemente e diligentemente para detectar variações indesejadas.
3.  **Adaptação:** Se uma inspeção revela que algo está fora dos limites aceitáveis, o processo ou o produto deve ser ajustado o mais rápido possível.

### 1.3. Valores do Scrum
Os cinco valores centrais do Scrum são: **Comprometimento, Foco, Abertura, Respeito e Coragem.**

## 2. Artefatos de Requisitos no Scrum

### 2.1. Product Backlog (PB)
O *Product Backlog* é o artefato central de requisitos.
* **Definição:** É a **única fonte** de trabalho para o Time Scrum. É uma lista **ordenada** de tudo que é conhecido como necessário no produto, sendo **emergente** por natureza (está em constante evolução).
* **Responsabilidade:** O **Product Owner (PO)** é o único responsável pelo gerenciamento do PB, decidindo o que entra e qual é a ordem de prioridade.
* **Características DEEP do Product Backlog:**
    * **D**etalhado (*Appropriately*): Detalhado o suficiente apenas para os itens que serão trabalhados em breve.
    * **E**stimado: Deve ter uma estimativa de esforço.
    * **E**mergente: Nunca está completo; novos itens surgem e antigos são removidos ou refinados.
    * **P**riorizado (*Ordered*): Deve ser ordenado com base no valor de negócio, risco ou dependência.

### 2.2. Histórias de Usuário (User Stories - HU)
As Histórias de Usuário são a forma mais comum de descrever os itens do Product Backlog.
* **Definição:** Uma descrição curta e simples de uma funcionalidade, contada da perspectiva do usuário, focada no **valor** a ser entregue.
* **Formato Padrão:** **"Como um `<Tipo de Usuário>`, eu quero `<algum objetivo/ação>` para que eu possa `<algum benefício/valor>`."**
* **Critérios de Qualidade (INVEST):**
    * **I**ndependente: Deve ser implementada sozinha, sem dependências.
    * **N**egociável: Deve estimular a conversa e o refinamento, não ser um contrato rígido.
    * **V**aliosa: Deve entregar valor real para o usuário/cliente.
    * **E**stimável: O esforço de implementação deve ser mensurável.
    * **P**equena (*Small*): Deve ser pequena o suficiente para caber em uma iteração (*Sprint*).
    * **T**estável: Deve ser possível criar Critérios de Aceitação claros para validá-la.

### 2.3. Mínimo Produto Viável (MVP)
* **Definição:** É a versão mais simples de um produto que pode ser entregue para um público inicial, com o objetivo de **validar hipóteses** de negócio e aprender.
* **Natureza:** O MVP não é um produto mal-acabado, mas sim um **processo** que emprega o mínimo de recursos (tempo e dinheiro) para entregar a **principal proposta de valor** da ideia.
* **Propósito:** Maximizar o aprendizado e "falhar cedo para aprender rápido". É o primeiro ciclo do *Build-Measure-Learn*.

## 3. Técnicas de Descoberta de Requisitos Ágeis

### 3.1. Persona
* **Definição:** Uma descrição de uma pessoa **fictícia** que representa um segmento de usuário ideal da solução. É criada com base em dados reais do público-alvo.
* **Objetivo:** Focar o design, a experiência do usuário e as funcionalidades nas necessidades do usuário principal, garantindo que o produto atenda a um propósito claro.
* **Componentes:** Inclui perfil demográfico (Nome, Idade, Profissão), dados comportamentais (Personalidade, Marcas que consome) e o foco da ER: **Necessidades, Dores/Frustrações e Objetivos** (o que o motiva).

### 3.2. Mapa de Empatia
* **Objetivo:** Aprofundar o entendimento da Persona, visualizando a perspectiva do usuário, o seu contexto e suas motivações profundas.
* **Estrutura:**
    * **Pensa/Sente:** O que realmente importa para a Persona.
    * **Vê:** O que ela observa no ambiente.
    * **Diz/Faz:** O que ela fala e como age.
    * **Ouve:** O que ela escuta de amigos e influenciadores.
    * **Dores:** Os obstáculos, medos e frustrações que ela enfrenta.
    * **Ganhos:** Os objetivos, sucesso e desejos.

### 3.3. Jornada do Usuário (User Journey Map)
* **Definição:** Uma representação visual da experiência do usuário em uma sequência de passos para atingir um objetivo específico no sistema.
* **Propósito:** Entender as interações do usuário em todas as etapas, mapeando os **Pontos de Dor** e identificando **Oportunidades** para novas funcionalidades.
* **Eixos de Análise:** O que o usuário *faz* (ação), o que ele *pensa* (cognitivo) e o que ele *sente* (emocional) em cada etapa da jornada.

## 4. Descoberta e Priorização de Funcionalidades

### 4.1. Funcionalidades
* **Definição:** É a descrição de uma ação ou interação de um usuário com o produto.
* **Descoberta:** As funcionalidades devem ser descobertas através de *brainstorming* e devem ser alinhadas com os objetivos, as Personas e as Jornadas mapeadas.

### 4.2. Priorização de Funcionalidades
A priorização é um desafio, pois a tendência é considerar todos os requisitos como "importantes".
* **Técnica de Comparação:** A forma mais eficaz de priorizar é forçar a escolha através da comparação: **"Qual dessas duas funcionalidades é prioritária?"** (e não "Essa funcionalidade é importante?").
* **Hierarquia de Priorização:** A priorização deve seguir uma ordem lógica:
    1.  Qual o usuário (Persona) mais importante?
    2.  Qual a jornada de usuário mais importante para esse usuário?
    3.  Quais funcionalidades são mais importantes para viabilizar aquela jornada?