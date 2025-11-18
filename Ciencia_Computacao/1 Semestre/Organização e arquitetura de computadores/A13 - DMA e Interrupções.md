---
tags:
  - OrgArc2306
---
# DMA: Direct Memory Access
- Tecnologia criada para agilizar o processamento e garantir que a CPU continue a trabalhar mesmo quando periféricos precisam ler/escrever dados na memória RAM
>[!quote] Síntese
>- É um método que permite que um dispositivo de entrada e saída envie ou receba dados diretamente da memória principal, desonerando a CPU e acelerando as operações que envolvem o uso da memória

- É o método pelo qual periféricos como placas de som, placas de rede e discos de armazenamento acessam e transferem diretamente os dados que precisam enviar ou receber, sem onerar a CPU no processo;
- Permite que o processador mantenha foco na tarefa que está realizando, enquanto a transferência de dados atua de maneira independente
## DMAC
- Para funcionar, o DMA usa um controlador dedicado DMAC (DMA controller), que atua como coprocessador para realizar as transferências, ter acesso ao barramento de dados do sistema e receber instruções da CPU, assim como avisar ao processador quando as transferências forem concluídas, para que seja possível verificar se houve ou não sucesso;
### Tipos de DMAC
- Um único na placa-mãe (Third-Party DMA - DMA de terceiros): é o método de acesso direto dememória que usa um controlador único do sistema, presente na placa-mãe
- Um controlador por periférico (First-Party DMA - DMA primário): também conhecido por Bus Mastering, utiliza um controlador por periférico. Logo, placas de vídeo, de som e sistemas de armazenamento possuem seus próprios DMAC
### Funcionamento do DMAC
1. Recebe a solicitação de um periférico (como uma placa de vídeo) para ter acesso direto à memória RAM
2. Solicita à CPU o acesso ao barramento para que o procedimento tenha início
3. E após a conclusão, o DMAC avisa a CPU, que verifica se o processo foi de fato concluído, e se houve êxito
## Vantagem
- Antes do uso dessa técnica, a CPU era responsável pela transferência de dados, impedindo-a o processamento de outras tarefas
- O método de DMA dá aumento de desempenho, permitindo acelerar o envio e recebimento de informações - que passaram então a ser enviadas em paralelo com outras tarefas da CPU
- De forma prática, isso significou maior desempenho para os sistemas computacionais
>[!attention] Atenção
>- *A CPU fica incapacitada de acessar a RAM durante o procedimento de DMA, essa limitação é contornada pelo uso da memória cache do chip*, que armazena as instruções e dados mais importantes em uso;
> 
>- *A coerência do Cache exige cuidados para que as informações no cache da CPU não se tornem desatualizadas conforme o DMA modifica os dados na memória RAM.* Do contrário, podem acontecer erros por incompatibilidade.

# Interrupção

- Em ciência da Computação, é um sinal de um dispositivo que tipicamente resulta em uma troca de contextos
- O processador para de fazer o que estava fazendo para atender o dispositivo que solicitou a interrupção
- Esses eventos são sinalizados para o processador através de pedidos de interrupção (IRQs)

>[!note] IRQ
>Um pedido de interrupção (interrupt request) trata-se de um sinal de hardware enviado ao processador que temporariamente pausa um programa em execução e permite que um programa especial, um manipulador de interrupções, seja executado.

- Interrupções de hardware são usadas para tratar eventos como recebimento de dados de um modem ou placa de rede, pressionamento de tecla ou movimento de mouse, por exemplo

>[!tip] Em resumo
>- Conceito: solicita à CPU para interromper a tarefa em andamento para tratar de um evento específico
>- Utilidade: tratar tempestivamente a um evento
>- Vantagem: o processador não precisa ficar monitorando constantemente os dispositivos. A interrupção alerta sobre o momento de tratar um evento.

