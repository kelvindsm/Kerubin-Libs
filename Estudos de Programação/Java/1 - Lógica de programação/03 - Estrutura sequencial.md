# Expressões aritméticas
- **Garante que uma expressão matemática retorne um valor numérico como resposta** - Ex: $4+5 = 9$
- <mark style="background: #FF5582A6;">Usa operadores aritméticos para entender o que fazer nas expressões</mark>, se deve somar ou subtrair, por exemplo. 

| ![[../0 - Imagens/operadoresAritmeticos.png\|350]] | OBS: o operador "mod" retorna o resto de uma divisão como valor da operação |
| ----------------------------------- | --------------------------------------------------------------------------- |
## Exemplos de expressões aritméticas:

| ![[../0 - Imagens/exExprAritmeticas.png\|300]] | ![[../0 - Imagens/exComMod.png\|300]] |
| ------------------------------- | ---------------------- |
## Variáveis e tipos básicos em Java
>[!quote] Visão geral
>- Um programa de computador **armazena os dados em forma de variáveis**;
>- As <mark style="background: #FF5582A6;">variáveis são porções de memória RAM usadas para armazenar os dados durante a execução dos programas</mark>;
> ![[../0 - Imagens/variavelEmMemoria.png|300]]
### Declaração de variáveis

- Sintaxe: <mark style="background: #FFB86CA6;">tipo_de_variavel</mark> <mark style="background: #ADCCFFA6;">nome_da_variavel</mark> = <mark style="background: #BBFABBA6;">valor_inicial</mark>;
```Java title:"Exemplos"
int idade = 25;
double altura = 1.68; 
char sexo = 'F';
```

>[!info] : Uma variável possui
>- <mark style="background: #ADCCFFA6;">Nome (ou indicador): definido da melhor forma pelo usuário para indicar a variável mais facilmente;</mark>
>- <mark style="background: #FFB86CA6;">Tipo: indica o formato do dado que a variável possa ser, um texto ou numero, por exemplo;</mark>
>- <mark style="background: #BBFABBA6;">Valor inicial: o valor atribuído para ser armazenado nessa variável, pode ser um "abacate" ou o numero 5, por exemplo;</mark>
### Tipos básicos em Java
![[../0 - Imagens/tiposBasicosEmJava.png|550]]
### Nomes de variáveis
-  Não pode começar com digito: se usa uma letra ou _ ;
- Não pode ter espaços em branco;
- Não usar acentos ou til;
- Sugestão de uso: "camel case"
![[../0 - Imagens/nomesDeVariaveis.png]]

---
# As três operações básicas de programação
>[!quote] As operações são definidas por:
>- <mark style="background: #FF5582A6;">Entrada de dados: é quando o usuário insere informações na máquina</mark> (geralmente por meio da digitação), esse processo também é chamado de <mark style="background: #FF5582A6;">leitura - "O programa está lendo dados".</mark>
>- <mark style="background: #FFB86CA6;">Processamento de dados: Quando o programa realiza os cálculos</mark>, **o processamento de dados se dá por um comando chamado atribuição**, por exemplo:  `{Java icon title:a }media = (x + y) / 2.0;`
>- <mark style="background: #FFF3A3A6;">Saída de dados: Quando a máquina retorna o valor do processamento para o usuário</mark>, o processo <mark style="background: #FFF3A3A6;">também é chamado de escrita - "O programa está escrevendo dados".</mark>

## Entrada de dados em Java
- <mark style="background: #FF5582A6;">Scanner: objeto usado para entrada de dados em Java</mark>
```Java title:"Definindo uma entrada de dados"
import java.util.Scanner;
Scanner sc = new Scanner(System.in);
sc.close(); // usado para encerrar a utlização do Scanner
```
### Exemplos para diferentes casos
```Java title:"Para ler uma palavra (texto sem espaços)"
String x;
x = sc.next();
```

```Java title:"Para ler um número inteiro"
int x;
x = sc.nextInt();
```

```Java title:"Para ler um número com ponto flutuante" wrap
double x;
x = sc.nextDouble();

// use Locale.setDefault(Locale.US); antes da declaração do Scanner para separar os decimais com ponto
```

```Java title:"Para ler um caractere"
char x;
x = sc.next().charAt(0);
```

```Java title:"Para ler vários dados na mesma linha"
string x; 
int y; 
double z; 

x = sc.next(); 
y = sc.nextInt(); 
z = sc.nextDouble();
```

```Java title:"Para ler um texto ATÉ A QUEBRA DE LINHA"
import java.util.Scanner;
public class Main { 
	public static void main(String[] args) { 
		Scanner sc = new Scanner(System.in); 
		String s1, s2, s3; 
		s1 = sc.nextLine(); 
		s2 = sc.nextLine(); 
		s3 = sc.nextLine(); 
		
		System.out.println("DADOS DIGITADOS:"); 
		System.out.println(s1); 
		System.out.println(s2); 
		System.out.println(s3); sc.close(); 
	} 
}
```

![[../0 - Imagens/quebraDeLinhaPendente.png|450]]

---
## Processamento de dados em Java
- <mark style="background: #FFB86CA6;">Comando de atribuição - sintaxe: variável = expressão;</mark>
>[!note] Regra:
>1. A expressão é calculada
>2. O resultado da expressão é armazenado na variável
>OBS.: Lê-se "=" como "recebe"

```Java title:"Exemplo 1" destaque:4
int x, y; 

x = 5; 
y = 2 * x; // onde ocorre o calculo

System.out.println(x); 
System.out.println(y);
```

```Java title:"exemplo 2 - calculo da área de um trapézio" destaque:6
double b, B, h, area;

b = 6f; 
B = 8f; 
h = 5f; 
area = (b + B) / 2.0 * h; 

System.out.println(area);
```

>[!hint] Boa prática
>Sempre indique o tipo do número, se a expressão for de ponto flutuante (não inteira):
>- Para double, use " .0";
>- Para float, use "f".
### Casting
- Conversão explícita de um tipo para outro - <mark style="background: #FFB86CA6;">necessário quando o compilador não é capaz de “adivinhar” que o resultado de uma expressão deve ser de outro tipo.</mark>
```Java title:"Conversão de valores int para double" destaque:5
int a, b; 
double resultado; 
a = 5; 
b = 2; 
resultado = (double) a / b; 

System.out.println(resultado);
```
---
## Saída de dados em Java

```Java title:"Para escrever na tela um texto qualquer"
System.out.print("Bom dia!"); // sem quebra de linha
System.out.println("Bom dia!"); // com quebra de linha no final
```
 
```java title:"Para escrever o conteúdo de uma variável de algum tipo básico"
int y = 32;
System.out.println(y); // escreve 32 no console
```

```Java title:"Para escrever o conteúdo de uma variável com ponto flutuante"
double x = 10.35784;

Locale.setDefault(Locale.US); // para separar as casas decimais com ponto

System.out.printf("%.2f%n", x); // "printf" é usado para dados tipo double
System.out.printf("%.4f%n", x); // %n: quebra de linha
// "%.4f" define a quantidade de casas decimais que aparecerá no numero
```

```Java title:"Para concatenar vários elementos em um mesmo comando de escrita"
String nome = "Maria"; 
int idade = 31; 
double renda = 4000.0; 

System.out.printf("%s tem %d anos e ganha R$ %.2f reais%n", nome, idade, renda);
```

>[!tip] Formas de citar valores em concatenações 
>- %f  :  para pontos flutuantes - float e double; 
>- %d  :  para valores inteiros - byte, short, int e long; 
>- %s = texto - string; 
>- %n = quebra de linha no final.

---