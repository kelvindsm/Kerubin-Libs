# Modelos de Processos de Desenvolvimento de Software
## Processo de Software

>[!quote] Definição
> - É a aplicação de uma abordagem **sistemática, disciplinada e possível de ser medida** para o **desenvolvimento, operação e manutenção** do software.
> - Abrange um conjunto de três elementos fundamentais: **Métodos**, **Ferramentas** e **Procedimentos** para projetar, construir e manter grandes sistemas de software de forma profissional.
### Elementos Fundamentais ^[[01 - Conceitos fundamentais de engenharia de software]]
- **Métodos**: Fornecem os detalhes sobre como fazer para construir o software.
    - Incluem: Planejamento e estimativa de projeto, análise de requisitos, projeto da estrutura de dados, algoritmos de processamento, codificação, teste e manutenção.
- **Ferramentas**: Dão **suporte automatizado** aos métodos.
	- Existem ferramentas para sustentar cada método;
    - Quando integradas, estabelecem um sistema de suporte chamado **[[CASE]]** (**C**omputer **A**ided **S**oftware **E**ngineering).
- **Procedimetnos**: Constituem o elo de ligação entre os métodos e as ferramentas.
    - Determinam a sequência dos métodos, os produtos a serem entregues, controles de qualidade e marcos de referência para administrar o progresso.
---
## Qualidade do Processo de Software
>[!quote]
> - A qualidade do processo está relacionada à extensão na qual um processo é **eficiente**, explicitamente **definido, gerenciado, medido e controlado**.
> - Também **implica em um potencial para crescimento** na capacidade do processo de software e a **consistência com qual ele é aplicado em projetos** por toda a organização.
### Atributos de Qualidade (Sommerville)
- **Inteligibilidade**: O processo é definido e **inteligível**.
- **Visibilidade**: O progresso do processo é **visível externamente**.
- **Suportabilidade**: Pode ser apoiado por **ferramentas [[CASE]]**.
- **Aceitabilidade**: É aceito por **todos envolvidos** nele.
- **Confiabilidade**: Os erros são descobertos **antes que resultem em erros no produto**.
- **Robustez**: Pode continuar apesar de **problemas inesperados**.
- **Manutenibilidade**: Pode **evoluir** para atender alterações de necessidades organizacionais.
- **Velocidade**: Quão rápido o sistema pode ser produzido.
---
## Fases Genéricas dos Processos
Modelos de processo de software, independentemente da aplicação, possuem três fases principais: **Definição, Desenvolvimento e Manutenção**, complementadas por **Atividades de Apoio**.
>[!note] Significado de alguns termos
> - Especificação: estabelecer os requisitos e restrições do sistema;
> - Projeto: produzir um modelo documentado do sistema;
> - Implementação: construir o sistema;
> - Teste: verificar se o sistema atende às especificações requeridas
> - Instalação (implantação): liiberar o sistema para o cliente e garantir que se torne operacional;
> - Manutenção: eliminar defeitos e evoluir o sistema conforme a demanda.
### 1. Fase de DEFINIÇÃO 
**Focaliza "O QUÊ" será desenvolvido.**
Busca estabelecer os requisitos e restrições do sistema:
- Que informação será processada.
- Que função e desempenho são desejados.
- Que interfaces e restrições de projeto existem.
- Que critérios de validação são exigidos.
### 2. Fase de DESENVOLVIMENTO
**Focaliza como o software será desenvolvido.**
- Como os dados serão estruturados.
- Como a função será implementada na arquitetura.
- Como os testes serão efetuados.
### 3. Fase de MANUTENÇÃO
**Focaliza mudanças do software.**
Ocorre depois que o software é liberado para uso operacional. Reaplica os passos de definição e desenvolvimento, mas no contexto de um software existente.
- **Mudanças associadas a:**
    - Correção de erros/defeitos.
    - Adaptações (ambiente evolui).
    - Aperfeiçoamentos (funções adicionais).
    - Modificações preventivas (evitar erros futuros).
