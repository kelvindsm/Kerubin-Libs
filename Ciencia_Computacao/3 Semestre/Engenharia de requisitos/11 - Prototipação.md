---
tags:
  - EngRequisitos
  - NaoRevisado
---
# Engenharia de Requisitos - Prototipação

## Introdução: Conceitos Fundamentais

### Layout
Um **Layout** é um esboço ou rascunho que mostra a **estrutura física** de uma página (jornal, revista ou internet).

- Engloba a forma como elementos como **texto, gráficos e imagens** se encontram em um determinado espaço.
- O layout gráfico pressupõe o trabalho de um designer gráfico.

### Grid
O **Grid** é um sistema de regras estabelecidas para a **divisão de espaço**, incluindo padrões como a divisão áurea.
- **Organiza** um conteúdo específico em relação ao espaço que irá ocupar.
- Permite ao designer criar diferentes layouts sem fugir da estrutura predeterminada.
- **Atenção**: O Grid não limita o Layout.

### Wireframe
O **Wireframe** é um guia visual que representa a **estrutura da página**, sua Hierarquia e os principais elementos. É um desenho básico, uma planta baixa ou um esqueleto.

- Demonstra a **arquitetura** do site, sistema ou aplicativo e como a interface final será de acordo com as especificações.
- É útil para discutir ideias com a equipe e clientes, e para informar o trabalho de diretores de arte e desenvolvedores.
- **Fase Crítica**: O escopo, validação de ideia e requisitos devem ser feitos nesta fase junto ao cliente.
#### Categorias de Wireframes (Fidelidade)
Existem 3 categorias de Wireframes:
- Wireframes de **baixa fidelidade**
- Wireframes de **média fidelidade**
- Wireframes de **alta fidelidade**

## O Protótipo e a Prototipação

>[!quote] O que é um Protótipo
> Um protótipo é uma **versão das ideias de projeto** com o intuito de materializar a visão e permitir **testes** anteriores à realização do produto.

- É o primeiro tipo criado, o original.
- Em engenharia, é um **modelo em menor escala** de um produto (carro, prédio, etc.).
- Exemplos no Design de Interação:
    - Uma série de **esboços em papel** construídos à mão livre.
    - Um conjunto de **storyboards**.
    - Uma apresentação (PowerPoint, etc.).
    - Uma interface do sistema desenhada para validação.
    - Um vídeo simulando o uso de um sistema.
    - Interface produzida em alta fidelidade com ferramentas de prototipação.

### Prototipação de Software
>[!info] Definição
> - É a atividade de criar **versões incompletas** do programa de software em desenvolvimento.
> - Seu objetivo é permitir que os usuários **avaliem as propostas** de design e testem-nas, em vez de apenas interpretar descrições.
> - Pode descrever e comprovar **requisitos que não foram considerados**.

#### Vantagens da Prototipação de Software
- Promove a **interação com os clientes**.
- Permite a **avaliação**.
- Facilita a **coleta de requisitos**.
- Reduz **custos e tempo**.

### Por que fazer Protótipos
- Facilitam a **comunicação** e a formação de ideias.
- Permitem opiniões sobre o design da interação de forma **fácil e imediata**.
- **Stakeholders** se envolvem ao ver, tocar e interagir.
- Permite ensaiar **várias ideias alternativas** sem incorrer em custos altos.
- Falhas (*gaps*) são identificadas rapidamente.
- Auxilia a percepção do usuário (validação de requisitos).
- Oferecem flexibilidade, rapidez e feedback.

## Níveis de Fidelidade dos Protótipos

Os níveis de fidelidade são definidos pelo grau de detalhamento dos protótipos, classificando sua proximidade com a solução final.

### Baixa Fidelidade
- Protótipo não possui **características dinâmicas** (ex: esboço, maquete).
- **Vantagens**:
    - Pouco tempo para construir.
    - Permitem que o projetista e o usuário reconstruam partes facilmente.
    - Transmite a impressão de ser **descartável** (sugestões podem ser acatadas sem comprometer o cronograma).
    - É de fato descartável (o desenvolvedor não se prende à solução).
- **Exemplos**: Esboços (Sketch), Storyboards, Cartões (*Post-it*), Mágico de Oz, Mockups.
#### Tipos de Baixa Fidelidade
1.  **Sketches (Esboços)**: Forma rápida de rabiscar uma nova interface usando papel e caneta. Úteis para validar rapidamente conceitos.
2.  **Storyboards**: Acrescenta-se a **dinâmica de navegação** e o fluxo de telas.
3.  **Cartões**: Elementos padronizados e **fáceis de manipular** durante os testes.
4.  **Mágico de Oz (Wizard of Oz)**:
    - O usuário pensa que manipula o sistema, mas na verdade é uma **pessoa que responde às interações**.
    - Bom para testar interações de **linguagem natural**.
5.  **Vídeo Conceitual**: Apresenta um conceito como se fosse um produto real. Objetivo é comunicar a **visão do produto** aos stakeholders.

### Média Fidelidade
- Exemplos: **Slide shows**.

### Alta Fidelidade
- A interface de usuário **pode ser executada**, mas a funcionalidade da aplicação **não está totalmente implementada**.
- Exemplos: Protótipos funcionais, Wireframes clicáveis ou layouts que simulam a navegação.

## Dimensão e Abrangência da Prototipação

### Dimensões
1.  **Representação**: Diagramas, Interfaces, Descrição Textual.
2.  **Escopo**: Interfaces, Componentes Computacionais.
3.  **Executabilidade**: Protótipo Executável.
4.  **Maturidade**: Revolucionário (descartável) ou Evolucionário (incremental).

### Tipos de Abrangência (Escopo)

| Tipo de Protótipo | Corte (Abrangência) | Características |
| :--- | :--- | :--- |
| **Protótipo Horizontal** | Corte nas **funcionalidades** | Inclui a interface de usuário (IU) para todo o sistema, mas **sem funcionalidade por baixo**. Permite testar toda a interface e avaliar como ela se encaixa no todo. É uma simulação do sistema. |
| **Protótipo Vertical** | Corte nas **tarefas** | Muita funcionalidade para **poucas tarefas**. Permite testar apenas uma pequena parte do sistema completo. |

### Maturidade: Evolutivo vs. Descartável

#### Descartável (Revolucionário)
- Envolve a criação de um modelo de trabalho em uma fase muito **precoce** e com investigação curta.
- É bastante **informal**, priorizando a **velocidade**.
- O protótipo é **descartado no final**.
- Não reaproveita o esforço (custo e tempo) de criação.
- Geralmente possui **baixo custo** e é mais rápido de criar.
#### Evolutivo (Incremental)
- O protótipo é mais **robusto** e é o coração do novo sistema, sendo continuamente **refinado e reconstruído**.
- Permite que a equipe adicione recursos ou faça alterações não concebidas na fase de requisitos.
- É evoluído até virar o **produto final**.
- O esforço de criação é **aproveitado** no produto final.
- Necessita de **mais investimento e esforço** de criação, pois deve apresentar funcionalidades básicas.
---