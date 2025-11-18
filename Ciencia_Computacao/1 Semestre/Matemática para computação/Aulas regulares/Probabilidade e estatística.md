---
tags:
  - MC2310
---

# Conjuntos e espaço amostral
## Espaço amostral
>[!note] Conceito
>- É o conjunto de todos os possíveis resultados de um determinada variável aleatória
>- Os elementos e subconjuntos do espaço amostral representam os possíveis eventos associados à variável aleatória
>- Os eventos podem ser combinados de acordo com as operações de conjuntos para formar novos eventos

## Variável aleatória
- Etimologicamente, Variável aleatória é uma:
	- Variável: Possui um valor desconhecido;
	- Aleatória: Pode possuir valores diferentes, com diferentes probabilidades
## Operações com conjuntos
### Complementar de um conjunto 
- O complementar (ou complementar absoluto) funciona como o operador negação
	- Dado um conjunto A ∈ Ω, seu complementar (A c ) constitui nos elementos presentes no espaço amostral, mas não em A
		- $A^c = {x ∈ Ω ∣ x ∉ A}$
- **Veja $A^c$ como NÃO A**
### Interseção de dois conjuntos
- A interseção (ou conjunção) entre os conjuntos A e B (A ∩ B) constitui nos elementos pertencentes tanto a A quanto a B
	 - $A ∩ B = {x ∈ Ω ∣ x ∈ A; x ∈ B}$
- **Veja A ∩ B como A “E” B**
### Eventos mutualmente excludentes
- Dois eventos A e B são ditos mutuamente excludentes quando A ∩ B = ∅
	- Se quando um acontece, o outro não acontece, é natural que A e B não possam acontecer ao mesmo tempo
### União de dois conjuntos
- A união (ou disjunção) entre os conjuntos A e B (A ∪ B) constitui nos elementos pertencentes a A, a B, ou a ambos
	- $A ∪ B = {x ∈ Ω ∣ x ∉ (A^c ∩ B^c )}$
- **Veja A ∪ B como A “OU” B**
### União exclusiva de dois conjuntos
- A união exclusiva (ou disjunção exclusiva) entre os conjuntos A e B (A ∪ B) constitui nos elementos pertencentes a A ou a B, mas não a ambos
	- $A ∪ B = (A ∩ B^c ) ∪ (A^c ∩ B)$
- **Veja A ∪ B como “OU” A, “OU” B**
### Diferença de dois conjuntos
- A diferença (ou complementar relativo) entre os conjuntos A e B (A \ B) constitui nos elementos pertencentes a A, mas não a B
	- $A \setminus B = {x ∈ Ω ∣ x ∈ A; x ∉ B}$
	- Note que $A^c = Ω \setminus A$
	- $A \setminus B ≠ B \setminus A$
# Probabilidade: axiomas e operações
## Definição “clássica” de probabilidade
- $$ P(X) = \frac{\mbox{Nº de casos favoráveis}} {\mbox{Nº de casos possíveis}} $$
## Probabilidade
- É o resultado numérico de uma função que associa cada elemento do espaço amostral de uma variável aleatória X a um número real entre 0 e 1
- $$ $P ∶ Ω⟶[0, 1] $$ $$P(ω) = P(X = ω), ω ∈ Ω $$
- Para cada resultado possível de uma variável aleatória, a função de probabilidade diz o quão provável é a ocorrência daquele evento
## Axiomas de Kolmogorov
- A probabilidade de ocorrência de eventos A1, A2, ... ∈ Ω segue três propriedades básicas:
- $0 ≤ P(A) ≤ 1$
- $P(Ω) = 1$
- Se A1, A2, ... forem dois a dois disjuntos: ![[Pasted image 20241202191126.png]]
## Probabilidade: propriedades
- Sejam os eventos A e B subconjuntos de Ω, é válido que:
- P(∅) = 0
- $P(A^c) = 1 − P(A)$
- Se A ⊆ B, então P(A) ≤ P(B)
- P(A ∪ B) = P(A) + P(B) − P(A ∩ B)
## Distribuição de probabilidade
- A atribuição da probabilidade de ocorrência a cada elemento do espaço amostral define uma distribuição de probabilidade
- A distribuição de probabilidade fornece P(X = ω), para todo ω ∈ Ω
## Função de probabilidade
- Caso a distribuição de probabilidade de uma variável aleatória X seja conhecida, é fácil construir sua função de probabilidade $$f (ω) = P(X = ω), ∀ ω ∈ Ω$$
- $f (ω) ≥ 0, ∀ ω ∈ Ω$
- $\sum_{Ω} f(ω)=1$
## Função de distribuição acumulada
- A função de distribuição acumulada fornece a probabilidade acumulada de X até um ponto específico $$F(ω) = P(X ≤ ω), ∀ ω ∈ Ω$$
- $P(k1 < ω ≤ k2) = F(k2) − F(k1)$
## Probabilidade condicional
- Probabilidade é um conceito que modela a incerteza
	- A incerteza é consequência da falta de informações