### Atividades de APOIO
São aplicadas **durante toda a engenharia do software**.
- **Controle e Acompanhamento do Projeto** de Software.
- Revisões Técnicas Formais.
- **Garantia de Qualidade** de Software.
- **Gestão de Configuração** de Software.
- Gestão de reutilização e Medições.
- Gestão de risco.
---
## Modelos de Processo de Software
São paradigmas que tentam colocar ordem na atividade de desenvolvimento.
### [[Modelos Clássicos]]
#### Modelo Cascata (Sequencial Linear)
- Divide o desenvolvimento em **etapas sequenciais**.
- Cada fase deve ser **concluída** antes que a próxima possa começar.
- **Fases:** Requisitos, Design, Implementação, Teste e Manutenção.
#### Modelo em V
- É uma **extensão do Modelo Cascata**.
- Enfatiza a **validação e verificação** em cada fase do desenvolvimento.
- As atividades de teste avançam conforme as fases de desenvolvimento progridem, criando a forma de 'V'.
### Modelos Iterativos e Incrementais
#### [[Modelo Incremental]]
- Divide o projeto em **incrementos (partes menores)**, onde cada incremento é uma **versão funcional do sistema**.
- Cada incremento adiciona funcionalidades e aprimora os anteriores.
- É **iterativo** por natureza e permite entregas mais cedo.
#### [[Modelo Espiral]]
- Modelo **iterativo** que enfatiza a **avaliação contínua dos riscos** e a adaptação.
- Divide o desenvolvimento em ciclos, cada um com 4 atividades principais:
    1. Determinar objetivos.
    2. Avaliar alternativas (riscos).
    3. Desenvolver e testar.
    4. Planejar a próxima iteração.
#### Modelos Evolutivos (Geral)
- Baseia-se no princípio de que o cliente **não expõe todos os requisitos** ou eles estão em constante mudança.
- Envolve **múltiplos ciclos** de análise, projeto, desenvolvimento e entrega.
- O cliente usa o software e fornece **feedback**, que é usado para guiar a próxima versão (evolução).
##### Vantagens do Modelo Evolutivo
- **Participação constante do cliente**.
- Diminui o risco de má interpretação de requisitos.
- O software atende a algumas necessidades **muito mais cedo** no processo.
- Aumenta a chance de **satisfação do cliente**.
##### Desvantagens do Modelo Evolutivo
- **Documentação Limitada**: Devido à velocidade, não é sempre viável documentar cada versão.
- **Estrutura Frágil**: Softwares desenvolvidos rapidamente podem ser mal estruturados, comprometendo a integridade.
- **Complexidade de Modificações**: Incorporar mudanças pode se tornar cada vez mais difícil e dispendioso.
- **Alto risco de gerenciamento** (risco de nunca terminar, estrutura não robusta, mudanças radicais do cliente).
### Modelos Ágeis (XP, Scrum, Kanban)

#### Metodologia Tradicional vs. Ágil
| Característica | [[Metodologia Tradicional]] | [[Metodologia Ágil]] |
| :--- | :--- | :--- |
| **Processo** | Linear e sequencial | Iterativo e incremental |
| **Planejamento** | Documentado e rígido | Adaptável e flexível |
| **Entrega** | Produto 100% entregue | Produto entregue por partes |
| **Percepção de Valor** | Avaliada no final do projeto | Avaliada conforme o projeto avança |
#### [[SCRUM]]
- Framework ágil que foca na **colaboração e adaptação contínua**.
- Divide o desenvolvimento em **sprints** (ciclos curtos, geralmente 2-4 semanas).
- **Promove transparência** e permite ajustes frequentes baseados em feedback
#### [[KANBAN]]
- Método **visual** que foca na **gestão do fluxo de trabalho**.
- Tarefas são cartões que se movem em um quadro (Kanban board).
- Objetivo é **otimizar o fluxo**, identificar gargalos e eliminar desperdícios.
- Altamente **flexível** e adequado para mudanças rápidas de prioridade.
#### [[Extreme Programming (XP)]]
- Abordagem que enfatiza a **qualidade do código** e a **colaboração constante**.
- **Práticas:** Programação em pares, testes automatizados, integração contínua e *releases* frequentes.
- Enfatiza a **comunicação próxima** entre desenvolvedores, clientes e *stakeholders*.

---
## Outros Modelos
- O Modelo RAD (Rapid Application Development).
- Modelos de Métodos Formais.
- Modelo de Montagem de Componentes.
- Modelo de Desenvolvimento Concorrente.
- Processo Unificado.
---