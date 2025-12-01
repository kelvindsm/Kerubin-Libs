---
tags:
  - Emprogresso
  - NaoRevisado
---
# Requisitos de Qualidade do Software (Não Funcionais): Norma ISO 25000

## Qualidade de Software: Conceitos e Importância

A **Qualidade de Software** é avaliada por atributos que garantem que o sistema satisfaça as necessidades dos usuários e agregue valor. A qualidade de um sistema é o grau em que ele satisfaz as necessidades explícitas e implícitas de seus usuários.

>[!quote] Definição de Roger Pressman
> "Qualidade de software é a conformidade a requisitos funcionais e de desempenho, que foram explicitamente declarados, a padrões de desenvolvimento claramente documentados, e a características implícitas que são esperadas de todo o software profissionalmente desenvolvido".

### Aspectos Chave da Qualidade
As definições de qualidade enfatizam três aspectos importantes:

1. **Requisitos são a base:** Os [[Requisitos Funcionais]] e de desempenho são a base a partir da qual a qualidade é medida. A falta de conformidade com os requisitos significa falta de qualidade.
2. **Padrões de Desenvolvimento:** Padrões especificados definem um conjunto de critérios que orientam a maneira pela qual o software é desenvolvido.
3. **Requisitos Implícitos:** Existe um conjunto de requisitos que frequentemente não são mencionados na especificação, mas são esperados (ex: integridade dos dados, facilidade de uso, [[Manutenibilidade]]).

### Qualidade e o Ponto de Vista
A percepção da qualidade do software varia dependendo do [[Stakeholder]]:

- **Usuário:** O interesse se concentra principalmente no uso do software, como a **facilidade de uso** e se os requisitos foram atendidos.
- **Desenvolvedor:** A qualidade está mais voltada às **características internas** do software, como legibilidade, [[Testabilidade]] e eficiência.
- **Gerente:** A qualidade não pode ser desvinculada dos interesses da organização, como **custos e prazos**.

### Premissas da Qualidade
- A qualidade não pode ser incorporada ao produto depois de pronto.
- Ela deve ser um objetivo constante do processo de desenvolvimento, inserida desde as primeiras fases do ciclo de vida.

## Histórico e Arquitetura ISO 25000 (SQuaRE)

O **SQuaRE (Software Product Quality Requirements and Evaluation)** é a arquitetura de normas que orienta a revisão e criação de padrões de qualidade de software.

>[!info] Norma ISO/IEC 25000
> - **Família de Normas:** Reformulação das normas **ISO/IEC 9126** (Características de Qualidade de Software) e **ISO/IEC 14598** (Guias para Avaliação de Produto de Software).
> - **ISO/IEC 25010:** É uma norma disponibilizada em 2011 que define modelos de avaliação da qualidade de produto de software e sistemas.
> - **Substituição:** Substituiu a ISO/IEC 9126, adicionando formalmente **Segurança** e **Compatibilidade** às características principais.

### Divisão da ISO/IEC 25000
A família ISO 25000 é dividida em seções (2500n, 2501n, etc.) para cobrir todo o ciclo de qualidade:

- **2501n (Modelo de Qualidade):** Define o modelo hierárquico de características e subcaracterísticas de qualidade do produto.
- **2502n (Medição da Qualidade):** Modelo de referência para a medição de produtos de software.
- **2503n (Requisitos de Qualidade):** Especifica o que são requisitos de qualidade.
- **2504n (Avaliação da Qualidade):** Requisitos, recomendações e orientações para a avaliação.

## ISO/IEC 25010: Qualidade do Produto de Software

A ISO/IEC 25010 define 8 características de qualidade de produto de software, essenciais para a especificação de [[Requisitos Não Funcionais (RQs)]].

### 1. Adequação Funcional
Diz que um sistema deve fornecer funções que correspondam às necessidades explícitas e implícitas, quando usado sob condições especificadas.

