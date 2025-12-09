---
tags:
  - Concluido
---
# Guia para o Gerenciamento de Processos de Negócio (BPM CBOK) V3.0
## I. Fundamentos da Disciplina de BPM
### O que é Processo de Negócio?
>[!info] Definição e Tipos
>Um processo é uma agregação de atividades e comportamentos executados por humanos ou máquinas para alcançar um ou mais resultados. Essa é uma visão **lógica** que orquestra atividades (visão física).
> - **Processo Primário (Essencial)**: Processo interfuncional ponta a ponta que agrega valor **diretamente para o cliente**.
> - **Processo de Suporte**: Existe para prover suporte a processos primários ou de gerenciamento, mas **não agrega valor diretamente** para o cliente.
> - **Processo de Gerenciamento**: Tem o propósito de **medir, monitorar, controlar** e administrar o negócio, assegurando que os processos primários e de suporte atinjam suas metas.
### BPM como Disciplina Gerencial
- **Definição**: BPM é uma disciplina gerencial que integra estratégias e objetivos da organização com as necessidades dos clientes, focando em processos ponta a ponta.
- **Capacidade Básica Interna**: BPM é uma capacidade que a organização desenvolve, envolvendo métodos, pessoas e tecnologias para gerenciar processos de forma eficiente e eficaz.
- **Ciclo de Vida Contínuo**: Processos devem ser gerenciados em um ciclo contínuo para manter sua integridade e permitir a transformação. O ciclo típico (análogo ao PDCA) envolve **Planejamento, Análise, Desenho, Implementação, Monitoramento & Controle e Refinamento**.
### Foco no Cliente (Visão Outside In)
- O propósito principal de uma organização é gerar valor para o cliente por meio de seus produtos e serviços.
- O BPM trata o trabalho **ponta a ponta**, orquestrando atividades ao longo das fronteiras funcionais (funções de negócio) para entregar produtos e serviços da forma mais **eficaz** possível para o cliente (visão "de fora para dentro" - *outside in*).
- O conceito de **"cliente interno" não faz sentido** na perspectiva BPM; o que existe são atores de processo ou outros processos encadeados.
- **Instância de Processo**: Cada execução de um processo (ex: um atendimento ao cliente).

---
## II. As Áreas de Conhecimento do BPM CBOK
O BPM CBOK V3.0 está organizado em **9 Áreas de Conhecimento**.
### 1. Modelagem de Processos (Capítulo 3)
- **Propósito**: Criar **representações completas e precisas** dos processos existentes ("AS-IS") ou propostos ("TO-BE") para comunicação e gerenciamento[^1].
- **Notações Chave**:
	- **[[BPMN (Business Process Model and Notation)]]**: Padrão robusto para modelagem e simulação, suportado por BPMS.
	- **Fluxograma**: Usa um conjunto simples de símbolos, útil para capturar fluxos rapidamente.
	- **EPC (Event-driven Process Chain)**: Descreve eventos desencadeantes e resultantes de funções.
	- **Raias de Piscina (Swim lanes)**: Construção que representa o executor (papel ou função) das atividades, ajudando a visualizar **handoffs** (transferências de controle).
	- **Diagrama vs. Modelo**: O **modelo** implica maior precisão e mais dados (permitindo simulação), enquanto o **diagrama** é uma representação simplificada.
	- **Abordagens de Modelagem**: Pode ser de **cima para baixo** (*top-down*), **de baixo para cima** (*bottom-up*) ou **do meio para fora** (*middle-out*).
