---
tags:
  - Outros
  - Calculo
  - Emprogresso
---
# Polinômios
>[!quote] Definição de monômios
>- São constituídos pelos produtos entre números conhecidos e incógnitas.
>- Exemplo: $2x$, $4xy^2$, $1x^3y^2$.

>[!quote] Definição de polinômios
>- Soma ou subtração de monômios.
>	- Exemplo: $4xy
>	- $4xy+2x+7yw$, $2xy^2+5x-3y$, $3^x4-x^2+60x+7x^0$

>[!quote] Definição de polinômios de uma incógnita
>- Um polinômio de uma incógnita $x$ é uma expressão que pode ser escrita na forma $${\color{RoyalBlue}{a_nx^n}}+a_{n-1}x^{n-1}+...+a_2x^2+a_1x+a_0$$
>	- OBS.: <mark style="color: white; background-color: RoyalBlue">Monômios são chamados de "termos".</mark>
>- Em que: $n\in\mathbb{N}$ e $a_n, a_{n-1},...,a_1,a_0$ são números reais, chamados de coeficientes. O grau desse polinômio é $n$.
>- Exemplos:
>	- $5x^{\color{OrangeRed}{3}}+2x^2-4x+0$ : polinômio de terceiro grau;
>	- $3x^{\color{Dandelion}{2}}+30x-11$ : polinômio de segundo grau;
>	- $2x^{\color{Emerald}{1}}+10$ : polinômio de primeiro grau.

## Adição e subtração de polinômios
- Quando se soma ou subtrai dois polinômios, podendo somar ou subtrair os termos semelhantes, ou seja, termos com a parte literal igual.
- Exemplo de adição:
$$
	\begin{gather*}
	\quad 
	\text{Equação inicial:}
	\\
	\textcolor{OrangeRed}{0x^4} + \textcolor{BurntOrange}{5x^3} + \textcolor{Yellow}{2x^2} + \textcolor{YellowGreen}{(-4x)} + \textcolor{OrangeRed}{2x^4} + \textcolor{BurntOrange}{3x^3} + \textcolor{Yellow}{(-2x^2)} + \textcolor{YellowGreen}{x}
	\\ \\
	\text{Organizando os termos semelhantes:}
	\\ = \textcolor{OrangeRed}{(0+2)x^4} + \textcolor{BurntOrange}{(5+3)x^3} + \textcolor{YellowOrange}{(2-2)x^2} + \textcolor{YellowGreen}{(-4+1)x}
	\\ \\
	\text{Simplificando os termos:}
	\\ = \textcolor{OrangeRed}{2x^4} + \textcolor{BurntOrange}{8x^3} + \textcolor{YellowOrange}{0x^2} + \textcolor{YellowGreen}{(-3x)}
	\\ \\
	\text{Resultado final:}
	\\ = \boxed{2x^4+8x^3-3x}
	\end{gather*}
