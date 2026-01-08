# Restrições e convenções para nomes
>[!hint] Dicas
> - Não pode começar com digito numérico: use uma letra ou underscore ( _ );
> - Não usar acentos ou til;
> - Não pode ter espaços em branco
> - Sugestão: use nomes que tenham significados.

```Java title:"Forma errada e correta"
// Forma errada
int 5minutes; 
int salário; 
int salario do funcionario;

// forma correta
int _5minutes; 
int salario; 
int salarioDoFuncionario;
```

---
# Convenções
- <mark style="background: #FF5582A6;">Camel Case ("lastName"):</mark> Normalmente usados em - <mark style="background: #FF5582A6;">Pacotes, atributos, métodos, variáveis e parâmetros;</mark>
- <mark style="background: #FFB86CA6;">Pascal Case ("ProductService"):</mark> normalmente <mark style="background: #FFB86CA6;">usado em classes.</mark>

```Java title:"Codigo Exemplo"
package entities; 

public class Account { 
	private String holder;
	private Double balance; 
	
	public Account(String holder, Double balance) { 
		this.holder = holder; 
		this.balance = balance; 
		} 
		
	public String getHolder() {
		return holder; 
	} 
	public void deposit(double amount) { 
		balance += amount; 
	} 
	public void withdraw(double amount) { 
		balance -= amount; 
	} 
}
```

--- 
# Operadores bitwise
>[!quote] Breve síntese
>- <mark style="background: #FFB8EBA6;">Técnica que permite alterar a sequência de bits de uma instância;</mark>
>- Podem ser **usadas para otimizar códigos e implementar estruturas de dados.**
## Operadores
![[../0 - Imagens/operadorBitwise.png]]
## Demonstração
![[../0 - Imagens/demonstracaoBitwise.png]]
### Operadores
- <mark style="background: #FFB8EBA6;">&: compara os bits de acordo com a regra logica "E"</mark>, sendo que **a comparação só resulta em 1 se ambas as entradas forem 1**. Logo, se realizando a comparação, o resultado entre (89 & 60) é "00011000" ou 24;

| ![[../0 - Imagens/comparacaoBitwise1.png\|400]] | A comparação dos valores em destaque resultam em um 0. Dessa forma que o bitwise é realizado. |
| -------------------------------- | --------------------------------------------------------------------------------------------- |

- <mark style="background: #FFB8EBA6;">| : compara os bits de acordo com a regra com a regra lógica "OU"</mark>, **sendo que a comparação resulta em 1 sempre quando houver o bit 1 na comparação**. Realizando a comparação entre (89 | 60) resultará em "01111101" ou 125;

- <mark style="background: #FFB8EBA6;">^:  compara os bits de acordo com a regra com a regra lógica "XOR" / ou exclusivo</mark>, **os resultados só serão 1 se os valores comparativos forem diferentes**. Por fim, realizando a comparação entre (89 ^ 60), o resultado será "01100101" ou 101.
- Aplicação: comparação de paridade entre pacotes.

```Java title:"Bitwise em código"
package course;

import java.util.Scanner;

public class Program {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int mask = 0b100000; // mascara usada para comparar com o valor de entrada;
		int n = sc.nextInt(); // valor de entrada que será atribuido pelo usuario
		
		// o programa compara os valores por bitwise e verifica se o sexto bit do valor selecionado pelo usuário é igual o da máscara ou não
		if ((n & mask) != 0) {
			System.out.println("6th bit is true!");
		} else {
			System.out.println("6th bit is false");
		}
		sc.close(); 	
	}
}
```

---
# Funções para String

- Formatar: 
	- ``toLowerCase()`` : altera as letras para minusculo;
	- ``toUpperCase()`` : altera as letras para maiúsculo;
	- ``trim()``: corta o texto, geralmente usado para cortar espaços, mas pode cortar outros caracteres
- Recortar: 
	- ``substring(inicio)`` : Retorna de uma String apenas os caracteres a partir de uma posição definida. Se houver 10 caracteres em uma String e o inicio for definido como 5, os cinco ultimo caracteres serão retornados;
	- ``substring(inicio, fim)`` : o mesmo que o de início, porém, pode ser definido um limite para retornar.
- Substituir: 
	- ``Replace(char, char)`` : substitui determinado caractere de um texto por outro
	- ``Replace(string, string)`` : troca determinada palavra por outra em um texto
- Buscar: 
	- ``IndexOf`` : retorna a posição da primeira ocorrência de um caractere ou substring dentro de uma determinada string. 
	- ``LastIndexOf`` : retorna a posição da última ocorrência de um caractere especificado ou uma substring em uma string. 
	- ``str.Split(" ")`` : corta a string em substrings de acordo com o delimitador definido, pode ser usado para separar palavras de uma frase.

---
# Comentários em Java (básico)

```Java title:"Tipos de comentários" destaque:18
package course;

import java.util.Locale; 
import java.util.Scanner; 

/* Este programa calcula as raízes de uma equação do segundo grau Os valores dos coeficientes devem ser digitados um por linha */ 

public class Program { 
	public static void main(String[] args) {
		Locale.setDefault(Locale.US);
		Scanner sc = new Scanner(System.in);
		
		double a, b, c, delta; 
		System.out.println("Digite os valores dos coeficientes:"); 
		a = sc.nextDouble();
		b = sc.nextDouble();
		c = sc.nextDouble(); 
		
		delta = b * b - 4 * a * c; // cálculo do valor de delta
	}
}
```

---
# Funções (sintaxe)

>[!quote] Funções
>- Representam um processamento que possui um significado;
>- Exemplo de funções:
>	- Math.sqrt(double); 
>	- System.out.println(string);
>- Principais vantagens: 
>	- modularização, delegação e reaproveitamento;
>- Dados de entrada e saída:
>	- Funções podem receber dados de entrada (parâmetros ou argumentos);
>	- Funções podem ou não retornar uma saída.
>- Em orientação a objetos, funções em classes recebem o nome de "métodos".

>[!example] Problema exemplo
>- Fazer um programa para ler três números inteiros e mostrar na tela o maior deles.
>![[../0 - Imagens/exemploBitwise.png]]

```Java title:"Solução simples"
package course; 
import java.util.Scanner; 

public class Program { 
	public static void main(String[] args) { 
	Scanner sc = new Scanner(System.in);
	
	System.out.println("Enter three numbers:"); 
	int a = sc.nextInt(); 
	int b = sc.nextInt(); 
	int c = sc.nextInt(); 
	
	if (a > b && a > c) { 
		System.out.println("Higher = " + a);
	} else if (b > c) {
		System.out.println("Higher = " + b);
	} else { 
		System.out.println("Higher = " + c); } sc.close(); 
	} 
}
```

```Java title:"Com a criação de função"
package course; 
import java.util.Scanner; 

public class Program {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		System.out.println("Enter three numbers:"); 
		int a = sc.nextInt();
		int b = sc.nextInt();
		int c = sc.nextInt();
		int higher = max(a, b, c); 
		showResult(higher); 
		
		sc.close();
	} 
	
	// função para definir qual valor dos três recebidos é o maior
	public static int max(int x, int y, int z) {
		int aux; 
		if (x > y && x > z) {
			aux = x;
		} else if (y > z) {
			aux = y;
		} else { 
			aux = z; 
		} 
		return aux; 
	} 
	
	// função de receber um valor e imprimir na tela
	public static void showResult(int value) { 
	System.out.println("Higher = " + value);
	} 
}
```

---