---
tags:
  - Naoconcluido
---
# Qualidade de Software e Norma ISO 25000 (Requisitos de Qualidade)

## 1. Conceitos e Premissas da Qualidade de Software

- **Definição Geral:** A qualidade de um sistema é o grau em que o sistema satisfaz as **necessidades explícitas e implícitas** de seus usuários, e, portanto, fornece valor.
- **Definição de Roger Pressman:** Qualidade é a conformidade a requisitos funcionais e de desempenho (explícitos), a padrões de desenvolvimento (documentados), e a **características implícitas** esperadas (ex: integridade, manutenibilidade).
- **A Qualidade depende do Ponto de Vista:**
    - **Usuário:** Foco na facilidade de uso e requisitos atendidos.
    - **Desenvolvedor:** Foco em características internas (legibilidade, testabilidade, eficiência).
    - **Gerente:** Foco nos interesses organizacionais (custos e prazos).

### Premissas e Desafios
- **Premissas:** A qualidade deve ser um objetivo constante e deve ser inserida já nas **primeiras fases** do ciclo de vida.
- **Desafios:**
    - Complexidade dos produtos de software.
    - Software é invisível (a representação em diagramas pode ser imprecisa).
    - Não há consenso sobre o que é qualidade.

## 2. Padronização da Qualidade (Normas ISO)

- **ISO (International Organization for Standardization):** Cria sistemas de garantia de qualidade para que produtos e serviços satisfaçam as expectativas dos clientes.
- **SQuaRE (Software Product Quality Requirements and Evaluation):** Arquitetura de normas que reformulou a ISO/IEC 9126.

### ISO/IEC 25000 (SQuaRE)
Série de normas que unifica requisitos e avaliação da qualidade.

#### ISO/IEC 25010: Qualidade do Produto (8 Características)
A ISO/IEC 25010 (substituiu a ISO 9126 e adicionou **Segurança** e **Compatibilidade**) define as 8 características de qualidade de produto:

1.  **Adequação Funcional:** Funções que correspondam às necessidades.
2.  **Eficiência de Desempenho:** Desempenho em relação aos recursos utilizados.
3.  **Compatibilidade:** Capacidade de o sistema trocar informações e/ou realizar funções ao compartilhar o mesmo ambiente.
4.  **Usabilidade:** Capacidade de o sistema ser usado para o alcance de metas com eficácia, eficiência e satisfação.
5.  **Confiabilidade:** Capacidade de executar funções específicas sob condições determinadas, evitando falhas (Maturidade, Tolerância a Falhas, Recuperabilidade, Disponibilidade).
6.  **Segurança:** Capacidade de proteger informações e dados, garantindo o grau de acesso apropriado (Integridade, Confidencialidade, Não Repúdio, Autenticidade, Responsabilização).
7.  **Manutenibilidade:** Capacidade de o sistema ser modificado (melhorias, correções) com eficácia e eficiência.
8.  **Portabilidade:** Capacidade de o sistema ser transferido de um ambiente para outro.

#### ISO/IEC 25010: Qualidade em Uso (5 Características)
Avalia a qualidade do software na **perspectiva do usuário** quando operado.

1.  **Efetividade:** Capacidade de atender a metas específicas com exatidão e integridade.
2.  **Eficiência:** Grau de consumo de recursos pelo software ao atingir metas.
3.  **Satisfação:** Capacidade de agradar o usuário (Utilidade, Confiança, Prazer, Conforto).
4.  **Ausência de Riscos:** Grau de minimização de riscos econômicos, humanos, de saúde e ambientais.
5.  **Cobertura de Contexto:** Grau em que o software pode ser usado com satisfação em contextos específicos ou não explicitamente identificados.
---