---
tags:
  - "#NaoRevisado"
  - "#EngRequisitos"
---
# Engenharia de Requisitos - Requisitos de Usabilidade

## Introdução: UI, AI e UX

A interface, arquitetura da informação e experiência do usuário são conceitos interligados essenciais na criação de produtos.

### User Interface (UI)
>[!info] Definição de UI
> - Refere-se a toda parte **visual de uma interface**, tanto digital quanto física.
> - Envolve desde a criação de painéis de carros e controles remotos até a concepção de interfaces para aplicativos e sites.

### Architecture Information (AI)
>[!info] Definição de AI
> - É a área de estudo responsável por **organizar as informações** de uma interface.
> - Seu objetivo é facilitar o entendimento da informação pelo usuário.
> - Ganhou destaque com a demanda por **SEO** (Search Engine Optimization), onde o conteúdo e a informação se tornaram foco nos mecanismos de pesquisa.

### User Experience (UX)
>[!info] Definição de UX
> - **Experiência do Usuário** ou experiência de quem usa.
> - Existe desde que as pessoas começaram a "usar" objetos para realizar tarefas.
> - As experiências são **subjetivas**; cada pessoa tem uma experiência diferente ao usar o mesmo produto.

>[!quote] UX segundo Jakob Nielsen e Donald Norman
> - A [[Experiência do Usuário]] engloba **todos os aspectos** da interação do usuário final com a empresa, seus serviços e seus produtos.
> - É responsável por estudar as melhores maneiras de atender as **necessidades dos usuários** e deixá-los satisfeitos com todo o processo.
> - O termo "User Experience" foi criado por **Donald Norman** na década de 1990.

## O Conceito de Usabilidade

### Definição
>[!info] O que é Usabilidade?
> - Usabilidade é a **facilidade** com que as pessoas podem utilizar uma ferramenta ou objeto para realizar uma tarefa.
> - No campo de [[Human-Computer Interaction]] e [[User Experience]], refere-se à **simplicidade** e **facilidade** com que uma interface (site, aplicativo, etc.) pode ser utilizada.

### Usabilidade conforme a ISO/IEC 25000 (SQuaRE)
>[!info] Norma ISO/IEC 25000
> - Característica que estabelece que um produto ou sistema deve ser usado por um usuário específico para o alcance de metas específicas com **eficácia, eficiência e satisfação** em um contexto de uso determinado.
> - Representa o **esforço necessário** para utilizar o software, especificando tanto o nível de desempenho quanto a satisfação do usuário.

#### Subcaracterísticas
- **Aprendizagem**
- **Operabilidade**
- **Proteção ao erro do usuário**
- **Acessibilidade**
- **Reconhecimento**
- **Estética**

#### Aspectos de Aplicação
- **Facilidade de Aprender**: Associado ao tempo e esforço mínimo exigido para alcançar um determinado nível de desempenho no uso do sistema.
- **Facilidade de Uso**: Relacionado à velocidade de execução de tarefas e à redução de erros no uso do sistema.

#### Critérios de Medição
- Tempo para realizar uma tarefa
- Percentual da tarefa concluído
- Percentual da tarefa concluído por unidade de tempo
- Taxa de sucessos/falhas
- Número de comandos utilizados
- Número de comandos disponíveis não utilizados
- Frequência de uso de ajuda (help) ou documentação
- Número de vezes que o usuário expressa satisfação

## Requisitos de Usabilidade na Prática

### 1. Simplicidade não é Simples
Chegar a uma solução simples de usabilidade é um processo complicado. A simplificação exige vários **rounds de design** e discussões sobre a priorização de funções.

>[!tip] Vantagem das Interfaces Digitais
> - Elas permitem **exibir e esconder botões** à medida que o usuário avança no fluxo.

#### Modelos de Giles Colbourne para Solucionar o Excesso de Informação
1.  **Remova**: Livre-se de qualquer coisa que não seja essencial para a aplicação, incluindo conteúdo e linguagem nos *labels* de navegação.
2.  **Organize**: Distribua os elementos da interface em **grupos lógicos**, baseando-se em modelos mentais do usuário ou padrões de interface familiares.
3.  **Esconda**: Deixe apenas os itens mais importantes **ao alcance** (óbvios) e esconda os outros, deixando-os acessíveis apenas por navegação.
4.  **Mova**: Coloque algumas funcionalidades em **outro dispositivo ou lugar**, para que a interface não precise mostrar todas as interações possíveis de uma só vez.

### 2. Ofereça Informações em Pequenas Doses
Os seres humanos têm uma **capacidade limitada** de digerir informações quando estão ocupados realizando uma tarefa.

>[!tip] Regra Geral
> - A regra é **simplificar, reduzir e oferecer informações em doses digeríveis** para evitar que as pessoas se sintam pressionadas a tomar decisões excessivas.

- **Priorize** informações buscadas com frequência para que sejam acessadas com menos cliques.
- Evite bombardear o usuário com informação, garantindo que a tarefa seja realizada com sucesso.
- Use o **mínimo de informação e texto possível** para a tarefa.
- Verifique se imagens estão contribuindo para a tarefa, em vez de serem meramente decorativas.
- Considere **excluir ou esconder links menos clicados** para simplificar a interface.

