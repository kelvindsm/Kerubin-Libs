---
tags:
  - Emprogresso
  - NaoRevisado
---
# Modelagem UML para Análise e Especificação de Requisitos
## 1. Introdução à UML (Unified Modeling Language)
A [[UML (Unified Modeling Language)]] é uma linguagem gráfica de modelagem que serve como **padrão da indústria** para visualizar, especificar, construir e documentar artefatos de sistemas complexos.
- **Conceito:** É uma linguagem de modelagem, não um processo de desenvolvimento ou uma metodologia.
- **Modelo:** É uma simplificação (representação) da realidade. Modelar permite compreender melhor o sistema e documentar decisões de arquitetura e comportamento.
### Visões da UML
A UML é dividida em visões que cobrem diferentes aspectos do sistema:

| Visão da UML                            | Foco Principal                             | Tipo de Diagrama              |
| :-------------------------------------- | :----------------------------------------- | :---------------------------- |
| **Visão de Caso de Uso**                | Requisitos Funcionais, Comportamento.      | Diagrama de Casos de Uso.     |
| **Visão de Projeto (Estrutural)**       | Vocabulário, funcionalidade, estrutura.    | Diagrama de Classes, Objetos. |
| **Visão de Interação (Comportamental)** | Desempenho, escalabilidade, *throughput*.  | Sequência, Atividade, Estado. |
| **Visão de Implementação**              | Gerenciamento da configuração e montagem.  | Componente.                   |
| **Visão de Implantação**                | Topologia do sistema, distribuição física. | *Deployment*.                 |

---
## 2. Diagrama de Casos de Uso

O [[04 - Diagrama de caso de uso|Diagrama de Casos de Uso (Use Case Diagram)]] é o modelo mais importante para a [[01 - Contextualização da engenharia de requisitos|Engenharia de Requisitos]], pois é o principal elemento de **modelagem funcional** do sistema.
>[!info] Objetivo Principal
> Descrever um modelo funcional do sistema, identificando os usuários e representando o sistema segundo a **visão do usuário**.
### Elementos do Diagrama de Caso de Uso
1.  **Ator (Actor):**
    - **Definição:** Alguém ou alguma coisa que interage com o sistema. É quem ou o que usa o sistema.
    - **Representação:** Boneco (*stick figure*).
	    ![[Pasted image 20251202120535.png|center|150]]
    - **Função:** O ator representa um **papel**, não um usuário individual. Podem ser pessoas (usuário, atendente) ou outros sistemas automatizados (sistema de pagamento).
2.  **Caso de Uso (Use Case):**
    - **Definição:** Uma **sequência de ações** que o sistema executa e que produz um **resultado de valor para um ator específico**.
    - **Representação:** Elipse.
    - ![[Pasted image 20251202120621.png|center|350]]
    - **Foco:** Descreve um **serviço do sistema** (*o que o sistema faz*), não como o sistema o faz.
3.  **Limite do Sistema (*Boundary*):**
    - **Definição:** Delimita o escopo (o que está dentro e fora) do sistema.
    - **Representação:** Retângulo que envolve os casos de uso.
### Relacionamentos em Casos de Uso
Os relacionamentos ajudam a reestruturar o diagrama para melhor demonstrar o encadeamento das funções.

| Relacionamento               | Representação                        | Semântica                                                                                                    |
| :--------------------------- | :----------------------------------- | :----------------------------------------------------------------------------------------------------------- |
| **Associação**               | ![[Pasted image 20251202121004.png]] | Conexão entre o **Ator** e o **Caso de Uso**.                                                                |
| **Inclusão (`<<include>>`)** | ![[Pasted image 20251202120812.png]] | Representa um comportamento obrigatório que **sempre** será executado pelo Caso de Uso base.                 |
| **Extensão (`<<extend>>`)**  | ![[Pasted image 20251202120840.png]] | Representa um comportamento **opcional** ou que ocorre sob uma condição específica (Ex: Tratamento de erro). |
| **Generalização**            | ![[Pasted image 20251202120920.png]] | Representa herança entre Atores (Ex: Administrador herda de Usuário) ou entre Casos de Uso.                  |

