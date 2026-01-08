# Resolvendo um problema sem orientação a objetos
>[!example] Problema exemplo
> ![[../0 - Imagens/problemaExemploSemOO.png]]
> ![[../0 - Imagens/problemaExemploSemOOSaida.png]]

```Java title:"Solução sem POO" destaque:11
package application; 

import java.util.Locale; 
import java.util.Scanner; 

public class Program {
	public static void main(String[] args) {
	Locale.setDefault(Locale.US); 
	Scanner sc = new Scanner(System.in); 
	
	double xA, xB, xC, yA, yB, yC; 
	System.out.println("Enter the measures of triangle X: "); 
	xA = sc.nextDouble(); 
	xB = sc.nextDouble(); 
	xC = sc.nextDouble(); 
	
	System.out.println("Enter the measures of triangle Y: "); 
	yA = sc.nextDouble(); 
	yB = sc.nextDouble(); 
	yC = sc.nextDouble(); 
	double p = (xA + xB + xC) / 2.0; 
	double areaX = Math.sqrt(p * (p - xA) * (p - xB) * (p - xC)); 
	p = (yA + yB + yC) / 2.0; 
	double areaY = Math.sqrt(p * (p - yA) * (p - yB) * (p - yC)); 
	System.out.printf("Triangle X area: %.4f%n", areaX);
	System.out.printf("Triangle Y area: %.4f%n", areaY); 
	
	if (areaX > areaY) { 
		System.out.println("Larger area: X"); 
	} else { 
		System.out.println("Larger area: Y"); 
	} 
	sc.close(); 
}
```
---
# Criando uma classe com três atributos para representar melhor o triângulo
### Discussão
- <mark style="background: #FF5582A6;">Triângulo é uma entidade com três atributos: a, b, c.</mark>
- Estamos usando três variáveis distintas para representar cada triângulo:
	- `double aX, bX, cX, aY, bY, cY;` 
	- Na memória:
		![[../0 - Imagens/atributosEmMemoria.png]]
- <mark style="background: #FF5582A6;">Para melhorar isso, será criado uma classe para representar um triângulo;</mark>

>[!quote] Classe
> - **É um tipo estruturado que pode conter** (membros): 
> 	- <mark style="background: #FF5582A6;">Atributos (dados / campos)</mark>: está relacionado com as características de um objeto;(exemplo) os lados dos triângulos, indicando o comprimento deles
> 	- <mark style="background: #FF5582A6;">Métodos</mark> (funções / operações): 
> 	
> - **A classe também pode prover muitos outros recursos**, tais como: 
> 	- <mark style="background: #FF5582A6;">Construtores; Sobrecarga; Encapsulamento;^[[08 - Contrutores, palavra this, sobrecarga, encapsulamento]] Herança; Polimorfismo^[[12 - Herança e polimorfismo]]</mark>.
> 	
> - Exemplos:
> 	- **Entidades**: Produto, Cliente, Triangulo
> 	- **Serviços**: ProdutoService, ClienteService, EmailService, StorageService
> 	- **Controladores**: ProdutoController, ClienteController 
> 	- **Utilitários**: Calculadora, Compactador
> 	- **Outros** (views, repositórios, gerenciadores, etc.)
### Aplicação da classe
```Java title:"Definição da classe Triangle"
package entities; 

public class Triangle {
	// atributos do triangulo
	public double a;
	public double b;
	public double c;
}
```
- alteração na memória:
	![[../0 - Imagens/alteracaoMemoriaPonteiro.png]]
	- Note que <mark style="background: #FFB86CA6;">"Triangle" se torna um tipo composto, isso é, possui três objetos em cada variável definida</mark>;
		- A variável x, por exemplo, aponta para um objeto composto por três atributos. Condensando as informações em uma única variável.
	- <mark style="background: #FF5582A6;">Quando a variável é do tipo classe, se deve instanciar a variável para que seja criada</mark>, sendo necessário chamar o `new Triangle();` .

