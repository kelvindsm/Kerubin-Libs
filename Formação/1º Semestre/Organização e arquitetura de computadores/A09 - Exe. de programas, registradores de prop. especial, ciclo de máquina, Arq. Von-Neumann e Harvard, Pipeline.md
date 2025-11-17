---
tags:
  - OrgArc2306
aliases:
  - Execução de programas, registradores de propósito especial, ciclo de máquina, Arquitetura Von-Neumann e Havard, Conceitos de Pipeline em processadores
---
# Execução de programas
 - Um computador executa um programa armazenado em sua memória
	- Para tal, copia as instruções da memória para a CPU, sempre que necessário
 - Uma vez na CPU, cada instrução é decodificada e executada
# Registradores de propósito especial
Deve-se considerar dois tipos de registradores de proposito especial:
- Registrador de instruções: usado para manter a instrução que está em execução
- Contador de programa: contém o endereço da próxima instrução a ser executada que serve como guia para que a máquina acompanhe o ponto em que está no programa
# Ciclo de máquina
Os três passos são:
## 1. Obter
- A CPU requisita que a memória principal forneça a ela a instrução que está armazenada no endereço indicado pelo contador de programa
- Esse processo envolve recuperar o conteúdo a partir da memória principal
- A CPU coloca a instrução recebida da memória em seu registrador de instruções e, então, incrementa o contador de programa, de forma que o contador contenha o endereço da próxima instrução armazenada na memória
- **Obtém a próxima instrução da memória (conforme indicado pelo contador de programa ) e incrementa o contador de programa**
## 2. Decodificar
- Após buscar a instrução da memória, a CPU decodifica a instrução - o que envolve quebrar o campo de operando em seus componentes apropriados
- **Decodifica o padrão de bits no registrador de instruções**
## 3. Executar
- Realiza a operação solicitada pela instrução no registrador de instruções
# Harvard x Von Neumann
## Harvard
- Caracterizada por dois barramentos internos, sendo um de instruções e outro de dados, sendo considerada uma arquitetura "paralela";
- Produz um conjunto simples de códigos de instruções, e por causa de seu paralelismo, é capaz de executar apenas uma instrução por ciclo de clock.
- Precisa de mais linhas de código para executar a mesma tarefa executada numa arquitetura Von Neumann 
## Von Neumann
- Existe apenas um barramento interno por onde circulam instruções e dados
- Permite produzir um conjunto complexo de códigos de instruções para o processador (CISC), com um tempo de execução por instrução de vários ciclos de clock;
- Mais simples, com menor número de portas lógicas, porém, sua velocidade é menor que a Harvard
>[!Note] Síntese
>- A arquitetura Harvard utiliza as instruções RISC, por possuir um conjunto mais simples de instruções, precisa de mais linhas de código para executar uma função. 
>- Já a arquitetura de Von Neumann utiliza as instruções CISC, por ser mais complexa e possuir mais funções, necessitando de menos linha de código para executar uma mesma tarefa que em comparação com a Harvard.
>
>- Ambas as diferenças são provenientes das suas características unicas de barramentos.
> CISC e RISC ^[A08 - Conceitos de programa armazenado, Linguagem de máquina, arquitetura CISC e RISC, Instruções de máquina]
# Conceito de Pipeline em processadores
## Técnica de pipeline em processadores
- Método usado em microprocessadores para executar múltiplas instruções simultaneamente
- Funciona a partir da divisão de uma tarefa em partes menores, que podem ser processadas em paralelo
- A técnica divide o processamento de uma instrução em múltiplos estágios (passos), permitindo que várias instruções sejam executadas ao mesmo tempo
- Essa técnica melhora, consideravelmente, a eficiência e o desempenho do sistema
## Funcionamento
- O pipeline pode ser visto como um tipo de paralelismo na execução das instruções;
- Uma instrução é um comando dado a um computador para execução de  uma tarefa - como operações lógicas ^[], operações matemáticas(+, -, * , /) e de fluxo (condições, repetições e desvios);
- As tarefas que um processador executa, em síntese, são sequências de instruções
- Com a técnica, o processador pode trabalhar no estágio 1 de uma tarefa enquanto trabalha no estágio 2 de outra tarefa mais avançada e assim por diante
- OBS.: a quantidade de instruções executadas paralelamente depende do tamanho do pipeline e da eficiência da arquitetura.
	![[Pasted image 20241118121001.png]]
### Analogia da lavanderia
- Numa lavanderia há 4 etapas: lavar, secar, dobrar e guardar roupas
- Cada uma das quatro etapas demora uma unidade de tempo
#### Sem Pipeline
- De forma serial (sem pipeline - sem paralelismo), só poderia começar uma nova tarefa após o fim da tarefa anterior, ou seja, só poderia lavar um segundo lote de roupas se o primeiro já estivesse terminado a etapa de guardar roupas:
	![[Pasted image 20241118121416.png]]
#### Com pipeline
- Nesse novo exemplo, com a técnica de paralelismo, outra etapa pode ser executada assim que uma acaba, por exemplo. Enquanto o primeiro lote de roupas sai da lavagem para a secagem, o segundo lote entra no processo de lavagem
- Assim, a máquina de lavar e a secadora estariam em trabalhando ao mesmo tempo, reduzindo o tempo de execução da tarefa de lavar roupas:
	![[Pasted image 20241118121908.png]]
>[!tip] Em resumo
>- A técnica de pipeline reduz o tempo de execução de uma tarefa de muitos processos
>- Enquanto uma etapa avança, outra etapa entra no local do processo avançado para ser processada, assim, várias etapas em paralelo são executadas ao mesmo tempo.