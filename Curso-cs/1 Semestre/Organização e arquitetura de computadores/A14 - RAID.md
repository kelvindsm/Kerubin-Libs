---
tags:
  - OrgArc2306
---
>[!info] Contexto
> - Na era digital, o armazenamento de dados é uma necessidade, a proteção dos dados, em muitos casos, é uma preocupação fundamental
> - Logo, RAID se apresenta como uma solução confiável de armazenamento, enfrentando questões como eficiência e segurança das informações

## O que é o RAID
- Significa "Redundant Array of Independent Disks", "Conjunto Redundante de Discos Independentes" ou "Matriz Redundante de Discos Independentes"
- É uma solução de armazenamento que usa vários discos rígidos para criar um sistema mais seguro e confiável
- Combina vários discos, formando um único volume lógico, aumentando a capacidade de armazenamento e protegendo os dados em caso de falha de um dos discos
## Tipos de RAID
### RAID 0
- Nível mais básico de RAID
- Usa dois ou mais discos para criar um único volume lógico que aumenta a velocidade de leitura e gravação de dados
- Não há redundância, não oferece proteção de dados
- Se um dos discos falhar, todo o sistema falhará
- Numero mínimo de 2 HD's
>[!note] Vantagens e desvantagens
>- Vantagem: rapidez para acessar informações e capacidade de armazenamento elevada
>- Desvantagem: Sem espelhamento, sem paridade de dados e não fornece segurança para os dados
### RAID 1 
- Nível mais simples de RAID redundante
- Utiliza dois discos para criar um único volume lógico que espelha os dados em ambos os discos
- Se um disco falhar, o sistema de armazenamento continuará a funcionar normalmente com o disco restante
- Numero mínimo de 2 HD's
>[!note] Vantagens e desvantagens
>- Vantagem: segurança dos dados (em caso de defeito do HD) e caso falhe algum setor, é possível recuperar copiando os arquivos do outro HD;
>- Desvantagem: Escrita mais lenta e Redução na capacidade em relação ao RAID 0
### RAID 5 
- Utiliza três ou mais discos par criar um volume lógico que distribui os dados e a paridade em todos os discos
- Se um disco falhar, os dados podem ser recuperados a partir da paridade armazenada nos outros discos
- Numero mínimo de 3 HD's
>[!note] Vantagens e desvantagens
>- Vantagem: Mais rápido para identificar erros, leitura rápida e maior segurança
>- Desvantagem: Escrita mais lenta que RAID 0 e sistema de controle de discos mais complexo
### RAID 6
- Semelhante ao RAID 5, mas usa dois conjuntos de paridade - redundância adicional
- Pode suportar falhas simultâneas de dois discos
- Número mínimo de 4 HD's
>[!note] Vantagens e desvantagens
>- Vantagem: Possibilidade de falhar 2 HD's ao mesmo tempo sem perda de dados e maior segurança comparado ao RAID 5
>- Desvantagem: Escrita mais lenta que o RAID 0 e sistema de controle de discos mais complexo.
### RAID 10 ou 1+0
- Combina a velocidade do RAID 0 com a redundância do RAID 1
- Utiliza quatro ou mais discos para criar dois volumes lógicos, espelhados em pares
- Pode suportar falhas simultâneas em até metade dos discos
- Número mínimo de 4 HD's
>[!note] Vantagens e desvantagens
>- Vantagem: Maior segurança contra perda de dados, pode falhar um ou dois HD's ao mesmo tempo (sem ser do mesmo subgrupo);
>- Desvantagem: Grande numero de discos rígidos utilizados em relação aos demais tipos, Drivers devem ficar em sincronismo de velocidade para ampliar a performance.

## Qual RAID escolher
Depende do domínio de aplicação e do problema a ser enfrentado:
- Se a velocidade é prioridade: RAID 0;
- Se a redundância for prioridade: RAID 5 ou RAID 6;
- Se a velocidade e a redundância forem igualmente importantes: RAID 10
>[!tip]
>- Faz-se necessário considerar a necessidade, número de discos e o orçamento disponível para o sistema de armazenamento

