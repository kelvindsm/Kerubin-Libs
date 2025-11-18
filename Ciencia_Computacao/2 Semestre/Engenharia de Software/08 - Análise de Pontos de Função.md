---
tags:
  - Naoconcluido
---

# Análise de Pontos de Função (APF)

## Análise de Pontos de Função (APF): Conceito e Objetivos

>[!info] Definição
> - É o **método-padrão** para a medição do desenvolvimento de software.
> - Visa estabelecer uma medida de **tamanho do software em Pontos de Função (PFs)**, baseada na **funcionalidade** a ser implementada, sob o **ponto de vista do usuário**.
> - A contagem é feita **sem se preocupar com a tecnologia** que será utilizada na implementação.

### Objetivos da APF
- Medir as **funcionalidades** do sistema requisitadas e recebidas pelo usuário.
- Medir projetos de desenvolvimento e manutenção de software.
- Melhorar as **estimativas** de projetos de desenvolvimento de softwares.
- Criar uma **unidade padrão de medida** de software.
- Comparar a **produtividade** entre ambientes de desenvolvimento: $P=\frac{PF}{Esforço}$.
---
## Procedimento para Contagem de PFs

O processo de contagem é dividido em etapas sequenciais:

1.  Determinar o **Tipo de Contagem**.
2.  Identificar o **Escopo** e **Fronteira** da Aplicação.
3.  Contagem das **Funções de Dados**.
4.  Contagem das **Funções Transacionais**.
5.  Determinar o **Fator de Ajuste (VAF)**.
6.  Calcular os **PFs Ajustados**.
### Etapa 2: Escopo e Fronteira
- **Fronteira**: Indica o limite entre o software que está sendo medido e o usuário.
    - Define o que é externo à aplicação.
    - É dependente da visão de negócio externa do usuário e **independente de considerações técnicas**.
---
## Contagem das Funções (PFs Não Ajustados)

A contagem não ajustada é feita a partir de Funções de Dados e Funções de Transação.
### Funções de Dados
- **ILF (Internal Logical File)**
    - Entidade lógica e persistente que **mantém os dados que sofrem manutenção dentro da Fronteira da Aplicação**.
- **EIF (External Interface File)**
    - Entidade lógica e persistente que é **mantida dentro da fronteira de outra aplicação**.
#### Tabela de Conversão (Exemplo de PFs Não Ajustados)
| Complexidade | ILF | EIF |
| :----------- | :-- | :-- |
| Baixa        | 7   | 5   |
| Média        | 10  | 7   |
| Alta         | 15  | 10  |
### Funções de Transação
- **EI (External Input)** (Entrada Externa): Processo lógico que **mantém os dados em um ou mais arquivos lógicos internos**.
- **EO (External Output)** (Saída Externa): Processo lógico que **gera dados para um usuário ou para outro aplicativo externo**.
- **EQ (External Query)** (Consulta Externa): Processamento lógico que **não contém fórmulas ou cálculos** nem cria dados derivados.
#### Tabela de Conversão (Exemplo de PFs Não Ajustados)
| Complexidade | EI e EQ | EO  |
| :----------- | :------ | :-- |
| Baixa        | 3       | 4   |
| Média        | 4       | 5   |
| Alta         | 6       | 7   |

---
## Cálculo dos Pontos de Função Ajustados (AFP)

### Etapa 5: Fator de Ajuste (VAF)
- **Fator de Ajuste de Valor (VAF)**: Passo final que avalia restrições de negócio adicionais **não consideradas** pelos cinco tipos de funções.
- Baseado na influência de **14 Características Gerais do Sistema**.
#### Fórmula do VAF
$$VAF = 0,65 + (0,01 \times Nt(total))$$
O VAF deve estar entre 0,65 e 1,35.
### Etapa 6: Ajustar a Contagem
O valor final dos Pontos de Função Ajustados (AFP) é:
$$\text{AFP} = \text{ADD} \times \text{VAF}$$
Onde ADD é a contagem não ajustada das funções do projeto.
### Aplicações da FPA (Estimativas)
- **Esforço de Desenvolvimento**: Produtividade $(\text{H/PF}) \times$ Tamanho $(\text{PF})$.
- **Custo de Software**: Tamanho $(\text{PF}) \times$ Custo $(\text{R\$/PF})$.
---