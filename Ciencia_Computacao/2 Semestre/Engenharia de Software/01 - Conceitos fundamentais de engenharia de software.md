# Conceitos Fundamentais
## [[Software]] e Produtos
### Definição de Software
>[!quote] Segundo Pressman (2006)
> - Software é um conjunto composto por **instruções de computador**, **estruturas de dados** e **documentos**.
### Tipos de Produtos de Software
- **Genéricos:** Desenvolvidos para serem vendidos para uma grande variedade de clientes (ex: Excel, Word).
- **Personalizados:** Desenvolvidos para um único cliente de acordo com suas especificações.
---
## Definições de Engenharia de Software

A Engenharia de Software é a aplicação de uma abordagem sistemática e organizada ao desenvolvimento de software, buscando a eficiência e qualidade.

>[!quote] Segundo o IEEE (1992)
> - "Engenharia de software é a aplicação de uma abordagem **sistemática**, **disciplinada** e **quantificável**, para o **desenvolvimento**, **operação** e **manutenção** do software; isto é, a aplicação de engenharia ao software".

>[!quote] Segundo Bauer (1969) apud Pressman (2006)
> - Engenharia de Software é "a criação e a utilização de **sólidos princípios de engenharia** a fim de obter softwares **econômicos** que sejam **confiáveis** e que trabalhem eficientemente em máquinas reais".
### Objetivos da Engenharia de Software
Almeja inserir as mesmas sistemáticas de outras áreas da engenharia:
- Custos aceitáveis.
- Gerenciamento do **processo de desenvolvimento**.
- Garantia do **trabalho em equipe**.
- Desenvolvimento de softwares com **qualidade**.
---
## Princípios da Engenharia de Software

Alguns princípios visam o bom funcionamento do produto final:
- Evitar dependência de determinadas pessoas ou processos.
- **Abstrair** aspectos importantes.
- **Subdividir problemas complexos**.
- **Reutilizar** resultados (código).
- **Flexibilização** e **modularização** para facilitar a manutenção.
---
## Fundamentos (Áreas Multidisciplinares)

A Engenharia de Software une as seguintes áreas:
- **[[Ciências da Computação]]**: Abrange arquitetura de computadores, lógica de programação, estrutura de dados, algoritmos, etc..
- **Administração**: O engenheiro de software atua como gestor, administrando prazos, equipe, custos e resultados.
- **Comunicação**: Habilidade para se expressar com clientes ou usuários.
- **Técnicas de solução de problemas**: Ser um solucionador de problemas, gerando soluções integradas e inteligentes.
---
## Surgimento da Engenharia de Software
### Década de 50
- Surgiram os primeiros softwares.
- Pesquisas eram focadas no **hardware**.
- Software desenvolvido **sem utilizar técnicas de engenharia**.
### Década de 60
- Surgiram os microprocessadores, e o hardware deixou de ser o principal problema.
- O **software tornou-se o foco** dos pesquisadores.
- Organizações começaram a desenvolver grandes sistemas.
### Problemas Iniciais (Falta de Metodologia)
A falta de metodologia resultou em:
- Equipes sem um modelo de como desenvolver.
- Ausência de documentação adequada.
- Dificuldade em dar **manutenção** em sistemas sem projeto ("E agora: como dar manutenção em um sistema que não tem projeto?").
---
## Desafios e Problemas Encontrados
### Desafios da Engenharia de Software
Os desafios atuais incluem:
- **Reduzir custos**: o custo de produção eram altos;
- **Melhorar a qualidade** do software: os recursos destinados ao projeto normalmente eram insuficiente;
- **Atender às expectativas do cliente**: as soluções propostas e desenvolvidas não conseguiam agradar os clientes;
#### Desafios-Chave Atuais
- **Heterogeneidade**: Construção de software que lide com plataformas heterogêneas e ambientes de execução.
- **Entrega (Delivery)**: Técnicas para a entrega mais rápida de software.
- **Confiança**: Técnicas que demonstrem que o software pode ter a confiança de seus usuários.
### Problemas Comuns
- **Custos:** O custo de software domina os custos de sistemas computacionais, sendo frequentemente maior que o custo do hardware em PCs;
- **Manutenção:** Manter um software custa mais que desenvolvê-lo;
- **Prazos e Custos:** Clientes reclamam que prazos e custos não são respeitados;
- **Requisitos:** Ineficiência na definição de requisitos que não atendem às necessidades dos clientes;
- **Gestão:** Gerentes e coordenadores despreparados para controlar o desenvolvimento.
#### Custo Relativo de Correção de Defeitos
O custo para corrigir um defeito aumenta drasticamente nas fases mais tardias do processo, sendo:
![[Pasted image 20251116003136.png | 500 | center]]

