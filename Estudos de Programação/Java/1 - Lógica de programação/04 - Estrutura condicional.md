# Expressões comparativas
>[!quote] Definição
>- são expressões que comparam uma coisa com outra, podendo se obter um resultado como verdadeiro ou falso: 
>	- Exemplo - "5>10" = falso.
## Operadores comparativos:
![[../0 - Imagens/operadoresComparativos.png]]
### Exemplos de expressões comparativas
- Suponha que x = 5
	- X > 0 - Resultado: V
	- X == 3 - Resultado: F
	- 10 <= 30 - Resultado: V
	- X != 2 - Resultado: V
---
# Expressões lógicas
>[!quote] Definição
>- São expressões avaliadas que dão um valor verdade (verdadeiro ou falso);
## Operadores lógicos
![[../0 - Imagens/operadoresLogicos.png|500]]
## Ideia por trás do operador "E"
- <mark style="background: #FF5582A6;">Todas as condições devem ser verdadeiras</mark>, exemplo: "Você pode obter uma habilitação de motorista se:"
	- For aprovado no exame psicotécnico, <mark style="background: #FF5582A6;">E</mark> for aprovado no exame de legislação, <mark style="background: #FF5582A6;">E</mark> for aprovado no exame de direção.
### Exemplos de expressões lógicas
- Suponha que x = 5:
	- X <= 20 && **X == 10** - Resultado: F, pois x não é igual a 10;
	- X > 0 && X != 3 - Resultado: V, pois ambos são verdades;
	- X <= 20 && **X == 10** && X != 3 - Resultado: F, pois x não é igual a 10.
### Tabela verdade do operador "E"
![[../0 - Imagens/operadorE.png|300]]

## Ideia por trás do operador "OU"
- <mark style="background: #FFB86CA6;">Pelo menos uma condição deve ser verdadeira para que o resultado seja verdadeiro</mark>, exemplo: "Você pode estacionar na vaga especial se:"
	- For idoso(a), <mark style="background: #FFB86CA6;">OU</mark> for uma pessoa com deficiência, <mark style="background: #FFB86CA6;">OU</mark> for uma gestante.
### Exemplo de ou
- Suponha que x = 5:
	- X == 10 | | X <= 20 - Resultado: V;
	- X > 0 | | X != 3 - Resultado: V;
	- X <= 0 | | X != 3 | | X != 5 - Resultado: V.
### Tabela verdade do operador "OU"
![[../0 - Imagens/operadorOU.png|300]]

## Ideia por trás do operador "NÃO"
- <mark style="background: #FFF3A3A6;">O operador inverte a condição</mark>, exemplo: "Você tem direito a receber uma bolsa de estudos se você: não possuir renda maior que $ 3000,00 "
	- Pedro recebe $4500,00 - Falso, pois tem renda maior que $ 3000,00;
	- Luiz recebe $2000,00 - Verdadeiro, pois não tem renda maior que $ 3000,00.
### Exemplos de "NÃO"
- suponha x = 5:
	- !(X == 10) - Resultado: V
	- !(X >= 2) - Resultado: F
	- !(X <= 20 && **X == 10**) - Resultado: V, pois originalmente seria falso por causa de "**X == 10**", porém por possuir um operador não, se torna verdadeira 
### Tabela verdade do operador "NÃO"
 ![[../0 - Imagens/operadorNao.png|250]]

---
# Estrutura condicional
- É uma estrutura de controle que <mark style="background: #BBFABBA6;">permite definir que um certo bloco de comando somente será executado dependendo de uma condição</mark>.
## Sintaxe de estrutura condicional
- Simples: <mark style="background: #BBFABBA6;">se verdadeira, executa o bloco de comandos</mark>, se não, pula ele
``` title:"Estrutura simples"
if (<condicao>) { 
	<comando1>
	<comando2>
}
```

- Composta: <mark style="background: #BBFABBA6;">se verdadeira, executa somente o bloco if</mark>, se não, executa o bloco do else
``` title:"Estrutura composta"
if (<condicao>) { 
	<comando1>
	<comando2>
} 
else { 
	<comando3>
	<comando4>
}
```

- Com mais de duas possibilidades: Encadeamento de estruturas condicionais
```
if (condição1) {
	comando1 
	comando2 
} else if (condição2) {
	comando3 
	comando4 
} else { 
	comando5 
	comando6 
}
```

## Sintaxe opcional: operadores de atribuição cumulativa

>[!example] Problema exemplo:
> - Uma operadora de telefonia cobra R$ 50.00 por um plano básico que dá direito a 100 minutos de telefone. Cada minuto que exceder a franquia de 100 minutos custa R$ 2.00. Fazer um programa para ler a quantidade de minutos que uma pessoa consumiu, daí mostrar o valor a ser pago.