### 3. Crie Hierarquia na Página
Hierarquia é o uso de diferentes **estilos visuais** para os elementos da tela, priorizando o que é mais importante. Uma boa hierarquia guia os olhos do usuário pelo caminho desejado.

- **Problema**: Quando tudo é importante, **nada é importante** (Exemplo: excesso de opções em uma prateleira de farmácia).

#### Boas Práticas para Hierarquia
- Organize **itens similares com visual similar**.
- Evite inconsistências; use o mesmo estilo visual para elementos com funções parecidas.
- Use **cores** e contraste para diferenciar as ações principais e atrair o olhar.
- **Categorize** e agrupe links por temas.
- Use **tamanhos de fonte diferentes** para criar hierarquia, mas limite a quantidade para manter a harmonia.
- Tenha um bom **equilíbrio de textos e imagens**; imagens podem tirar o foco em processos críticos como pagamento.

### 4. Diga ao Usuário o que Fazer a Seguir
É crucial evitar "ruas sem saída". O usuário precisa saber, em toda tela, o que deve fazer a seguir.

- Quando o usuário fica sem opções, é comum ele abandonar o site.
- Cada decisão que o usuário é forçado a tomar aumenta o **esforço cognitivo**.
- **Ação Principal**: Deve estar nítida o suficiente.
- **Texto do Botão**: O texto deve dar uma dica clara do que vem a seguir (Exemplo: em vez de "Enviar," use "Criar Minha Conta").

>[!question] Perguntas para Otimizar a Usabilidade do Produto
> - O usuário sabe **onde está** (página, site, passo do fluxo)?
> - O usuário sabe **o que fazer a seguir**?

### 5. Dê Feedback sobre o Estado do Sistema
**Clareza** é a palavra de ordem. O usuário precisa entender o que está se passando com o sistema a qualquer momento.

- Toda ação deve ter uma **reação imediata** da interface para uma boa experiência.
- Em caso de preenchimento incorreto de um formulário, a interface deve comunicar isso com clareza e dar **instruções precisas** sobre como resolver o problema.

### 6. Evite Erros Antes que Aconteçam
É mais interessante prevenir erros do que comunicá-los. Um erro do usuário é frequentemente **culpa da interface** que falhou em guiá-lo corretamente.

- **Prevenção Ativa**: O sistema deve antecipar o erro e tomar medidas para evitá-lo.
    - **Exemplo (iOS)**: Oculta a opção de compartilhar por e-mail se mais de 5 fotos forem selecionadas, prevendo que o anexo seria muito pesado.
    - **Exemplo (Twitter)**: Destaca em vermelho os caracteres excedentes e desabilita o botão *Tweet* para evitar que o erro de limite ocorra.
    - **Exemplo (Gmail)**: Mostra um alerta se o usuário usa palavras como "anexo" mas não anexou nenhum arquivo, confirmando se houve distração.

### 7. Simplifique Formulários
- Pergunte-se: Qual o **mínimo de informação** que você precisa coletar do usuário para que ele possa seguir adiante no fluxo?
- Evite pedir todas as informações que a empresa deseja em um único formulário; colete o essencial.
- Verifique se a informação pode ser coletada em um momento futuro e se está claro para o consumidor por que ela é solicitada.
- Oferecer a opção de "**Comprar sem conta**" ou "Comprar como convidado" evita um desvio de rota grande na experiência do usuário (Exemplo: Nike.com).
- Apresente o **melhor tipo de campo** para o usuário (Exemplo: usar um **calendário** para seleção de datas em vez de um campo de texto, evitando erros de formatação como $DD/MM/AAAA$).

## Princípios de Usabilidade de Hansen

Wilfred J. Hansen publicou em 1971 os princípios de Usabilidade para sistemas interativos (User engineering principles for interactive systems).

### Principais Princípios (ou Engenharia de Usuário)
- **Primeiro Princípio: Conhecer os Usuários**
    - O desenvolvimento deve começar com os **usuários e suas necessidades**, antes de qualquer questão tecnológica.
    - É necessário pesquisar, observar e entrevistar pessoas para conhecer seus hábitos, comportamentos, contexto e rotina.
    - O foco nas necessidades, desejos e limitações dos usuários deve ser mantido durante todo o projeto.
- **Minimizar Memorização**
    - Reduzir a necessidade de memorização substituindo a entrada de dados pela **seleção de itens**, usando nomes em vez de números, prevendo comportamentos e fornecendo fácil acesso às informações.
- **Otimizar Operações**
    - Execução rápida de operações comuns, **consistência da interface**, e organização/reorganização da estrutura da informação baseada na observação do uso do sistema.
- **Boas Mensagens de Erro**
    - Criar designs que **evitem os erros mais comuns**, possibilitar desfazer ações realizadas e garantir a integridade do sistema em caso de falha.

## Os 10 Princípios Heurísticos de Nielsen

Jakob Nielsen, co-fundador do Nielsen Norman Group, criou a [[avaliação heurística]].

1.  **Visibilidade do status do sistema**
2.  **Compatibilidade do sistema com o mundo real**
3.  **Dar controle e liberdade ao usuário**
4.  **Consistência e padrões**
5.  **Prevenir erros**
6.  **Reconhecer ao invés de lembrar**
7.  **Flexibilidade e eficiência no uso**
8.  **Estética e design minimalista**
9.  **Ajude o usuário a reconhecer, diagnosticar e se recuperar de erros**
10. **Ajuda e documentação**
---