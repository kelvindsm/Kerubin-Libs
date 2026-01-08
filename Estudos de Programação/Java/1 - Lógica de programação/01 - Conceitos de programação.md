# Algoritmo, Automação, Programas de Computador

<mark style="background: #FFF3A3A6;">Algoritmo: sequencia finita de instruções para se resolver um problema</mark>

Exemplo: Problema -  lavar roupa suja 
Algoritmo: 
1) Colocar a roupa em um recipiente 
2) Colocar um pouco de sabão e amaciante 
3) Encher de água 
4) Mexer tudo até dissolver todo o sabão 
5) Deixar de molho por vinte minutos 
6) Esfregar a roupa 
7) Enxaguar 
8) Torcer

<mark style="background: #BBFABBA6;">Automação: Consiste em utilizar máquinas para executar o procedimento desejado de forma automática ou semiautomática.</mark>
- Importante pois facilita o trabalho e economiza o tempo.

>[!info] O computador
> - Hardware: parte física (a máquina em si)
> - Software: parte lógicas (os programas)

### Programa e algoritmo
<mark style="background: #ADCCFFA6;">Programas de computador são algoritmos executados pelo computador</mark> (em linhas gerais).

<mark style="background: #ADCCFFA6;">Conclusão: o computador é uma máquina que automatiza a execução de algoritmos como processamento de dados e cálculos, por exemplo.</mark>

---
# O que é preciso para se fazer um programa de computador
- <mark style="background: #BBFABBA6;">Uma linguagem de programação: regras léxicas e sintáticas para se escrever o programa;</mark>
- <mark style="background: #ABF7F7A6;">Uma IDE: software para editar e testar o programa;</mark>
- <mark style="background: #ADCCFFA6;">Um compilador: software para transformar o código fonte em código objeto;</mark>
- <mark style="background: #D2B3FFA6;">Um gerador de código ou máquina virtual: software que permite que o programa seja executado.</mark>
---
# Linguagem de programação, Léxica, sintática
- <mark style="background: #FFF3A3A6;">Léxica: diz respeito à correção das palavras "isoladas"</mark>
- <mark style="background: #ADCCFFA6;">Sintáticas: diz respeito à correção das sentenças</mark>
- <mark style="background: #BBFABBA6;">Linguagem de programação: é um conjunto de regras léxicas (ortografia) e sintáticas (gramática) para se escrever programas</mark>

- Exemplos de linguagens de programação: Java, Python, C, C++...
---
# IDE - Ambiente Integrado de Desenvolvimento
- **Programa usado para desenvolver, testar e executar o algoritmo em desenvolvimento**, existem vários. Para java, o recomendado é: Eclipse, Netbeans e Idea.
---
# Compilação, interpretação, código fonte, código objeto, máquina virtual 

- <mark style="background: #FFB8EBA6;">Código fonte: aquele escrito pelo programador em linguagem de programação.</mark> Entendido pelo humano mas não pela máquina
- <mark style="background: #FF5582A6;">Compilação: transforma o código fonte em código executável.</mark> Faz analise léxica e sintática para tornar em código objeto, que passará por um gerador de código (para realizar a construção) e criar o código executável
	![[../0 - Imagens/compilacao.png|400]]
- <mark style="background: #FFF3A3A6;">Interpretação: um interpretador lê o código e faz a análise léxica, sintática e a geração de código sob demanda</mark>, ou seja, gradualmente conforme a leitura
	![[../0 - Imagens/interpretacao.png|center|400]]
- <mark style="background: #FFB86CA6;">Hibrida: o código passa por uma pré-compilação</mark> (análise lexica e sintática) <mark style="background: #FFB86CA6;">sendo transformado em um bytecode que será interpretado por uma máquina virtual para fazer a execução do programa</mark>
	![[../0 - Imagens/abordagemHibrida.png|450]]

>[!tip] Compilação e interpretação
> - Compiladas (C, C++): transforma o código fonte em um código compilado
> ![[../0 - Imagens/codCOmpilado.png|450]]
> - Interpretadas (PHP, JavaScript): Pega o codigo fonte para transformar ele gradualmente em código interpretado - "lê linha por linha" 
> ![[../0 - Imagens/codInterpretado.png|450]]
> - pré-compiladas + máquinas virtuais (Java, C#): código compilado e executado numa máquina virtual
>![[../0 - Imagens/codCompiladoVm.png|450]]

---