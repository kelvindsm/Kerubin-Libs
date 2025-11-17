---
tags:
  - OrgArc2306
---
# Conceito de programa armazenado
>[!quote] Ideia central
>Refere-se à ideia de armazenar um programa de computador em sua memória principal;

Abordagem padrão usada atualmente - mas não usada desde sempre:
- Inicialmente, imperava a noção de que os dados eram armazenados na memória e os programas eram parte da CPU (para alterações no programa, eram necessárias alterações nos circuitos da CPU)

Conceito implementado às CPU's ocasionou na criação da Arquitetura de Von Neumann
Com essa arquitetura, a Unidade de Controle é projetada para:
1. Extrair o programa da memória
2. Decodificar as instruções, e
3. executá-las.
- Dessa forma, o programa que a máquina segue pode ser modificado simplesmente por meio da modificação do conteúdo da memória do computador, não havendo necessidade de reconfiguração da CPU (alteração física no chip).
---
# Linguagem de máquina

>[!Cite] .
>Para aplicar o conceito de programa armazenado, as CPU's são projetadas para reconhecer instruções codificadas como padrão de bits

Essa coleção de instruções, juntamente com o sistema de codificação, é chamada de linguagem de máquina. Uma instrução expressa nessa linguagem é chamada de "instrução no nível de máquina" ou mais comumente por "instrução de máquina".
>[!n] Síntese
>- Linguagem de máquina é a linguagem em coleções de bits junto com o sistema de codificação para realizar a conversa entre software e hardware. Por ser a forma mais "simples" de conversa da máquina (pois são apenas bits e comandos), é definido como uma linguagem de baixo nível.

A lista de instruções de máquina que uma CPU comum precisa ser capaz de decodificar e e executar é bastante curta.

Uma vez que a máquina possa realizar certas tarefas básicas, mas bem selecionadas, e a adição de mais recursos não aumenta as capacidades teóricas da máquina

**Assim, recursos adicionais podem aumentar certas facilidades como a conveniência, mas não adicionam nada às funcionalidades fundamentais da máquina.** A forma como o projeto de máquinas tira proveito desse fato levou duas filosofias de arquitetura de CPU's.

--- 
# Arquitetura RISC e CISC

### RISC

- **A CPU deve ser projetada para executar um conjunto mínimo de instruções de máquina.** Essa abordagem levou o conhecimento de "Computador com conjunto reduzido de instruções (RISC)"
- O argumento a favor dessa arquitetura é a eficiência da máquina: *maior velocidade, menos dispendiosa para ser fabricada e consumo reduzido de energia.*
### CISC
- **São CPU's com a habilidade de executar um grande número de instruções complexas - mesmo que muitas sejam redundantes.** O resultado dessa abordagem é conhecida como "Computador com conjunto complexo de instruções"
- O argumento a favor dessa arquitetura é que uma *CPU mais complexa pode lidar melhor com as complexidades cada vez maiores dos sistemas de softwares atuais;*
- Com CISC, **os programas podem explorar um rico e poderoso conjunto de instruções, muitas das quais requereriam uma sequência de múltiplas instruções em um projeto RISC;**
### RISC x CISC
- Os **processadores Intel, usados em pc's, são exemplo de arquiteturas CISC**
- A arquitetura CISC assegura seu lugar nos computadores de mesa (desktops); Consomem quantidade maior de energia elétrica;
- Os processadores PowerPC (Apple, IBM e Motorola) são exemplos de arquiteturas RISC, foram usados no Macintosh da Apple
>[!note] Síntese
>**Arquitetura RISC é mais usada em smartphones** (pois consome menos enegia). A ARM é uma companhia que desenvolve diversos designs desse tipo de processador.
>
>**Arquitetura CISC é mais fácilmente encontrada em computadores de mesa** (desktops) onde as operações complexas são mais necessárias.

---
# Instrução de máquina
> [!info] 
> Independentemente da escolha entre RISC e CISC, as instruções de uma máquina podem ser categorizadas em três grupos:
>
> 1. o grupo de transferência de dados
> 2. o grupo de lógica e aritmética 
> 3. o grupo de controle