### 2. Análise de Processos (Capítulo 4)
- **Propósito**: Criar um **entendimento comum** do estado atual ("AS-IS") e avaliar a **eficiência e eficácia** do processo.
- **Foco da Análise**: A análise deve ser **ponta a ponta** e abranger **O QUE, ONDE, QUANDO, POR QUE, COMO e POR QUEM** o trabalho é feito.
- **Técnicas de Levantamento**: Pesquisa, entrevista, workshop estruturado, observação direta e simulação de atividades.
- **Técnicas Analíticas**:
- **Análise de Padrão**: Busca por atividades repetidas para racionalização.
- **Análise de Causa-Raiz**: Usada para descobrir a fonte implícita de um problema.
- **Análise SWOT**: Avalia Forças, Fraquezas, Oportunidades e Ameaças para posicionamento estratégico.
- **Análise de Custo e Tempo de Ciclo**: Essenciais para quantificar o desempenho.
- **Análise de Valor**: Classifica atividades em "adiciona valor ao cliente", "adiciona valor ao negócio" ou "não adiciona valor".
- **Handoffs**: Pontos onde o trabalho ou a informação passa de uma função para outra, sendo áreas de risco e vulnerabilidade a desconexões.
### 3. Desenho de Processos (Capítulo 5)
- **Propósito**: Concepção de novos processos e especificação de como funcionarão, serão medidos, controlados e gerenciados ("TO-BE").
- **Distinção Crítica**: O desenho deve considerar o nível de **Fluxo de Processo** (interfuncional) e **Fluxo de Trabalho** (intrafuncional) para evitar maximizar a eficiência em um nível e comprometer a eficácia em outro.
- **Abordagem**: Deve começar com o entendimento do **estado atual ("AS-IS")** e da **cultura organizacional**.
- **Simplicidade**: Simplicidade é um direcionador fundamental; a perfeição é alcançada quando não há mais o que retirar do processo.
- **Desenho de Serviço (Outside In)**: Em serviços, o cliente é parte integral da geração de valor. O desenho deve ser centrado no cliente como um **ator primário**.
- **Sustentabilidade**: O desenho deve considerar os impactos ambientais e sociais (Triple Bottom Line - Profit, Planet, People), buscando reduzir o consumo de recursos e desperdícios.
### 4. Gerenciamento de Desempenho de Processos (Capítulo 6)
- **Propósito**: Monitoramento formal e planejado da execução dos processos para apurar sua **eficiência e eficácia**.
- **Desempenho de Processo**: Rendimento em termos de **tempo, custo, capacidade e qualidade**.
- **Conceitos de Medição**:
- **Medida**: Quantificação de dados em padrão aceitável.
- **Métrica**: Extrapolação de medidas (cálculo).
- **Indicador**: Representação simplificada de métrica ou medida, comparada a um alvo.
- **PPI (Process Performance Indicators)**: Indicadores que monitoram as metas de desempenho do processo.
- **Tipos de Indicadores**: Indicadores **direcionadores** (*drivers*) monitoram a causa antes do efeito e permitem alterar o curso; Indicadores de **resultados** (*outcome*) monitoram o efeito (resultado final).
- **Controle Estatístico de Processos (SPC)**: Lida com a coleção, classificação e análise de dados para entender, reduzir ou eliminar a **variabilidade** em processos instáveis.
### 5. Transformação de Processos (Capítulo 7)
- **Propósito**: Discorre sobre mudanças em processos, com o objetivo de **reinvenção** ou **modernização** da operação, e não apenas melhoria.
- **Amplitudes de Transformação**:
	- **Melhoria de Processos (BPI)**: Iniciativa ou projeto para melhorias específicas e **incrementais** (ex: [[Lean]], Six Sigma).
	- **Redesenho de Processos**: Repensar holístico do processo existente, mas ainda baseado em conceitos fundamentais do processo.
	- **Reengenharia de Processos (BPR)**: Repensar **fundamental** e **redesenho radical** de processos para obter melhorias dramáticas ("Jogue tudo fora e comece novamente do zero").
	- **Mudança de Paradigma**: Criação de novas abordagens e regras, tornando a concorrência irrelevante (ex: Estratégia do Oceano Azul).
	- **Gerenciamento de Mudança**: Processo iterativo que auxilia a organização e colaboradores na transição de um estado atual para um estado futuro sustentável. Envolver os colaboradores **cedo e comunicar frequentemente** é fator-chave de sucesso para superar a resistência.
### 6. Organização do Gerenciamento de Processos (Capítulo 8)
- **Organização Orientada por Processos**: Estruturada, organizada, mensurada e gerenciada em torno de seus processos de negócio.
- **Papéis Centrais de BPM**:
	- **Dono de Processos**: Responsável final pelo desenho, execução e desempenho (eficácia e eficiência) do processo ponta a ponta.
	- **Gerente de Processos**: Coordena e gerencia o desempenho no dia a dia e lidera iniciativas de transformação.
	- **Arquiteto de Processos**: Responsável por desenvolver e manter o modelo de *Arquitetura Corporativa de Processos*, repositório e padrões.
	- **Escritório de Processos (Process Office)**: Dono do processo de gerenciamento de processos, definindo princípios, práticas e padrões de BPM (governança).
### 7. Gerenciamento Corporativo de Processos (Capítulo 9)
- **Gerenciamento Corporativo de Processos (EPM)**: Aplica BPM em toda a organização para alinhar o portfólio e a arquitetura de processos com a estratégia e prover um modelo de **governança**.
- **Modelo de Maturidade em Processos**: Avaliação que ajuda a organização a definir o roteiro para aumentar a maturidade e a capacidade dos processos, progredindo de Ad-hoc a Gerenciado Proativamente.
- **Melhores Práticas**: Adotar a visão **"de fora para dentro"** (outside in), atribuir corretamente nomes aos processos (ex: Do Pedido ao Caixa) e construir um plano focado em **transformação**.
### 8. Tecnologias de BPM (Capítulo 10)
- **Princípio**: A tecnologia desempenha papel de **apoio** e não de liderança na implementação de BPM.
- **BPMS (Business Process Management Suite)**: Conjunto de ferramentas que fornece o ambiente completo de operação para modelagem, execução, controle, simulação e geração de aplicações.
- **BRMS (Business Rules Management Systems)**: Ferramentas que proveem suporte à identificação, definição e execução de **regras de negócio**.
- **SOA/EAI (Service Oriented Architecture/Enterprise Application Integration)**: Abordagem de arquitetura para vincular recursos sob demanda e integrar sistemas, permitindo o reuso e compartilhamento de serviços.
- **Gerenciamento Adaptativo de Caso (ACM)**: Abordagem para descrever e automatizar o trabalho de **Processos de Negócio Intensivos em Conhecimento (KIBP)**, onde o processo é imprevisível e não se repete de forma consistente.

--- 

[^1]: Acesse [[04 - Modelagem de Processos de Negócio (BPMN)]] para saber mais sobre modelagem de processos.
