# Modelagem de Processo: Fundamentos de OO e UML

## Por Que Orientação a Objetos (OO)?

### Cenário Atual (Problemas no Modelo Tradicional)
O desenvolvimento de software tradicional enfrentava problemas como:
- **[[Levantamento de Requisitos]]**: Requisitos importantes eram esquecidos.
- **Validação com o Usuário**: O usuário frequentemente não validava, pois não compreendia o que foi modelado.
- **Desenvolvimento**: Havia excesso ou falta de documentação.
- **Prazo**: Cronograma apertado resultava em prazo estourado.
- **Entrega Final**: Resultava em cliente insatisfeito e horas infindáveis de manutenção corretiva.
### Foco da Orientação a Objetos
A modelagem em OO busca focar em **Objetos** (o mundo real), em contraste com a **Análise Estruturada**, cujo foco principal era em **Funções**.
### Benefícios da Modelagem OO
O que se busca ao modelar orientado a objetos:
- Diminuição do **tempo e custo de desenvolvimento**.
- Atendimento da demanda gerada pela evolução tecnológica.
- **[[Reutilização de Código]]** e facilidade de **manutenção**.
---
## [[UML (Unified Modeling Language)]]
### Surgimento
- Na Década de 90, os métodos de **Booch** (Grady Booch), **OMT** (Rumbaugh) e **OOSE** (Jacobson) eram os principais.
- Os três autores unificaram seus métodos, criando a UML.
- **UML (Unified Modeling Language)** Versão 1.1 foi padronizada pelo **[[OMG (Object Management Group)]]** em Novembro de 1997.
### Conceito
- UML é uma **Linguagem Gráfica**.
- **UML não é uma Metodologia**: Ela diz o que pode ser feito, mas não diz como deve ser feito (é independente de processo).
- **Metodologia** = UML + MÉTODO.
---
## Estrutura da UML
### Elementos Básicos do Modelo
- **Estruturais**: classes, interfaces, colaborações, casos de uso, classes ativas, componentes, nós.
- **Comportamentais**: interação, estado.
- **Agrupamento**: pacotes.
- **Anotacionais**: notas.
- **Relacionamentos**: dependência, associação, generalização, realização.
### Classificação dos Diagramas

| Diagramas Estáticos                                       | Diagramas Dinâmicos                                            |
| :-------------------------------------------------------- | :------------------------------------------------------------- |
| **[[05 - Diagrama de Classes UML\|Diagrama de Classes]]** | **[[04 - Diagrama de caso de uso\|Diagrama de Casos de Uso]]** |
| **[[05 - Diagrama de Classes UML\|Diagrama de Objetos]]** | Diagramas de Interação (Sequência e Colaboração)               |
| Diagrama de Implementação                                 | **[[Diagrama de Atividade]]**                                  |
| Diagrama de Componentes                                   | **[[Diagrama de Gráfico de Estados]]**                         |
| Diagrama de Implantação                                   | -                                                              |

---
## Detalhamento dos Diagramas
### 1. [[04 - Diagrama de caso de uso|Diagrama de Casos de Uso]]
- **Enfoque**: Análise de Requisitos.
- **[[04 - Diagrama de caso de uso|Caso de Uso]]**: É uma sequência de ações executadas com o objetivo de atingir um propósito.
- **Cenário Principal**: O fluxo perfeito.
- **Cenários Alternativos**: Alternativas do fluxo principal ou exceções, cruciais para o desenvolvimento.
- **Relacionamentos**: Inclui `<<extends>>` e `<<include>>`.
- **Melhoria**: Descrição concisa, sem ambiguidades. Protótipos melhoram o entendimento.
- **Ligação com Outros Diagramas**: Serve de entrada para o Diagrama de Classes, Diagramas de Interação e Diagrama de Atividades.
### 2. Diagrama de Classes
- **Fases**: Abrange as fases de Análise e Projeto.
- **Objetivo**: Modelagem de classes e seus relacionamentos.
- A análise dos casos de uso permite **identificar classes e atributos** (primeira abstração).
### 3. Diagrama de Sequências (Interação)
- **Tipo**: Diagrama de Interação.
- **Objetivo**: Representação dos cenários de um caso de uso, mostrando a **troca de mensagens entre objetos** em uma **sequência temporal**.
### 4. Diagrama de Colaboração (Interação)
- **Tipo**: Diagrama de Interação.
- **Objetivo**: Enfatiza a **colaboração entre objetos** sem identificar a sequência temporal.
### 5. Diagrama de Atividades
- **Objetivo**: Focaliza um **fluxo de atividades** que ocorrem para um determinado processamento (como um caso de uso ou uma operação).
### 6. Diagrama de Gráfico de Estados
- **Objetivo**: Descreve o **comportamento de objetos** por meio de **sequências de estados e ações** que ocorrem durante a sua vida.
### 7. Diagrama de Componentes (Implementação)
- **Tipo**: Diagrama de Implementação.
- **Objetivo**: Mostra a **estrutura de componentes** (como *Pedidos.class*).
### 8. Diagrama de Implantação (Implementação)
- **Tipo**: Diagrama de Implementação.
- **Objetivo**: Mostra a **configuração de elementos de processamento em tempo de execução** (nós como *Servidor de Aplicações*) e os componentes de software que neles são executados.
---