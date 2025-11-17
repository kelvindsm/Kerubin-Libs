---
tags:
  - Naoconcluido
  - OrgArc2306
---
> [!quote] CPU
> - Dispositivo que controla a manipulação de dados em um computador
> - Em máquinas da metade do século XX, as CPUs eram grandes unidades compostas de diversos racks de circuitos eletrônicos
> - Com o tempo, foram reduzindo o tamanho e aumentando a capacidade de processamento
> - Atualmente são dispositivos eletrônicos inseridos na placa-mãe de computadores pessoais
> - Em smartphones e outros dispositivos menores, podem ser menores que um selo postal
> - Devido ao tamanho reduzido, são chamados de "microprocessadores

# Principais características
Possui três partes básicas:
1. Unidade lógica aritmética (ULA): contém circuitos que realizam operações sobre dados (como adição e subtração)
2. Unidade de controle (UC): contém os circuitos para a coordenação das atividades da máquina
3. Unidade de registro (UR ou registradores): contém células de armazenamento de dados, usada para armazenar informações temporárias dentro da CPU
# Registradores
Classificados como:
1. de propósito geral
2. de propósito específico
## Registradores de propósito geral
- servem como locais temporários de armazenamento para dados que são manipulados pela CPU, podem ser utilizados pelos programas para qualquer objetivo. Exemplo: mantêm as entradas para os circuitos da ULA e armazenam os resultados produzidos por essa unidade;
- Para uma operação com dados armazenados na memória principal, a UC transfere os dados da memória principal para os registradores de propósito geral, informa a ULA sobre quais registradores mantêm os dados, ativa os circuitos apropriados dentro da ULA e diz à ULA qual registrador deve receber o resultado.
## Registradores de propósito específico
- Usados apenas em algumas tarefas específicas, alguns exemplos são: Program Counter (PC) - Contador de programas, usado para determinar a próxima instrução a ser realizaada; Memory Adderess (MAR) - Registrador de endereço, usado para operações de transporte de dados, trabalha