>[!note]
> - 60% dos custos são de desenvolvimento e 40% são de testes.
> - Para software sob encomenda, os custos de **evolução** (manutenção) normalmente excedem os de desenvolvimento.

---
## Camadas da Engenharia de Software

A Engenharia de Software é construída sobre quatro camadas que trabalham juntas, com foco constante na **qualidade**:
1.  **Ferramentas** (Apoio automatizado):
    - Inclui **[[CASE]]** (Computer Aided Software Engineering).
    - Abrange ferramentas de banco de dados e linguagens de programação.
2.  **Métodos** (Como fazer):
    - Diferentes métodos para as etapas de desenvolvimento.
    - Existem métodos para análise de requisitos, projeto, codificação, testes e manutenção.
3.  **Processo** (Métodos + Ferramentas):
    - Define a sequência dos métodos e as ferramentas que serão disponibilizadas.
---
## Estrutura de um Processo de Software (Atividades Genéricas)
O Processo de Software é o conjunto de atividades para o desenvolvimento ou evolução de um software. As atividades genéricas em todos os processos são:

1.  **[[Comunicação]]** (Foco no cliente/usuário):
    - Envolve alta comunicação e colaboração com o cliente/usuário.
    - Abrange o **levantamento de requisitos**.
2.  **[[Planejamento]]**:
    - Descreve tarefas técnicas, riscos, recursos, produtos que serão produzidos e um **cronograma**.
3.  **[[Modelagem]]**:
    - Constrói modelos para que desenvolvedor e cliente entendam os requisitos e o software que atenderá esses requisitos.
4.  **[[Construção]]**:
    - Criação dos **códigos** e execução de **testes**.
5.  **[[Implantação]]**:
    - Avaliação e **feedback** do cliente sobre o software desenvolvido.

### Atividades Genéricas Focadas
- **Especificação**: O que o sistema deve fazer e suas restrições de desenvolvimento.
- **Desenvolvimento**: Produção do sistema de software.
- **Validação**: Verificação de que o software é o que o cliente deseja.
- **[[Evolução]]**: Mudança do software em resposta às demandas de mudança (manutenção).
---
## Atributos de um Bom Software

Um bom software deve ter:
- **Facilidade de Manutenção**: Deve evoluir para atender às necessidades de mudança.
- **Confiança**: O software deve ser confiável.
- **Eficiência**: Não deve desperdiçar os recursos do sistema.
- **Usabilidade**: Deve ser aceito pelos usuários, sendo compreensível, usável e compatível com outros sistemas.
---
## Tipos de Software (Exemplos de Áreas Potenciais)

Com o aumento da complexidade, a classificação se torna difícil. Áreas potenciais incluem:
- Software básico.
- Software de tempo real.
- Software comercial.
- Software científico e de engenharia.
- Software embutido.
- Software de computador pessoal.
- Software linguagens de 4ª geração.
- Software educativo.
- Software de [[Inteligência Artificial (IA)]].
- Software de gestão empresarial.
- Software de informações gerenciais.
- Software de apoio à decisão.
---