```Java title:"Código com a classe Triangle importada" destaque:12-13
package application; 

import java.util.Locale; 
import java.util.Scanner; 
import entities.Triangle; 

public class Program { 
	public static void main(String[] args) {
		Locale.setDefault(Locale.US); 
		Scanner sc = new Scanner(System.in);
		Triangle x, y;
		x = new Triangle();
		y = new Triangle(); 
		
		System.out.println("Enter the measures of triangle X: "); 
		x.a = sc.nextDouble(); 
		x.b = sc.nextDouble(); 
		x.c = sc.nextDouble(); 
		
		System.out.println("Enter the measures of triangle Y: "); 
		y.a = sc.nextDouble(); 
		y.b = sc.nextDouble(); 
		y.c = sc.nextDouble(); 
		
		double p = (x.a + x.b + x.c) / 2.0; 
		double areaX = Math.sqrt(p * (p - x.a) * (p - x.b) * (p - x.c)); 
		p = (y.a + y.b + y.c) / 2.0; 
		double areaY = Math.sqrt(p * (p - y.a) * (p - y.b) * (p - y.c));
		// (...)
	}
}
```
### Instanciação
- <mark style="background: #FFF3A3A6;">Quando as variáveis são definidas, elas são criadas na "Stack" da memória</mark>, área onde são criadas as variáveis estáticas (declaradas);
- <mark style="background: #FFF3A3A6;">Pode-se fazer alocação dinâmica de memória durante a execução de um programa</mark>, usando o "New";
- **Quando se usa `x = New Triangle();`, será instanciado um objeto do tipo Triangle numa outra área da memória chamada** <mark style="background: #FFF3A3A6;">HEAP, área da memória onde são criadas os objetos dinâmicos durante a execução;</mark>
- A variável x, existe durante a execução, porém não está com os dados do Triangle, <mark style="background: #FFF3A3A6;">dentro dela há um endereço de memória do objeto criado no HEAP;</mark>
	- x é uma referência para um objeto armazenado no HEAP.
	- ![[../0 - Imagens/ponteiroInstanciacao.png]]
	- A seta indica um ponteiro para a memória onde os atributos estão armazenados na memória HEAP.

>[!hint] Lembre-se
>- Classe: definição do tipo
>- Objeto: instâncias da classe
>- Atributos: dados e campos da classe


---
# Criando um método para obtermos os benefícios de reaproveitamento e delegação
## Discussão
- Com o uso de CLASSE, agora nós **temos uma variável composta do tipo "Triangle" para representar cada triângulo** :
```Java title:"representação dos triângulos"
Triangle x, y; 
x = new Triangle(); 
y = new Triangle();
```

- Agora vamos melhorar nossa CLASSE, acrescentando nela um MÉTODO para calcular a área.
	- Na própria classe, **deverá ter um método que calcula a área para eliminar os códigos de cálculo da classe principal**
```Java title:"Classe Triangle"
package entities; 

public class Triangle {
	public double a;
	public double b;
	public double c; 
	
	public double area() { // aqui os atributos da classe serão calculados e será retornado o valor da área
		double p = (a + b + c) / 2.0; 
		return Math.sqrt(p * (p - a) * (p - b) * (p - c)); 
	}
}
```

```Java title:"Codigo principal atualizado" destaque:26-27
package application; 

import java.util.Locale; 
import java.util.Scanner; 
import entities.Triangle; 

public class Program {
	public static void main(String[] args) {
	Locale.setDefault(Locale.US); 
	Scanner sc = new Scanner(System.in); 
	
	Triangle x, y;
	x = new Triangle();
	y = new Triangle();
	
	System.out.println("Enter the measures of triangle X: ");
	x.a = sc.nextDouble(); 
	x.b = sc.nextDouble(); 
	x.c = sc.nextDouble(); 
	
	System.out.println("Enter the measures of triangle Y: ");
	y.a = sc.nextDouble(); 
	y.b = sc.nextDouble(); 
	y.c = sc.nextDouble(); 
	
	double areaX = x.area(); 
	double areaY = y.area(); 
	(...)
	}
}
```
### Estrutura da classe
![[../0 - Imagens/estruturaClasse.png]]
#### Projeto de classe (UML)
- Diagrama que representa as classes
	![[../0 - Imagens/estruturaClasseUML.png]]
