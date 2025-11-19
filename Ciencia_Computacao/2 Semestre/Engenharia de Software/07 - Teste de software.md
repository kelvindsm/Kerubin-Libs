---
tags:
  - Naoconcluido
---
# Testes de Software

## O que é Teste de Software?

>[!info] Definição
>- É um **conjunto de atividades** executadas para **revelar erros** cometidos quando o software foi projetado e construído.

## Como Realizar os Testes: Estratégia e Roteiro

>[!question] Questões Iniciais
>- Devemos estabelecer um **plano formal**?
>- Devemos testar **todo o programa ou parte dele**?
>- Devemos realizar teste quando **adicionamos novo componente**?
>- Quando devemos envolver o Cliente?

### Estratégia de Teste
- Uma **Estratégia de Teste** é desenvolvida pelo **Gerente de Projetos**, pelos **Engenheiros de Software** e pelos **Especialistas em Testes**.
### O Roteiro de Teste
- É um roteiro que descreve **o que, quando e como testar**.
### Objetivo do Plano de Teste
- O objetivo do plano de teste é responder às questões:
    - **O que?** (Escopo e objeto de teste)
    - **Como?** (Nível e técnicas de teste)
    - **Quando?** (Momento do projeto)
    - **Quem?** (Participantes)
    - **Necessidades?** (Necessidades de recursos)
## Processo de Teste (Atividades)

As atividades de teste seguem a seguinte sequência:
1.  **Planejar Testes**
    - Planejamento de Testes inclui definir a Estratégia de Testes e a Revisão de Documentos.
2.  **Projetar Casos de Teste**
3.  **Executar Testes**
4.  **Coletar e Avaliar Dados**
## Quem Realiza os Testes?
- **Software Tester:** Pode atuar em qualquer nível de teste de software.
- **Software Developer:** Responsável pelos **testes unitários** e de **integração**.
## Verificação e Validação
- São tarefas essenciais para garantir a qualidade do software.
### Verificação
- **Conceito:** Tarefas que garantem que o software implementa corretamente uma função.
- **Foco:** O produto que estamos criando está **correto**?
- **Exemplos de Atividades (Verificação):**
    - Revisões Técnicas
    - Auditorias de Qualidade e Configuração
    - Revisão de Documentação
    - Análise de Algoritmo
    - Revisão do Desenho de Testes
    - Script de Testes
### Validação
- **Conceito:** Tarefas que asseguram que o software atende os requisitos do cliente.
- **Foco:** Estamos criando o **produto certo**?
### O V-Model (Verificação e Validação no Processo de Software)
- O V-Model relaciona as fases de desenvolvimento (Verificação) com os níveis de teste (Validação).

| Fase de Desenvolvimento (Verificação) | Nível de Teste (Validação) |
| :------------------------------------ | :------------------------- |
| Requisito                             | [[Teste de Aceitação]]     |
| Análise                               | [[Teste de Sistema]]       |
| Arquitetura                           | [[Teste Integração]]       |
| Código                                | [[Teste Unitário]]         |
## Níveis de Teste
### Teste Unitário
- **Objetivo:** Explorar a **menor unidade do projeto** (módulo), procurando provocar falhas ocasionadas por defeitos de lógica e de implementação em cada módulo, separadamente.
### Teste de Integração
- **Objetivo:** Visa provocar falhas associadas às interfaces entre os módulos quando esses são integrados para construir a estrutura do software.
### Teste de Sistema
- **Objetivo:** Avalia o software em busca de falhas por meio da utilização dele, como se fosse um **usuário final**. Os testes são executados com as mesmas condições e dados de entrada que um usuário utilizaria.
### Teste de Aceitação
- **Objetivo:** Verificar se o comportamento do sistema está de acordo com o solicitado.
- **Execução:** Realizados geralmente por um restrito grupo de **usuários finais** do sistema.
## Classificação dos Testes: O que, Quando e Como

A classificação nos ajuda a planejar e realizar melhor a atividade de teste.

| Categoria         | Questionamento       | Tipos e Técnicos                                                                   |
| :---------------- | :------------------- | :--------------------------------------------------------------------------------- |
| **O que testar**  | **Tipo de Teste**    | **Funcionalidade**, **Usabilidade**, **Desempenho**, **Segurança**                 |
| **Quando testar** | **Nível de Teste**   | **Unidade**, **Integração**, **Sistema**, **Aceitação**                            |
| **Como testar**   | **Técnica de Teste** | **Caixa Branca**, **Caixa Preta**, **Análise Estática**, **Heurística de Nielsen** |

## Relação entre Nível, Tipo e Técnica (Exemplos)

### Testar Componente de Software (Nível de Unidade)
>[!tip] Foco: Componente Individual
>- **Nível:** Teste Unitário
>- **Exemplo de Objetivo:** Quero saber se o componente que programei está funcionando, dentro dos padrões e recomendações.
>- **Técnicas Comuns:**
 >   - [[Caixa Branca]]
 >   - Análise Estática
 >   - Test Driven Development (TDD)

### Testar Comunicação entre as Partes (Nível de Integração)
>[!tip] Foco: Interfaces e Fluxos
>- **Nível:** Teste de Integração
>- **Tipo:** Integração
>- **Técnicas Comuns:**
 >   - Bottom-Up, Top-Down, Big-Bang
 >   - Integração com APIs, Comunicação com Banco de Dados

### Testar Desempenho (Nível de Sistema)
>[!tip] Foco: Performance e Volume
>- **Nível:** Teste de Sistema
>- **Tipos:** Performance e Volume
>- **Técnicas Comuns:**
 >   - [[Teste de Carga]]
 >   - [[Teste de Estresse]]

### Testar Interação Usuário e Software
>[!tip] Foco: Experiência do Usuário (UX)
>- **Nível:** Teste de Sistema ou Teste de Aceitação
>- **Tipos:** Teste de Usabilidade e de Acessibilidade
>- **Técnicas Comuns:**
 >   - [[Heurística de Nielsen]] (Usabilidade)
 >   - Teste Alpha e Teste Beta

### Testar Funcionalidades
>[!tip] Foco: Requisitos e Casos de Uso
>- **Nível:** Teste de Sistema e de Aceitação
>- **Tipo:** Funcional
>- **Técnicas Comuns:**
>	- [[Caixa Preta]]
>	- [[Homologação]]
>	- Revisão Formal ou Informal

### Testar Software Após Manutenção
>[!tip] Foco: Garantir que Mudanças Não Quebraram o Existente
>- **Níveis:** Unidade, Integração, Sistema e Aceitação
>- **Técnica:** [[Teste de Regressão]]

---
## Outros Tipos de Teste Importantes
- [[Portabilidade]]
- [[Instalação e Configuração]]
- [[Segurança]]
- [[Monitoração]]
- [[Contingência]]
---