---
## 3. Especificação de Casos de Uso (UML)
A [[03 - Casos de uso e Requisitos Não Funcionais|Especificação de Caso de Uso]] é a descrição **narrativa textual** das interações que ocorrem entre os elementos externos (Ator) e o sistema.
- **Diagrama vs. Especificação:** Enquanto o [[04 - Diagrama de caso de uso|diagrama]] representa a visão **gráfica** e macro do usuário, a especificação é o detalhamento **textual** das interações.
- **Modelo Padrão:** A UML não define uma estrutura textual única, mas a boa prática exige: Identificação, Atores, Descrição, Pré-condição, Fluxo Principal, Fluxos Alternativos e Pós-condição.
### Componentes da Especificação
1.  **Identificação e Descrição Geral:** Título, ID, Atores, Descrição sucinta.
2.  **Pré-condição:** Condições que devem ser verdadeiras para que o caso de uso possa ser iniciado.
3.  **Fluxo Principal (Básico):**
    - **Definição:** Sequência de passos que representa o **caminho ideal e mais provável** do sucesso.
    - **Estrutura:** Usa duas colunas (Ações do Ator vs. Ações do Sistema) para detalhar a interação.
4.  **Fluxos Alternativos:**
    - **Definição:** Variações do fluxo principal que também terminam em sucesso, mas por um caminho diferente.
5.  **Fluxos de Exceção:**
    - **Definição:** Sequências que representam erros, falhas ou condições que fazem o caso de uso **terminar sem sucesso** (ou retornar a um ponto anterior).
6.  **Pós-condição:** Estado do sistema e do ambiente após o caso de uso ser concluído com sucesso.

---
## 4. Diagrama de Classes
O [[05 - Diagrama de Classes UML|Diagrama de Classes (Class Diagram)]] é o principal artefato para a **visão estática e estrutural** de um sistema em UML.
- **Objetivo:** Visualizar as classes que irão compor o sistema, seus **atributos** e **métodos (operações)**, e como elas se relacionam.
- **Foco:** Representa a **estrutura lógica** e serve de base para os demais diagramas da UML.
### Componentes de uma Classe
Uma classe é representada por um retângulo dividido em três compartimentos:
1.  **Nome da Classe:** No topo.
2.  **Atributos:** Características da classe.
    - **Notação de Visibilidade:**
        - **`+` (Público):** Acessível a qualquer classe.
        - **`-` (Privado):** Acessível apenas dentro da própria classe.
        - **`#` (Protegido):** Acessível na classe e em suas subclasses.
3.  **Métodos (Operações):** Comportamentos da classe (funções que a classe pode executar).

>[!tip] Persistência
> **Nem toda classe** é ou precisa ser **persistente** (ter um equivalente em tabela de banco de dados). Classes de controle ou interface (ex: `Controlador_Banco`) não são geralmente persistentes.
### Relacionamentos em Diagramas de Classe

| Relacionamento                       | Representação                                                                                                                                                                              | Semântica                                                                                                      |
| :----------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------- |
| **Associação**                       | Linha contínua.                                                                                                                                                                            | Conexão estrutural entre duas classes. Indica que uma classe interage com a outra.                             |
| **Multiplicidade**                   | Indica o número de instâncias de uma classe que se relacionam com as instâncias da outra. (*Ex:* `1..*` (um para muitos), `1` (exatamente um)).                                            |                                                                                                                |
| **Agregação (Diamante Vazado)**      | Forma de associação **"todo-parte"**, onde as partes podem existir independentemente do todo. (*Ex:* Uma *Ordem de Serviço* tem *Itens*, mas os *Itens* podem existir fora da ordem).      |                                                                                                                |
| **Composição (Diamante Preenchido)** | Forma de agregação **forte**. As partes **não podem existir** sem o todo. (*Ex:* Uma *Conta Bancária* é composta por *Transações*. Se a conta é excluída, as transações também devem ser). |                                                                                                                |
| **Generalização (Herança)**          | Linha com seta fechada e vazia, apontando para a **Superclasse (Geral)**.                                                                                                                  | Indica que uma subclasse herda atributos e métodos da superclasse (Ex: *Pessoa Física* é um tipo de *Pessoa*). |
| **Realização (Interface)**           | Seta pontilhada com seta fechada e vazia.                                                                                                                                                  | Uma classe implementa as operações definidas em uma [[Interface]].                                             |

---