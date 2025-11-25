---
tags:
  - Naoconcluido
---

# Modelagem de Requisitos com UML e Especificação de Casos de Uso

## 1. Unified Modeling Language (UML)

### 1.1. Fundamentos e Propósito
- **Definição:** A [[UML (Unified Modeling Language)|UML]] é uma **Linguagem Gráfica de Modelagem** padrão (OMG) utilizada para **visualizar, especificar, construir, documentar** e **comunicar** artefatos de sistemas complexos. Não é um processo ou metodologia, mas uma ferramenta de apoio.
- **Histórico:** A UML surgiu da unificação dos principais métodos orientados a objetos (OO) da década de 90, notadamente os de **Grady Booch**, **James Rumbaugh (OMT)** e **Ivar Jacobson (OOSE)**.
- **Modelo:** É uma representação simplificada da realidade, que ajuda a compreender e comunicar o sistema. Modelamos as dimensões de **dados, função** e **comportamento**.

### 1.2. Elementos de Construção da UML
A UML é baseada em três pilares:
1.  **Blocos de Construção (Things):**
    - **Itens Estruturais:** Representam elementos conceituais (Classes, Interfaces) ou físicos (Componentes, Nodos).
    - **Itens Comportamentais:** Representam o lado dinâmico (Interações, Máquinas de Estado).
    - **Itens de Agrupamento:** Usados para organizar o modelo (Pacotes).
    - **Itens Anotacionais:** Comentários e observações.
2.  **Regras da UML:** Definem o que é um modelo **bem-formado**, estabelecendo regras de: nome, escopo, visibilidade, integridade e execução.
3.  **Mecanismos Básicos:**
    - **Especificações:** Descrições detalhadas dos blocos de construção.
    - **Adornos:** Informações textuais ou gráficas adicionais.
    - **Mecanismos de Extensão:** Permitem estender a linguagem para domínios específicos: **Stereotype** (definição de um novo tipo), **Tagged Value** (propriedade adicional) e **Constraint** (regra de coerência).

### 1.3. Visões e Diagramas
Os diagramas UML são agrupados em **Visões** que definem o foco da análise ou projeto:

| Visão | Foco Principal | Categoria de Diagrama |
| :--- | :--- | :--- |
| **Caso de Uso** | Requisitos Funcionais, Escopo e Fronteira do Sistema | Comportamental |
| **Projeto** | Estrutura lógica (Classes, Pacotes) | Estrutural |
| **Interação** | Fluxo de controle, Ordem das Operações (Tempo) | Comportamental (Dinâmico) |
| **Implementação** | Configuração, Componentes, Módulos | Estrutural |
| **Implantação** | Topologia física, Distribuição (Nós, Processos) | Estrutural |

- **Diagramas Estruturais (Estáticos):** Classes, Componentes, Implantação.
- **Diagramas Comportamentais (Dinâmicos):** Caso de Uso, Atividades, Máquina de Estados, Sequência.

## 2. Diagrama de Casos de Uso (UCD)

### 2.1. Conceitos Fundamentais
- **Objetivo:** Capturar os [[Requisitos Funcionais]] do sistema do ponto de vista do usuário/ator. É o primeiro diagrama a ser construído, definindo a **fronteira** do sistema.
- **Ator:** Representa um **papel** (e não uma pessoa específica) que interage com o sistema para atingir uma meta. Pode ser um usuário, um hardware ou um sistema externo.
    - **Ator Primário:** Aquele que inicia o Caso de Uso.
    - **Ator Secundário:** Aquele com o qual o sistema interage para cumprir o Caso de Uso.
- **Caso de Uso (UC):** Uma funcionalidade completa que gera um **resultado observável de valor** para o ator. O nome deve ser uma **frase verbal** (Ex: *Realizar Login*, *Cadastrar Cliente*).

### 2.2. Relacionamentos Entre Casos de Uso
| Relacionamento | Notação | Direção | Significado | Finalidade |
| :--- | :--- | :--- | :--- | :--- |
| **Inclusão** (`<<include>>`) | Seta tracejada | Base $\rightarrow$ Incluído | **Obrigatório/Comum** (Rotina compartilhada) | Reuso de funcionalidades e estruturação. |
| **Extensão** (`<<extend>>`) | Seta tracejada | Estensor $\rightarrow$ Base | **Opcional/Condicional** (Comportamento extra) | Modularização de funcionalidades menos frequentes. |
| **Generalização** | Seta com triângulo vazio | Especializado $\rightarrow$ Geral | **Herança/Especialização** (É um tipo de) | Reutilização e organização de funcionalidades similares. |

