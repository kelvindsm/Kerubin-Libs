# Análise de Sistemas Orientada a Objeto: Diagrama de Classes

## O Diagrama de Classes na UML

>[!info] Definição e Importância
> - É o diagrama **mais utilizado** e o **mais importante** da [[UML (Unified Modeling Language)]], servindo de apoio para a maioria dos outros diagramas.
> - Define a **estrutura das classes** utilizadas pelo sistema, determinando os **atributos** e **métodos** de cada classe.
> - Estabelece como as classes **se relacionam e trocam informações** entre si.
### Diagrama Estático
- Diagramas de Classe são chamados diagramas **"estáticos"** porque mostram classes, seus métodos e atributos, e os **relacionamentos estáticos** entre elas.
- Eles mostram quais classes "conhecem" ou quais classes "são parte" de outras classes, mas **não mostram a troca de mensagens** (comportamento dinâmico) entre elas.
---
## Elementos de uma Classe (Desenho)
- Em UML, classes são representadas por **retângulos**.
- O retângulo pode mostrar o nome da classe, e, em compartimentos inferiores, os atributos e as operações (métodos) da classe.
![[Pasted image 20251116140706.png|center|350]]
### 1. Atributos
- São mostrados com pelo menos seu **nome**, e podem incluir seu tipo, valor inicial e outras propriedades.
- **Visibilidade:**
    - `+`: indica atributos **públicos**.
    - `#`: indica atributos **protegidos**.
    - `-`: indica atributos **privados**.

### 2. Operações (Métodos)
- São exibidos com pelo menos seu **nome**, e podem mostrar seus **parâmetros** e **valores de retorno**.
- **Visibilidade:**
    - `+`: indica operações **públicas**.
    - `#`: indica operações **protegidas**.
    - `-`: indica operações **privadas**.

### Classes vs. Tipos
- Uma **Classe** define os atributos e os métodos de um conjunto de objetos.
- **Tipo** é um termo mais genérico e nem sempre é a mesma coisa que Classe.

---

## Relacionamentos Estáticos entre Classes
![[Pasted image 20251116140741.png|center|450]]
### 1. Generalização (Herança)
- É um conceito fundamental da [[Programação Orientada a Objetos]] (POO).
- Uma classe (derivada) "ganha" todos os atributos e operações da classe que herda (base), podendo sobrepor, modificar ou adicionar novos membros.
- **Representação UML:** Uma linha conectando duas classes, com uma **seta vazada** no lado da **classe base** (ou superclasse).
![[Pasted image 20251116140859.png|center|150]]
### 2. Associação
- Representa um **relacionamento** entre classes.
- É o mecanismo que permite aos objetos **comunicarem-se entre si**.
- **Regra**: Pode especificar o propósito da associação (uni ou bidirecional).
- **Multiplicidade**: Dita quantos objetos em um lado da associação podem se relacionar com o outro lado.
    - Exibida como um intervalo `[min...máx]`.
    - `*` (asterisco) no lado máximo representa **infinito**.
- **Representação UML**: Linhas conectando as classes, podendo mostrar a regra e a multiplicidade.
![[Pasted image 20251116141221.png|center|350]]
### 3. Agregação ("Todo-Parte" Fraco)
- É um tipo especial de associação que forma um relacionamento **"todo-parte"**.
- Descreve como a classe que possui a regra do **todo** é composta (tem) de outras classes (as partes).
- A classe que age como o todo sempre tem uma multiplicidade de **um**.
- **Representação UML**: Uma associação com um **romboide vazado (diamante branco)** no lado do todo.
![[Pasted image 20251116141246.png|center|350]]
### 4. Composição ("Todo-Parte" Forte)
- Associações que representam **agregações muito fortes**.
- O relacionamento é tão forte que as **partes não podem existir de forma independente**.
- Se o todo é destruído, as partes morrem junto.
- **Representação UML**: Um **romboide sólido (diamante preto)** no lado do todo.
![[Pasted image 20251116141321.png|center|350]]
---
## Outros Elementos de Modelagem

### Interface
- Classes **abstratas** que significam que **instâncias não podem ser diretamente criadas delas**.
- Podem conter operações (métodos) mas **não podem conter atributos**.
- Classes podem derivar de interfaces (através da realização de uma associação).
![[Pasted image 20251116141342.png|center]]
### Diagrama de Objetos
- Está amplamente associado e é um **complemento** do Diagrama de Classes.
- Fornece uma **visão dos valores armazenados pelos objetos** de um Diagrama de Classes em um **determinado momento** da execução de um processo.
![[Pasted image 20251116141413.png|center|350]]
### Outros Tipos
- **Tipos de Dados**: Primitivos que são tipicamente construídos em uma linguagem (ex: inteiros, lógicos).
- **Enumerações**: Uma lista simples de valores, cujas opções são chamadas Literais de Enumeração (ex: dias da semana).
- **Pacotes**: Representam um **espaço de nomes** e são usados para representar partes de um sistema que contêm várias classes.
---