## Síntese
>[!hint] Vantagens da criação de classes
>- Quais são os <mark style="background: #BBFABBA6;">benefícios de se calcular a área de um triângulo por meio de um MÉTODO dentro da CLASSE Triangle</mark>? 
 > 1) <mark style="background: #BBFABBA6;">Reaproveitamento de código:</mark> nós eliminamos o código repetido (cálculo das áreas dos triângulos x e y) no programa principal;
 > 2) <mark style="background: #BBFABBA6;">Delegação de responsabilidades:</mark> quem deve ser responsável por saber como calcular a área de um triângulo é o próprio triângulo. A lógica do cálculo da área não deve estar em outro lugar.

---
# Começando a resolver um segundo problema exemplo

> [!example] Outro exemplo
> - **Fazer um programa para ler os dados de um produto em estoque** (nome, preço e quantidade no estoque). Em seguida: 
> 	- **Mostrar os dados do produto** (nome, preço, quantidade no estoque, valor total no estoque) ;
> 	- **Realizar uma entrada no estoque e mostrar novamente os dados do produto;**
> 	- **Realizar uma saída no estoque e mostrar novamente os dados do produto** 
> 	
> 	- Para resolver este problema, você deve criar uma CLASSE conforme projeto ao lado:
> 	![[../0 - Imagens/segProblemaExemploPOO.png]]

## Object e ToString

> [!quote] Síntese 
>- <mark style="background: #ABF7F7A6;">Toda classe em Java é uma subclasse da classe Object; </mark>
>- **Object possui os seguintes métodos**: 
>	- getClass- retorna o tipo do objeto;
>	- equals - compara se o objeto é igual a outro;
>	- hashCode - retorna um código hash do objeto;
>	- toString - converte o objeto para string.

```Java title:"Class Product" destaque:13,17 
package entities; 

public class Product {
	public String name; 
	public double price; 
	public int quantity;
	
	public double totalValueInStock() { // calcula quanto em moeda vale o estoque
		return price * quantity;
	}
	
	public void addProducts(int quantity) { // adiciona mais produtos ao estoque
		this.quantity += quantity; 
	}
	
	public void removeProducts(int quantity) { // remove produtos do estoque
		this.quantity -= quantity; 
	} 
	
	public String toString() {
		return name + ", $ " + String.format("%.2f", price) + ", " + quantity + " units, Total: $ " + String.format("%.2f", totalValueInStock());
	} 
}
```

- <mark style="background: #ADCCFFA6;">"toString": converte toda a concatenação, ou qualquer valor também, em "string", sendo possível definir uma função que retornará um texto.</mark>

>[!note] Palavra this
> - **Palavra reservada que significa uma auto referência para o objeto**. Quando usado, indica que o atributo da classe será usado diretamente, e não o parâmetro.

## Terminando o problema exemplo
```Java title:"Codigo Program completo"
package application; 

import java.util.Locale; 
import java.util.Scanner; 
import entities.Product; 

public class Program {
	public static void main(String[] args) {
		Locale.setDefault(Locale.US);
		Scanner sc = new Scanner(System.in);
		Product product = new Product();
		
		System.out.println("Enter product data: "); // adiciona produtos
		System.out.print("Name: ");
		product.name = sc.nextLine();
		System.out.print("Price: ");
		product.price = sc.nextDouble();
		System.out.print("Quantity in stock: ");
		product.quantity = sc.nextInt(); 
		System.out.println();
		
		System.out.println("Product data: " + product); // informa o estoque
		System.out.println();
		
		// adiciona mais itens ao estoque
		System.out.print("Enter the number of products to be added in stock: ");
		int quantity = sc.nextInt(); 
		product.addProducts(quantity);
		System.out.println();
		System.out.println("Updated data: " + product);
		System.out.println();
		
		// remove itens do estoque
		System.out.print("Enter the number of products to be removed from stock: ");
		quantity = sc.nextInt(); 
		product.removeProducts(quantity);
		System.out.println();
		
		System.out.println("Updated data: " + product);
		sc.close(); 
	} 
}
```