$$
- Exemplo de subtração:
$$
\begin{gather*}
\text{Equação inicial}
\\ (2x^4y+2x^2y-3x) - (2x^3y+3x^2y-2x) 
\\ \\
\text{Distribuindo o sinal negativo no segundo polinômio:}
\\ = \textcolor{OrangeRed}{2x^4y} + \textcolor{Yellow}{2x^2y} \textcolor{YellowGreen}{-} \textcolor{YellowGreen}{3x} \textcolor{BurntOrange}{-2x^3y} \textcolor{Yellow}{-3x^2y} \textcolor{YellowGreen}{+} \textcolor{YellowGreen}{2x} 
\\ \\
\text{Organizando e agrupando os termos semelhantes:} \\
= \textcolor{OrangeRed}{(2)x^4y} + \textcolor{BurntOrange}{(-2)x^3y} + \textcolor{Yellow}{(2-3)x^2y} + \textcolor{YellowGreen}{(-3+2)x} 
\\ \\
\text{Simplificando os termos:}
\\
= \textcolor{OrangeRed}{2x^4y} \textcolor{BurntOrange}{-} \textcolor{BurntOrange}{2x^3y} + \textcolor{Yellow}{(-1)x^2y} + \textcolor{YellowGreen}{(-1)x} 
\\ \\
\text{Resultado final:}
\\ = \boxed{2x^4y - 2x^3y - x^2y - x}
\end{gather*}
$$
## Multiplicação de polinômios
- É utilizada a propriedade distributiva para resolver
- Exemplo:
$$
\begin{gather*}
	\text{Definição inicial da equação:} 
	\\(\textcolor{OrangeRed}{3x^2} \textcolor{OrangeRed}{-} \textcolor{OrangeRed}{4x}) \cdot (\textcolor{RoyalBlue}{x^2} \textcolor{RoyalBlue}{-} \textcolor{RoyalBlue}{3x} \textcolor{RoyalBlue}{+} \textcolor{RoyalBlue}{2}) 
	\\ \\
	\text{Usando a Propriedade Distributiva (Cada termo do 1º multiplica todos os termos do 2º):} 
	\\ \\
	\text{1. Distribuição de } \textcolor{OrangeRed}{3x^2} \text{:} 
	\\
	\textcolor{OrangeRed}{3x^2} \cdot (\textcolor{RoyalBlue}{x^2}) + \textcolor{OrangeRed}{3x^2} \cdot (\textcolor{RoyalBlue}{-3x}) + \textcolor{OrangeRed}{3x^2} \cdot (\textcolor{RoyalBlue}{2})
	\\
	\text{Resultado desta distribuição:} 
	\\
	\textcolor{MediumPurple}{3x^4} \textcolor{MediumPurple}{-} \textcolor{MediumPurple}{9x^3} \textcolor{MediumPurple}{+} \textcolor{MediumPurple}{6x^2} 
	\\ \\
	\text{2. Distribuição de } \textcolor{OrangeRed}{-4x} \text{:} 
	\\
	\textcolor{OrangeRed}{-4x} \cdot (\textcolor{RoyalBlue}{x^2}) + \textcolor{OrangeRed}{-4x} \cdot (\textcolor{RoyalBlue}{-3x}) + \textcolor{OrangeRed}{-4x} \cdot (\textcolor{RoyalBlue}{2})
	\\
	\text{Resultado desta distribuição:}
	\\
	\textcolor{MediumPurple}{-4x^3} \textcolor{MediumPurple}{+} \textcolor{MediumPurple}{12x^2} \textcolor{MediumPurple}{-} \textcolor{MediumPurple}{8x} 
	\\ \\
	\text{Combinando os resultados :}
	\\
	= \textcolor{MediumPurple}{3x^4} \textcolor{MediumPurple}{-} \textcolor{MediumPurple}{9x^3} \textcolor{MediumPurple}{+} \textcolor{MediumPurple}{6x^2} \textcolor{MediumPurple}{-} \textcolor{MediumPurple}{4x^3} \textcolor{MediumPurple}{+} \textcolor{MediumPurple}{12x^2} \textcolor{MediumPurple}{-} \textcolor{MediumPurple}{8x} 
	\\ \\
	\text{Agrupando e somando os termos semelhantes:} 
	\\
	= 3x^4 + (-9-4)x^3 + (6+12)x^2 - 8x 
	\\ \\
	\text{Resultado Final:} \\
	= \boxed{3x^4 - 13x^3 + 18x^2 - 8x}
\end{gather*}
$$
### Produtos notáveis
- Produtos úteis em fatoração de polinômios
1. $(u+v)*(u-v)=u^2-v^2$
2. $(u+v)^2 =u^2+2uv+v^2$
3. $(u-v)^2=u^2-2uv+v^2$
4. $(u+v)^3=u^3+3u^2v+3uv^2+v^2$
5. $(u-v)^3=u^3-3u^2v+3uv^2-v^3$
## Divisão de polinômios
### Método das chaves (completar depois)
- Baseado na fórmula de divisão, que define que: $$P(x)=D(x)*Q(x)+R(x)$$
- Onde:
	- $P(x)$: é o dividendo;
	- $D(x)$: é o divisor;
	- $Q(x)$: é o quociente;
	- $R(x)$: é o resto da divisão.
### Dispositivo de Briot-Ruffini (Completar depois)
- Usado para dividir um polinômio por $(x-a)$...
## Fatoração de polinômios
- Forma de simplificar polinômios, transformando-os em produto de polinômio de grau menor.
- Exemplo:
$$
x^4+5x^3-4x^2-20x=x(x+5)*(x+2)*(x-2)
$$
### Métodos de fatoração de polinômios
#### 1. Fator comum em evidência
- Colocando o fatores em comum em evidência
$$
x^4+5x^3-4x^2-20x=x(x^3=5x^2-4x-20)
$$
#### 2. Diferença de dois quadrados
$$
\begin{gather}
(u+v)*(u-v)=u^2-v^2
\\ \\
\text{Exemplo 1: }(x+2)*(x-2)=x^2-4
\\ \\
\text{Exemplo 2: } (2x^2+5x)*(2x^2-5x)=4x^2-25x^2
\end{gather}
$$
#### 3. Trinômio quadrado perfeito
$$
\begin{gather*}
(u+v)^2 = u^2+uv+v^2
\\
\text{Exemplo 1: } (x+3)^2 = (x+3)*(x+3) = \boxed{x^2+6x+9}
\\ \\
(u-v)^2=u^2-2uv+v^2
\\ 
\text{Exemplo 2: (desenvolver depois...)}  
\end{gather*}
$$
#### 4. Trinômio cubo perfeito
$$
\begin{gather*}
(u-v)^3=u^3-3u^2v+3uv^2-v^3
\\
(u-v)*(u^2+uv+v^2)=u^3-v^3
\end{gather*}
$$
#### 5. Teorema de D'alembert
- Seja $P(x)$ um polinômio e $a\in\mathbb{R}$. Se temos que $P(a)=0$, (mesmo que: "a é raiz de $P(x)$") então $P(x)$ é divisível por $(x-a)$.
- Exemplo: "Fatore o polinômio $x^3+5.(-5)^2-4(-5)-20$"