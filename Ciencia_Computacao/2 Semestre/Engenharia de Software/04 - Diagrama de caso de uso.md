# Diagrama de Caso de Uso (UML)

## Conceito e Propósito do Diagrama

>[!info] Definição
> - Descreve os **relacionamentos e dependências** entre um grupo de **Caso de Uso** e os **Atores** participantes no processo.
> - É feito para facilitar a **comunicação** com os futuros usuários e clientes.
> - É especialmente útil para **determinar os recursos necessários** que o sistema deve ter.
> - Diagramas de Caso de Uso dizem **o quê** o sistema deve fazer, mas **não especificam como** isto será conseguido.
> - **Limitação:** Não são adequados para representar o desenho, e não podem descrever os mecanismos internos de um sistema.

---

## Caso de Uso e sua Descrição

### Caso de Uso
- Descreve, do ponto de vista dos atores, um grupo de **atividades num sistema** que produz um **resultado concreto e tangível**.
- São descrições de **interações típicas** entre os usuários de um sistema e o sistema propriamente dito.
- Representam a interface externa do sistema e especificam um conjunto de exigências do que o sistema deve fazer.
- Em um diagrama de caso de uso, são **representados por elipses**
### Regras do Caso de Uso
1.  Cada Caso de Uso está relacionado com **no mínimo um ator**.
2.  Cada Caso de Uso possui um **iniciador (isto é, um ator)**.
3.  Cada Caso de Uso liga-se a um **resultado relevante** (um resultado com "valor de negócio").
### Descrição do Caso de Uso
- São **narrativas de texto** do Caso de Uso.
- Explicam o processo ou atividades que tomarão lugar no Caso de Uso.

---
## Relacionamentos entre Casos de Uso
### 1. Associação de Inclusão («include»)
- **Notação**: «include».
- **Significado**: Especifica que um Caso de Uso toma lugar **dentro** de outro Caso de Uso.
- **Implicação**: Ao executar o caso de uso **A**, executa-se **também** o caso de uso **B**.
- **Natureza**: Indica que B é **essencial** para o comportamento de A. Pode ser dito que B *é parte de* A.
- **Exemplo**: *Processar Pedido* «include» *Emitir Nota Fiscal*.
![[Pasted image 20251116123220.png | center | 350 ]]
### 2. Associação de Extensão («extend»)
- **Notação**: «extend».
- **Significado**: Especifica que em determinadas situações, ou em algum **ponto de extensão**, um Caso de Uso será **estendido** por outro.
- **Implicação**: Ao executar o caso de uso **A**, **não necessariamente** o caso de uso **B** será executado.
- **Natureza**: O Caso de Uso B **pode ser acrescentado** para descrever o comportamento de A, mas **não é essencial**.
- **Ponto de Extensão**: Uma indicação no Caso de Uso original de que outros Casos de Uso poderão ser adicionados. O Caso de Uso invocado verificará se suas extensões devem ou não ser invocadas.
![[Pasted image 20251116123327.png | center |400]]
### 3. Generalização (Herança) entre Casos de Uso
- **Significado**: Especifica que um Caso de Uso herda as características do "Super" Caso de Uso.
- **Funcionalidade**: O caso de uso herdado pode **sobrepor** algumas características ou **adicionar novas**, de maneira semelhante à herança entre classes.
---
## Ator
### Definição
- É uma **entidade externa (fora do sistema)** que interage com o sistema participando (e frequentemente iniciando) um Caso de Uso.
- Podem ser **pessoas reais** (usuários), **outro sistema de computador** ou **eventos externos**.
- Atores não representam a pessoa física ou sistemas, mas sim sua **regra**.
### Regras Múltiplas
- Se uma pessoa interage com o sistema de diferentes maneiras (assumindo diferentes regras), ela será representada por **diversos atores**.
- **Exemplo:** Uma pessoa que fornece suporte ao cliente por telefone e recebe ordens pode ser representada por um ator da "Equipe de Suporte" e um ator "Representante de Vendas".
### Relacionamento entre Atores
- **Generalização**: Especifica que um ator (subclasse, ex: Ator B) herda as características do "Super" Ator (superclasse, ex: Ator A).
- Os casos de uso do Ator B são também casos de uso do Ator A.
- O Ator A tem seus próprios casos de uso.
![[Pasted image 20251116124626.png|center|350]]
### Relacionamento Ator e Caso de Uso
- **Associação**: Define uma **funcionalidade do sistema do ponto de vista do usuário**.
![[Pasted image 20251116124718.png|center|350]]
---