## 3. Especificação de Caso de Uso (Narrativa)

- **Objetivo:** Detalhar a interação entre o ator e o sistema para cada Caso de Uso, descrevendo a funcionalidade de forma **textual e verificável**. A narrativa serve como base para [[Casos de Teste]].
- **Princípio:** Deve ser escrita do ponto de vista do **usuário** e usando a **terminologia do negócio** (cliente).

### Componentes Chave da Especificação
| Componente | Propósito | Exemplo |
| :--- | :--- | :--- |
| **Pré-condições** | O estado do sistema antes do caso de uso iniciar (deve ser verdadeiro). | O Atendente deve estar autenticado no sistema. |
| **Pós-condições** | O estado final do sistema após a conclusão bem-sucedida (deve ser verdadeiro). | A conta do cliente foi atualizada no banco de dados. |
| **Fluxo Principal** | A sequência de passos **ideal e sem erros** que atinge o objetivo do ator. | 1. O Ator clica em 'Cadastrar'. 2. O Sistema exibe o formulário. |
| **Fluxo Alternativo** | Sequências de passos que se desviam do fluxo principal, mas **ainda levam ao sucesso** (Ex: "Ator altera um dado e retorna"). | O Ator cancela o cadastro (e o UC é encerrado). |
| **Fluxo de Exceção** | Sequências que descrevem erros ou falhas **inesperadas** que **impedem o sucesso** do objetivo (Ex: Falha de comunicação, dado inválido). | CPF já cadastrado (retorna ao passo 3). |

## 4. Diagrama de Classes

### 4.1. Estrutura da Classe (Modelo Estático)
- **Objetivo:** Mostrar a estrutura **estática** (classes, atributos, métodos) e os relacionamentos do sistema.
- **Persistência:** O Diagrama de Classes pode incluir classes persistentes (que virarão tabelas no banco de dados) e classes temporárias (Ex: classes de controle ou interface).

| Componente | Notação | Descrição |
| :--- | :--- | :--- |
| **Visibilidade** | `+` (Público), `#` (Protegido), `-` (Privado), `~` (Pacote) | Define o acesso a atributos e métodos. |
| **Atributo Estático** | Sublinhado (`_`) | Valor pertencente à classe, comum a todas as instâncias (objetos).
| **Atributos** | `visibilidade nome: tipo [multiplicidade] = valor default {restrições}` | Representa as propriedades da classe (o **"o que é"**). |
| **Métodos** | `visibilidade nome(parâmetros): tipo de retorno` | Representa as ações que a classe pode realizar (o **"o que faz"**). |

### 4.2. Relacionamentos Estruturais
- **Associação:** Vínculo estrutural mais geral entre classes.
    - **Multiplicidade:** Indicada em cada extremidade da associação, definindo o número de objetos envolvidos (Ex: `1`, `*` - zero ou mais, `1..*` - um ou mais, `0..1` - zero ou um).

- **Agregação (Todo-Parte Fraca):**
    - **Notação:** Losango **vazado** no lado da classe "Todo".
    - **Significado:** A parte pode existir **independentemente** do todo. (Ex: Um *Aluno* pertence a uma *Turma*, mas o aluno pode existir sem a turma).

- **Composição (Todo-Parte Forte/Exclusivo):**
    - **Notação:** Losango **preenchido** no lado da classe "Todo".
    - **Significado:** A parte **não pode existir** se o todo for destruído (forte dependência do ciclo de vida). (Ex: Um *Departamento* pertence a uma *Empresa*; se a empresa é destruída, o departamento também é).

- **Generalização (Herança):**
    - **Notação:** Seta com triângulo vazio apontando para a **Superclasse** (Classe Pai).
    - **Significado:** Relacionamento "é um" (Ex: *Pessoa Física* **é uma** *Pessoa*). A subclasse herda características da superclasse.

- **Outros Relacionamentos:**
    - **Dependência:** Uma classe usa a outra (temporariamente) como argumento de método ou variável local.
    - **Realização:** Uma classe implementa um **contrato** (métodos) de uma [[Interface]].