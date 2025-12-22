---
tags:
  - Emprogresso
---

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
## Composição de uma classe
![[Pasted image 20251222120901.png|center|550]]

### Atributos
- São mostrados com pelo menos seu **nome**, e podem incluir seu tipo, valor inicial e outras propriedades.
- **Visibilidade:**
    - `+`: indica atributos **públicos**.
    - `#`: indica atributos **protegidos**.
    - `-`: indica atributos **privados**.
#### 1. Visibilidade
- Denota como um atributo, pode ser enxergado por outras classes
- Modificadores de visibilidade:
	- **Público (+)**: o elemento é visível por qualquer classe;
	- **Protegido (#)**: o elemento é visível na própria classe e pleas subclasses da classe;
	- **Pacote(~)**: o elemento é visível apenas pela própria classe ou dentro do pacote onde a classe está localizada;
	- **Privado(-)**: o elemento é visível apenas pela própria classe
	![[Pasted image 20251222143700.png|center|500]]
#### 2. Nome do atributo
- Representa o nome do atributo
![[Pasted image 20251222143758.png|center|500]]
#### 3. Tipo do atributo
- Representa o tipo do atributo: inteiro, booleano, String, Date...
![[Pasted image 20251222143822.png|center|500]]
#### 4. Multiplicidade
- Representa o limite inferior e superior da quantidade de objetos na qual um outro objeto pode ser associado...
![[Pasted image 20251222143854.png|center|500]]
![[Pasted image 20251222144023.png|center|250]]
#### 5. Valor default
- Valor padrão de um atributo caso ele seja omitido no momento da criação...
![[Pasted image 20251222144129.png|center|500]]
#### 6. Restrição
- Permite fornecer propriedades adicionais ao atributo
- Ex.: Lista de array deve ser ordenada...
![[Pasted image 20251222144205.png|center|550]]
#### 7. Escopo de atributo
- Instância
	- cada objeto tem o seu próprio valor;
	- Os atributos do objeto variam de acordo com a instanciação de cada objeto...
- Classe
	- Valor do atributo é comum a todos os objetos da classe
	- Para denotar dessa forma, usa-se o sublinhado
	- Atributo estático (*static*)
![[Pasted image 20251222144250.png|center|550]]
### 2. Operações (Métodos)
- São exibidos com pelo menos seu **nome**, e podem mostrar seus **parâmetros** e **valores de retorno**.

#### 1. Visibilidade:
- Denota como um método pode ser enxergado por outras classes:
	- **Público (+)**: o elemento é visível por qualquer classe;
	- **Protegido (#)**: o elemento é visível na própria classe e pelas subclasses da classe;
	- **Pacote (~)**: o elemento é visível apenas pela própria classe ou dentro do pacote onde a classe está localizada;
	- **Privado (-)**: o elemento é visível apelas pela própria classe.
	![[Pasted image 20251222145331.png|center|550]]
#### 2. Nome da operação
- Representa o nome da operação
![[Pasted image 20251222145428.png|center|550]]
#### 3. Parâmetros
- Representa os parâmetros da operação
![[Pasted image 20251222145645.png|center|550]]
#### 4. Tipo de retorno
- Representa o tipo do retorno
![[Pasted image 20251222145831.png|center|550]]
#### 5. Restrição
- Permite indicar propriedades adicionais
![[Pasted image 20251222145921.png|center|550]]
### Classes vs. Tipos
- Uma **Classe** define os atributos e os métodos de um conjunto de objetos.
- **Tipo** é um termo mais genérico e nem sempre é a mesma coisa que Classe.

---
## Relacionamentos Estáticos entre Classes
![[Pasted image 20251116140741.png|center|550]]
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