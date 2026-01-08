---
tags:
  - Naoconcluido
---
## Tipos referência e tipos valor
### Tipos referência
- Classes são tipo referência: variáveis cujo tipo são classes não devem ser entendidas como caixas, mas sim como setas (ponteiros) para as caixas;
	- Quando se declara uma variável, ela é armazenada no Stack da memória, porém, quando se atribui valores a ela, esses dados serão armazenados no Heap da memória, enquanto na Stack será armazenado somente um endereço de referência apontando (ponteiro) para os dados da variável na HEAP.
	- Quando uma variável recebe outra, exemplo `p2 = p1`, a variável `p2`passa a apontar para o mesmo objeto onde `p1` aponta.
	- Valor "null": tipos referência aceitam o valor "null", que indica que a variável aponta para ninguém.
### Tipos valor
- Em Java, tipos primitivos são tipos valor. Tipos valor são como caixas e não ponteiros.
	- Quando se declara duas variáveis tipo valor e quando se atribui `y = x`, o valor y recebe uma cópia do valor de x, e não aponta como nos tipo referência
## Tipos primitivos e inicialização
- Demo: 
```Java erro:2 destaque:5
int p;
System.out.println(p); // erro: variável não iniciada

p = 10;
System.out.println(p);
```

## Valores padrão
- Quando alocamos (new) qualquer tipo estruturado (classe ou array), são atribuídos valores padrão aos seus elementos:
	- Números: 0;
	- boolean: false;
	- char: caractere código 0;
	- objeto: null.

![[../0 - Imagens/tipoReferenciaTipoValor.png|500]]

---
# Comportamento de memória
## Garbage Collector
- Processo que automatiza o gerenciamento de memória de um programa em execução;
- O garbage collector monitora os objetos alocados dinamicamente pelo programa (no heap), <mark style="background: #FF5582A6;">desalocando aqueles que não estão mais sendo utilizados.</mark>
	- - Um objeto sem referência será desalocado pelo garbage collector, responsável por monitorar processos do HEAP.
### Desalocação por escopo
- Variáveis locais são desalocadas imediatamente assim que seu escopo local sai de execução;
- (Explicar melhor)
---
# Vetores