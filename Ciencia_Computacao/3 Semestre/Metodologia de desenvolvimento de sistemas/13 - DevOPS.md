---
tags:
  - MDS
  - Naoconcluido
  - NaoRevisado
---
# DevOps: Cultura, Fluxo e Feedback Contínuo

>[!info] Conceito de DevOps
> - **DevOps** é um conjunto de práticas que enfatiza a **automação**, **comunicação** e **colaboração** entre equipes de **Desenvolvimento (Dev)** e **Operações (Ops)**.
> - Busca construir, testar e implantar aplicações de forma mais rápida e confiável.
> - A cultura de DevOps é construída com base na colaboração de equipes que, tradicionalmente, funcionavam como silos organizacionais com **objetivos conflitantes**.
> - Enquanto o time **Dev** foca na **velocidade** e entrega de novas *features* , o time **Ops** foca na **estabilidade**, confiabilidade e bom desempenho do ambiente de produção.

## Importância e Benefícios do DevOps
- O DevOps é amplamente relevante no mercado, com 56% das organizações já tendo uma iniciativa em andamento e 44% considerando-o **muito importante**.
- **Medidas Críticas de Sucesso**:
	- Acelerar a velocidade de entrega (**67%**)
	- Melhorar a qualidade (**61%**)
	- Reduzir o risco (**47%**)
	- Aumentar a satisfação do cliente (**45%**)
	- **Acelera a Velocidade**: Equipes de alta performance possuem *lead times* mais curtos e implementações 200x mais frequentes.
	- **Melhora a Estabilidade**: Reduz 3x a taxa de falha de mudança e permite 24x mais rápida recuperação de falhas.

>[!tip] Lead Time (Tempo de Ciclo)
> - É a medida de qualidade do processo de desenvolvimento, medindo o tempo médio que leva para ir do **conceito ao dinheiro** ou do **pedido do cliente à entrega do software**.
> - Um desempenho excelente resulta em completar o ciclo com o menor tempo e esforço desperdiçados.
## DevOps e o Pipeline de Implantação
- O DevOps, que sucede o movimento [[Ágil]], estende a visão do ciclo de vida do software, englobando desde o início do Desenvolvimento até o Suporte em Produção (Ciclo Infinito).
- **[[Entrega Contínua]] (Continuous Delivery)** é uma disciplina que visa criar software em um estado que possa ser liberado em produção a qualquer momento de forma rápida e confiável.
- O **Pipeline de Implantação (Deployment Pipeline)** é o fluxo de entrega de software de forma rápida e confiável, repetidamente, que integra:
	- Planejar, Codificar
	- Integrar (**Integração Contínua**)
	- Testar (**Testes Integrados**)
	- Release
	- Implantar (Deploy)
	- Operar
	- Feedback
## As Três Maneiras do DevOps (Three Ways)
### 1. Fluxo (Flow)
- Permite o **fluxo rápido** do trabalho da Esquerda (Desenvolvimento) para a Direita (Operações e Cliente).
- O foco é otimizar o fluxo de valor global, e não apenas melhorias locais.
- **Práticas para Otimizar o Fluxo**:
	- **Torne o Trabalho Visível**: Utilizar quadros [[Kanban]] ou quadros de tarefas para transformar o trabalho invisível do software em visível, facilitando a identificação de gargalos e trabalhos incompletos (WIP).
	- **Reduza o Tamanho do Lote**: Lotes de trabalho menores levam a um **Menor Lead Time**.
	- **Aplique a Teoria das Restrições (TOC)**: Focar melhorias na **restrição** (gargalo) do fluxo. Qualquer melhoria feita fora da restrição é uma ilusão.
	- **Gerencie o WIP (Work In Progress)**: Estabelecer um limite para o trabalho em andamento para melhorar o fluxo e reduzir o tempo de ciclo.
	- **Reduza as Transferências de Trabalho (Hands-off)**: A transferência de conhecimento a cada nova etapa do processo (Reqs $\to$ Design $\to$ Dev $\to$ Test $\to$ Ship $\to$ Customer) é um ponto de perda de conhecimento e geração de filas. Formas de reduzir: **Automação de Processos** e **Reorganização das equipes** com autonomia.
### 2. Feedback (Feedback)
- Permite o **fluxo rápido e constante de feedback** da Direita (Operações/Cliente) para a Esquerda (Desenvolvimento).
- O objetivo é revelar os problemas à medida que ocorrem e focar na causa raiz.
- **Práticas para Criar Feedback Rápido**:
	- **Testes Automatizados**: Reduzem esforço manual, minimizam erros humanos e permitem a detecção antecipada de defeitos.
	- **Revisão de Código (Manual/Automatizada)**: Essencial para verificar a correção lógica, semântica, o uso de padrões de codificação e a segurança.
	- **Integração Contínua (CI)**: Construção e teste de código no ambiente de desenvolvimento, permitindo testes sistêmicos.
	- **Implantação Contínua (Continuous Deployment)**: O código é liberado para produção de forma **automática** a qualquer momento.
	- **Entrega Contínua (Continuous Delivery)**: O código é liberado para produção a qualquer momento, mas a entrega **não é automática** (requer aprovação manual).
	- **Teste A/B**: Comparação de versões diferentes para identificar qual tem a melhor aceitação do público-alvo.
	- **Telemetria**: Feedback em tempo real (Nível de Negócio, Aplicação e Infraestrutura) para monitorar aplicativos.
### 3. Aprendizado e Experimentação Contínua
- Criação de uma cultura generativa de alta confiança que suporta uma abordagem dinâmica e científica para tomada de riscos na experimentação.
- É crucial **combater a cultura do medo** e do comando e controle.
- **Práticas**:
- Alocar tempo para melhorar o trabalho diário.
- Transformar descobertas locais em conhecimento global.
- Introduzir falhas no sistema para aumentar a resiliência (Engenharia do Caos).
- Líderes devem reforçar uma cultura de aprendizagem.
## O Desafio das Especialidades
- A organização excessiva por especialidades (perfil **I-Shape** ou especialista) gera *lead times* mais longos e problemas de comunicação (silos).
- O DevOps incentiva o perfil **T-Shape** (generalista-especialista) ou **E-Shape** (experiência em várias áreas + especialização profunda).
- O **Cross-Training** (treinamento cruzado) é essencial para aumentar as habilidades T-Shaped da equipe.

---