```Java title:"Método sem atribuição cumulativa" destaque:12
import java.util.Locale; 
import java.util.Scanner; 

public class Main { 
	public static void main(String[] args) {
		Locale.setDefault(Locale.US); 
		Scanner sc = new Scanner(System.in); 
		
		int minutos = sc.nextInt(); 
		double conta = 50.0; 
		if (minutos > 100) { 
			conta = conta + (minutos - 100) * 2.0; 
		}
		
		System.out.printf("Valor da conta = R$ %.2f%n", conta);
		sc.close(); 
	}
}
```
-  Usando operadores de atribuição cumulativa
```Java title:"Método com atribuição cumulativa" destaque:12
import java.util.Locale; 
import java.util.Scanner; 

public class Main { 
	public static void main(String[] args) {
		Locale.setDefault(Locale.US); 
		Scanner sc = new Scanner(System.in); 
		
		int minutos = sc.nextInt(); 
		double conta = 50.0; 
		if (minutos > 100) { 
			conta += (minutos - 100) * 2.0; 
		}
		
		System.out.printf("Valor da conta = R$ %.2f%n", conta);
		sc.close(); 
	}
}
```

- Operadores de atribuição cumulativa
![[../0 - Imagens/operacaoAtribuicaoCumulativa.png]]
## Sintaxe opcional: switch-case

>[!quote] Definição
>- Estrutura switch-case: <mark style="background: #ABF7F7A6;">Quando se tem várias opções de fluxo a serem tratadas com base no valor de uma variável</mark>, ao invés de várias estruturas if-else encadeadas, alguns preferem utilizar a estrutura switch-case.

- Problema exemplo: Fazer um programa para ler um valor inteiro de 1 a 7 representando um dia da semana (sendo 1=domingo, 2=segunda, e assim por diante). Escrever na tela o dia da semana correspondente, conforme exemplos.
```Java title:"Sem uso de switch-case"
import java.util.Scanner; 
public class Main { 
	public static void main(String[] args) { 
		Scanner sc = new Scanner(System.in); 
		int x = sc.nextInt(); 
		String dia; 
		
		if (x == 1) { 
			dia = "domingo"; 
		} else if (x == 2) { 
			dia = "segunda"; 
		} else if (x == 3) { 
			dia = "terca"; 
		} else if (x == 4) { 
			dia = "quarta"; 
		} else if (x == 5) { 
		dia = "quinta"; 
		} else if (x == 6) { 
		dia = "sexta"; 
		} else if (x == 7) { 
		dia = "sabado"; 
		} else { 
			dia = "valor invalido"; 
		} 
		
		System.out.println("Dia da semana: " + dia); sc.close();
	}
}
```

```Java title:"Com uso de switch-case" destaque:9
import java.util.Scanner; 
	public class Main { 
		public static void main(String[] args) { 
		
		Scanner sc = new Scanner(System.in); 
		int x = sc.nextInt(); 
		String dia; 
		
		switch (x) { 
		case 1: 
			dia = "domingo"; 
			break; 
		case 2: 
			dia = "segunda"; 
			break; 
		case 3: 
			dia = "terca"; 
			break; 
		case 4: 
			dia = "quarta"; 
			break; 
		case 5: 
			dia = "quinta";
			break; 
		case 6: 
			dia = "sexta"; 
			break; 
		case 7: 
			dia = "sabado"; 
			break; 
		default: 
			dia = "valor invalido"; 
			break; 
		} 
		
		System.out.println("Dia da semana: " + dia);
		sc.close();
	}
}
```

```Java title:"Sintaxe do switch-case" 
switch ( expressão ) { 
case valor1: 
	comando1;
	comando2;
	break; 
case valor2: 
	comando3;
	comando4;
	break; 
default: 
	comando5;
	comando6;
	break; 
}
```
## Expressão condicional ternária
- Estrutura opcional ao if-else quando se deseja decidir um VALOR com base em uma condição
```Java title:"Sintaxe"
( condição ) ? valor_se_verdadeiro : valor_se_falso

( 2 > 4 ) ? 50 : 80 // resultado: 80 pois é falso
( 10 != 3 ) ? "Maria" : "Alex" // resultado: maria pois é verdadeiro
```

```Java title:"Demonstração com a expressão condicional ternária" destaque:11 
//demonstração sem expressão condicional ternária
double preco = 34.5; 
double desconto; 
if (preco < 20.0) { 
	desconto = preco * 0.1; 
} else { 
	desconto = preco * 0.05; 
}

//demonstração com expressão condicional ternária
double preco = 34.5; 
double desconto = (preco < 20.0) ? preco * 0.1 : preco * 0.05;
```

---
# Escopo e inicialização
>[!quote] Do que se trata (atualmente)
>- **Escopo de uma variável: é a região do programa onde a variável é válida**, ou seja, onde ela pode ser referenciada. 
>- **Uma variável não pode ser usada se não for iniciada**.

```Java title:"" title:"Demonstração" destaque:3,6
double price = sc.nextDouble();

double discount = 0.0; // deve ser atribuida antes, e não apenas no bloco isolado, para que seja reconhecida em todo o código

if (price > 100.0) { 
	double discount = price * 0.1; 
} 

System.out.println(discount);
```

---