# Estrutura while (enquanto)
>[!quote] Definição
>- <mark style="background: #FFB8EBA6;">Repete um bloco de comando enquanto uma condição for verdadeira;</mark>
>- Quando **usar: quando não se sabe previamente a quantidade de repetições que será realizada**.

- Sintaxe:
```
while ( condição ) { 
	comando 1 
	comando 2 
}
```
- <mark style="background: #FFB8EBA6;">Regra - V: executa e volta F: pula fora.</mark>

>[!example] Problema exemplo:
>- Fazer um programa que lê números inteiros até que um zero seja lido. Ao final mostra a soma dos números lidos.

```Java title:"Resolução"
import java.util.Scanner;  
  
public class Main {  
	public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
		
        System.out.println("Digite um valor (0 para terminar): ");  
        int numero = -1;  
        int soma = 0;  
		
        while (numero != 0) {  
            numero = sc.nextInt();  
            soma += numero;  
        }  
        System.out.println("SOMA = " + soma);  
  
        sc.close();  
    }  
}
```

---
# Estrutura for (para)
>[!quote] Definição
> - <mark style="background: #FF5582A6;">Repete um bloco de comandos para um certo intervalo de valores;</mark>
> - Quando **usar: quando se sabe previamente a quantidade de repetições, ou o intervalo de valores.**

- Sintaxe:
	![[../0 - Imagens/estruturaFOR.png]]

>[!example] Problema exemplo
> - Problema exemplo: Fazer um programa que lê um valor inteiro N e depois N números inteiros. Ao final, mostra a soma dos N números lidos.

```Java title:"Resolução"
import java.util.Scanner;  
  
public class Main {  
  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
  
        int lim = sc.nextInt();  
        int soma = 0;  
  
        for(int i = 0; i < lim; i++){  
            int valor = sc.nextInt();  
            soma += valor;  
        }  
        System.out.println("SOMA = " + soma);  
  
        sc.close();  
    }  
}
```

### Importante
- Perceba que <mark style="background: #FF5582A6;">a estrutura for é ótima para se fazer uma repetição baseada em uma CONTAGEM</mark>:
```Java title:"contagem ou contador"
for (int i=0; i<5; i++) { 
	System.out.println("Valor de i: " + i); 
}
```

```Java title:"Contagem regressiva"
for (int i=4; i>=0; i--) { 
	System.out.println("Valor de i: " + i); 
}
```

---
# Estrutura do-while (faça-enquanto)
>[!quote] Definição
>- <mark style="background: #FFB86CA6;">O bloco de comandos executa pelo menos uma vez, pois a condição é verificada no final.</mark>

- Sintaxe
```
do { 
	comando1 
	comando2 
} while ( condição );
// regra - V: volta F: pula fora
```

>[!example] Problema exemplo
>- Fazer um programa para ler uma temperatura em Celsius e mostrar o equivalente em Fahrenheit. Perguntar se o usuário deseja repetir (s/n). Caso o usuário digite "s", repetir o programa. $$ Fórmula: \frac{9C}{5} + 32$$
>	![[../0 - Imagens/ExemploDoWhile.png|500]]

```Java title:"Resolução do problema"
import java.util.Locale;
import java.util.Scanner;

public class Main { 
	public static void main(String[] args) {
		Locale.setDefault(Locale.US);
		Scanner sc = new Scanner(System.in);
		char resp;
		
		do { 
			System.out.print("Digite a temperatura em Celsius: ");
			double C = sc.nextDouble();
			double F = 9.0 * C / 5.0 + 32.0;
			System.out.printf("Equivalente em Fahrenheit: %.1f%n", F);
			System.out.print("Deseja repetir (s/n)? "); 
			resp = sc.next().charAt(0);
		} while (resp != 'n'); 
		sc.close(); 
	} 
}
```

---