- Assim, à medida que mais informações estão disponíveis, a probabilidade de ocorrência de um evento pode mudar
### intuição da probabilidade condicional
>[!info] Forneça uma estimativa da probabilidade de uma pessoa escolhida ao acaso ter uma altura superior a 2 metros, dadas as seguintes informações:
>> - A pessoa escolhida é um homem
>> - A pessoa escolhida tem altura maior que 1.70 metro
>> - A pessoa escolhida é um jogador de basquete
>> - A pessoa escolhida joga como pivô
>> - A pessoa escolhida é a mais alta do seu time
> 
>**Acréscimos informacionais implicam em diminuição do espaço amostral associado!**

- Caso seja sabido que um evento A ocorreu, o espaço amostral original (em que A era uma incerteza) reduzir-se-à aos casos em que A passa a ser uma certeza
- A probabilidade de ocorrência de B, dado que aconteceu A (P(B∣A)), equivale a calcular P(B) em relação ao espaço amostral reduzido onde A é uma certeza
>[!WARNING] Atenção
>- P(B∣A) **NÃO** precisa ser maior que P(B)
>>- O espaço amostral está associado à diminuição da incerteza; dada a ocorrência de A, a probabilidade de B ocorrer pode aumentar ou diminuir 

$$P(B∣A) = \frac{P(A ∩ B)} {P(A)}$$
>[!note] Propriedades:
>- $0 ≤ P(B∣A) ≤ 1$
>- $P(Ω∣A) = 1$
>- $P(A∣A) = 1$
>- $P(\varnothing ∣A) = 0$
>- $P(A∣ \varnothing) = P(A)$
>- Se $B1 ∩ B2 = \varnothing, P(B1 ∪ B2∣A) = P(B1∣A) + P(B2∣A)$
## Eventos independentes
- Dois eventos A e B são ditos independentes quando a probabilidade de ocorrência de um não influencia na probabilidade de ocorrência do outro.
	- A e B são independentes ↔ $P(A∣B) = P(A)$ ↔ $P(A ∩ B) = P(A) ⋅ P(B)$
	- **Eventos independentes e eventos mutuamente excludentes são duas coisas diferentes!**
- Se A é independente de B, qualquer informação a respeito de B (incluindo o fato de B não ter acontecido) não deve alterar a probabilidade de A.
	- Se A e B são eventos independentes, A e $B^c$ , $A^c$ e B, e $A^c$ e $B^c$ também o são.
## Partição do espaço amostral
>[!quote] Partição
> - n eventos E1, E2, ..., En formam uma partição do espaço amostral Ω quando:
> >- $P(Ei) > 0, ∀ i ∈ {1, 2, ..., n}$
> >- ![[Pasted image 20241202193315.png]]
> >- $P(Ei ∩ Ej) = \varnothing, ∀ i ≠ j, i, j ∈ {1, 2, ..., n}$

## Regra da probabilidade total
>[!note] Dado um espaço amostral Ω particionado em E1, E2, ..., En e um evento A ∈ Ω, a probabilidade de ocorrência de A pode ser expressa por:
> - ![[Pasted image 20241202193532.png]]

>[!tip] Quando se usa?
>- Essa regra nos permite calcular a probabilidade de um evento, condicionando em todas as instâncias possíveis de um "evento diferente", ou, formalmente falando, em todos os conjuntos de uma partição do espaço amostral;
>-  **Ela expressa a probabilidade total de um resultado que pode ser realizado através de vários eventos distintos.**
## Condicionamento reverso
- Com a regra da probabilidade total, podemos enunciar $P(E_j∣ A)$ em termos de $P(A∣E_j)$ e $P(E_j)$
- Lembre-se que $$P(Ej∣A) = \frac{P(Ej ∩ A)} {P(A)}$$
## Teorema de Bayes
- Dado um espaço amostral Ω particionado em $E_1, E_2, ..., E_n$ e um evento A ∈ Ω, a probabilidade condicional de $E_j$ dado A, para todo $j ∈ {1, 2, ..., n}$, é dada por:
- 
- ![[Pasted image 20241202193859.png]]
>[!tip] Quando se usa?
>- Se usa quando pretendemos saber a probabilidade de um evento acontecer tendo como base um evento inicial

---