### Passos para somar valores armazenados em memórias
1. Obtenha um dos valores a ser somado e coloque-o em um registrador
2. Obtenha da memória  o outro valor a ser somado e coloque-o em outro registrador
3. Ative os circuitos de adição com os registradores usados nos 1 e 2 como entrada e outro registrador selecionado para guardar o resultado
4. Armazene o resultado na memória
5. Pare.
### 1. Grupo de instruções para transferência de dados

>[!quote] Conceito
>- O grupo de transferência de dados **compreende instruções relativas ao movimento de dados de uma localidade a outra;**
>- O processo envolvido em uma instrução de transferência **é mais parecido com uma cópia de dados do que com uma movimentação real;** 

>[!note] Definições
>- Instrução de carga(LOAD): Requisição que **preenche um registrador de propósito geral com o conteúdo de uma célula de memória** 
>- Instrução de armazenamento (STORE): requisição **para transferir o conteúdo de um registrador para uma célula de memória.**
>  
1. Obtenha da memória um dos valores a ser somado e coloque-o em um registrador
2. Obtenha da memória o outro valor a ser somado e coloque-o em outro registrador
3. Ative os circuitos de adição com os registradores usados no 1 e 2 como entrada e outro registrador selecionado para guardar o resultado
4. Armazene o resultado na memória 
5. Pare.
>[!tip] Nota
>- Os passos 1 e 2 são instruções LOAD, e o passo 4 é uma instrução STORE. *São exemplo do grupo de transferência de dados.*
>
>	>[!quote] Definição
>	>- Instrução de carga(LOAD): Requisição que **preenche um registrador de propósito geral com o conteúdo de uma célula de memória**  
>	>- Instrução de armazenamento (STORE): requisição **para transferir o conteúdo de um registrador para uma célula de memória.**


### 2. Grupo de instruções de lógica e aritmética
1. Obtenha da memória um dos valores a ser somado e coloque-o em um registrador
2. Obtenha da memória o outro valor a ser somado e coloque-o em outro registrador 
3. Ative os circuitos de adição com os registradores usados nos passos 1 e 2 como entrada e outro registrador selecionado para guardar o resultado
4. Armazene o resultado na memória
5. Pare
>[!tip] Nota
>- O grupo de lógica e aritmética é utilizado quando a unidade de controle requisita uma atividade da unidade de lógica e aritmética
>	- O passo 3 do procedimento acima se encaixa nesse grupo
>	
>- Além das operações de lógica e aritmética. existem operações que permitem que o conteudo dos registradores seja movido para a direita ou para a esquerda dentro do registrador (Operações SHIFT pu ROTATE)
---

### 3. Grupo de controle
> [!quote] Definição
> - O grupo de controle consiste nas instruções que direcionam a execução do programa.
> - Contém algumas das instruções mais interessantes de uma máquina, como: família de instruções de salto JUMP, usadas para direcionar a CPU a executar uma instrução que não seja próxima da lista.
> 	> [!note] Aparecem em duas variedades: saltos incondicionais e condicionais
> 	> - Incondicionais: "Pular para o passo 5"
> 	> - Condicionais: "Se o valor for 0, pular para o passo 5"
#### Exemplo 1: adição de valores
1. Obtenha da memória um dos valores a ser somado e coloque-o em um registrador
2. Obtenha da memória o outro valor a ser somado e coloque-o em outro registrador
3. Ative os circuitos de adição com os registradores usados nos Passos 1 e 2 como entrada e outro registrador selecionado para guardar o resultado
4. Armazene o resultado na memória
5. Pare
 >[!Note] .
>- **O grupo de controle é utilizado para conduzir a execução do programa;**
>- O passo 5 se encaixa no grupo dos incondicionais, mesmo sendo básico.
#### Exemplo 2: Divisão de valores armazenados na memória
1. Carregar (LOAD) um registrador com um valor da memória
2. Carregar (LOAD) outro registrador com outro valor da memória
3. Se esse segundo valor for zero, saltar (JUMP) para o passo 6
4. Dividir o conteúdo do primeiro registrador pelo segundo registrador e armazenar o resultado em um terceiro registrador
5. Armazenar (STORE) o conteúdo do terceiro registrador na memória
6. Parar (STOP)
> [!Note] .
> - **O grupo de controle é utilizado para conduzir a execução do programa;**
> - Como um exemplo, a sequência de instruções acima representa um algoritmo de divisão entre dois valores. **O passo 3 é um passo condicional que evita uma possível divisão por zero.**

---