---
# Membros estáticos
>[!quote] Definição
>- Também chamados membros de classe 
>	- Em oposição a membros e instância
>- <mark style="background: #FF5582A6;">São membros que fazem sentido independentemente de objetos. Não precisam de objeto para serem chamados.</mark> São chamados a partir do próprio nome da classe.
>	- **"Dá o mesmo resultado independente de qualquer objeto".**
><mark style="background: #FFF3A3A6;">- Aplicações comuns: </mark>
>	- <mark style="background: #FFF3A3A6;">Classes utilitárias - Exemplo: Math.sqrt(double)</mark>
>	- <mark style="background: #FFF3A3A6;">Declaração de constantes </mark>
>- ***Uma classe que possui somente membros estáticos, pode ser uma classe estática também. Esta classe não poderá ser instanciada.***

## Problema exemplo
>[!example] Problema exemplo
>- Fazer um programa para ler um valor numérico qualquer, e daí mostrar quanto seria o valor de uma circunferência e do volume de uma esfera para um raio daquele valor. Informar também o valor de PI com duas casas decimais.
### Versão 1: métodos na própria classe do programa
```Java title:"Program.java" destaque:23-29
package application; 

import java.util.Locale;
import java.util.Scanner;

public class Program {
	public static final double PI = 3.14159;
	
	public static void main(String[] args) { 
		Locale.setDefault(Locale.US); 
		Scanner sc = new Scanner(System.in);
		System.out.print("Enter radius: ");
		double radius = sc.nextDouble(); 
		double c = circumference(radius);
		double v = volume(radius); 
		 
		System.out.printf("Circumference: %.2f%n", c);
		System.out.printf("Volume: %.2f%n", v);
		System.out.printf("PI value: %.2f%n", PI); 
		sc.close(); 
	} 
	
	public static double circumference(double radius) { 
		return 2.0 * PI * radius;
	} 
	
	public static double volume(double radius) { 
		return 4.0 * PI * radius * radius * radius / 3.0; 
	} 
}
```

---
### Versão 2: classe Calculator com membros de instância
```Java title:"Classe Calculator" 
package util; 

public class Calculator { 
	public final double PI = 3.14159;
	
	public double circumference(double radius) {
		return 2.0 * PI * radius;
	} 	
	public double volume(double radius) {
		return 4.0 * PI * radius * radius * radius / 3.0; 
	}
}
```

```Java title:"Program.java" destaque:2,6-7
(...)
		Calculator calc = new Calculator(); 
		System.out.print("Enter radius: "); 
		
		double radius = sc.nextDouble();
		double c = calc.circumference(radius);
		double v = calc.volume(radius);
		
		System.out.printf("Circumference: %.2f%n", c);
		System.out.printf("Volume: %.2f%n", v);
		System.out.printf("PI value: %.2f%n", calc.PI);
(...)
```

---
### Versão 3: classe Calculator com método estático
```Java title:"Class Calculator" destaque:5,7,10
package util; 

public class Calculator {
	
	public static final double PI = 3.14159;
	
	public static double circumference(double radius) {
		return 2.0 * PI * radius; 
	} 
	public static double volume(double radius) {
		return 4.0 * PI * radius * radius * radius / 3.0; 
	} 
}
```

```Java title:"Program.java" destaque:2-4
		System.out.print("Enter radius: "); 
		double radius = sc.nextDouble(); 
		double c = Calculator.circumference(radius); 
		double v = Calculator.volume(radius); 
		
		System.out.printf("Circumference: %.2f%n", c);
		System.out.printf("Volume: %.2f%n", v);
		System.out.printf("PI value: %.2f%n", Calculator.PI);
```

---