- **Subcaracterísticas:** Completude funcional, Correção funcional, Adequabilidade funcional.

### 2. Eficiência de Desempenho
Estabelece o desempenho de um sistema em relação à quantidade dos **recursos utilizados** sob condições estabelecidas.

- **Subcaracterísticas:** Comportamento no tempo (tempo de resposta), Utilização de recursos (memória, CPU), e Capacidade.
- **Exemplo:** O sistema deve suportar até 100 usuários simultâneos sem se degradar.

### 3. Compatibilidade
Diz que um produto ou sistema deve trocar informações e/ou realizar suas funções necessárias, ao compartilhar o mesmo ambiente de hardware ou software.

- **Subcaracterísticas:** Coexistência e Interoperabilidade.
- **Exemplo:** O software deve rodar em navegadores Edge, Firefox e Chrome.

### 4. Usabilidade
Estabelece que um produto ou sistema deve ser usado por um usuário específico para o alcance de metas específicas com eficácia, eficiência e satisfação em um contexto de uso determinado.

- **Subcaracterísticas:** Aprendizagem, Operabilidade, Proteção ao erro do usuário, Acessibilidade, Reconhecimento apropriado, Estética da interface.
- **Exemplo:** Documentação quanto ao uso e funcionamento deve ser fornecido por meio de orientação *on-line*.

### 5. Confiabilidade
Diz que um sistema executa funções específicas sob condições determinadas em um dado período de tempo. Capacidade de evitar falhas e manter desempenho adequado.

- **Subcaracterísticas:** Maturidade, Tolerância a falhas, Capacidade de recuperação, e [[Disponibilidade]].
- **Exemplo:** Se o processo for interrompido por uma falha, o sistema deve permitir recuperar os dados e continuar.

### 6. Segurança
Diz que um sistema protege as informações e dados, de modo que as pessoas, outros produtos ou sistemas possuam o grau de acesso de dados apropriado.

- **Subcaracterísticas:** Integridade, Confidencialidade, Não Repúdio, Autenticidade, Responsabilização (Rastreabilidade).
- **Referência:** Normas da família ISO/IEC 27000 (Sistema de Gestão de Segurança da Informação).

### 7. Manutenibilidade
Diz que um sistema possui a capacidade de ser **modificado** com determinado grau de eficácia e eficiência. Corresponde à capacidade de comportar modificações, melhorias, correções ou adaptações a novos requisitos.

- **Subcaracterísticas:** Testabilidade, Modularidade, Reusabilidade, Analisabilidade, Modificabilidade.

### 8. Portabilidade
Diz que um sistema pode ser **transferido** de um hardware, software ou ambiente operacional para outro, com determinado grau de eficácia e eficiência.

- **Subcaracterísticas:** Adaptabilidade, Instalabilidade, Capacidade de substituição.
- Corresponde à capacidade de operar em diferentes ambientes (organizacionais, de hardware e software).

## ISO/IEC 25010: Qualidade em Uso do Software

Além das 8 características de Produto, a ISO/IEC 25010 fornece um modelo de **Qualidade em Uso**, que é uma avaliação da qualidade na perspectiva do usuário.

- **Fatores de Avaliação:**
- **Efetividade:** Capacidade de atender a metas específicas sob condições de uso, levando em conta a exatidão e a integridade.
- **Eficiência:** Grau de consumo de recursos pelo software ao atingir metas específicas.
- **Satisfação:** Capacidade de agradar seus usuários, satisfazendo necessidades (inclui Utilidade, Confiança, Prazer e Conforto).
- **Ausência de Riscos:** Grau em que o software minimiza riscos econômicos, humanos, de saúde e ambientais (Mitigação de riscos).
- **Cobertura de Contexto:** Grau em que um software pode ser usado com eficácia e satisfação, tanto em contextos específicos de uso quanto naqueles não explicitamente identificados (inclui Completude e Flexibilidade do Contexto).