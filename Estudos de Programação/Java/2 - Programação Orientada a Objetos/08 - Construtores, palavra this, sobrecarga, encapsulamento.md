# Construtores
>[!quote] Definição
>- Operação especial da classe, executa no momento da instanciação do objeto
>- Usos comuns:
>	- Iniciar valores dos atributos;
>	- Permite ou obriga que o objeto receba dados / dependencias no momento de sua instanciação (injeção de dependência).
>- Se um construtor customizado não for especificado, a classe disponibiliza o construtor padrão: `Product p = new Product();` .
>- É possível especifica mais de um construtor na mesma classe (sobrecarga).

> [!quote] Problema exemplo anterior
> - **Fazer um programa para ler os dados de um produto em estoque** (nome, preço e quantidade no estoque).
> 	
> ![[../0 - Imagens/segProblemaExemploPOO 1.png]]
>>[!warning] Problema
>>- Quando executado os comandos da questão, os atributos de um produto "product" é instanciado como vazio, o que não faz sentido um produto não possuir nome, quantidade e preço.
>
>>[!tip] Solução
>> - Para que seja obrigatória a inserção desses valores, é necessário criar um construtor que solicite esses dados num primeiro momento.

```Java title:"Classe Product, com o construtor"
package entities;
public class Product { 
	public String name;
	public double price;
	public int quantity;
	
	public Product(String name, double price, int quantity) {
	this.name = name; 
	this.price = price;
	this.quantity = quantity; 
	} 
(...)
```
---
```Java title:"Program atualizado para receber a alteração"
System.out.println("Enter product data: ");
System.out.print("Name: "); 
String name = sc.nextLine(); 
System.out.print("Price: "); 
double price = sc.nextDouble(); 

System.out.print("Quantity in stock: ");
int quantity = sc.nextInt();
Product product = new Product(name, price, quantity);
```
---
# Palavra this
>[!quote] Definição
>- É uma referência para o próprio objeto
>- Usos comuns:
>	- Diferenciar atributos de variáveis locais;
>	- Passar o próprio objeto como argumento na chamada de um método ou construtor
### Diferenciar atributos de variáveis locais
- Com o uso da palavra this, se tem acesso ao valor da variável que foi atribuído no momento da inserção dos dados pelo escopo do construtor; 
---
# Sobrecarga
>[!quote] Definição
>- É um recurso que uma classe possui de oferecer mais de uma operação com o mesmo nome, porém com diferentes listas de parâmetros.

>[!todo] Proposta de melhoria
> - Vamos criar um construtor opcional, o qual recebe apenas nome e preço do produto. A quantidade em estoque deste novo produto, por padrão, deverá então ser iniciada com o valor zero.
> - Nota: é possível também incluir um construtor padrão.

---

```Java title:"Melhoria em Product"
package entities;
public class Product { 
	public String name; 
	public double price; 
	public int quantity; 
	
	public Product() {
	} 
	public Product(String name, double price, int quantity) {
		this.name = name;
		this.price = price;
		this.quantity = quantity;
	} 
	public Product(String name, double price) {
		this.name = name; 
		this.price = price; 
	} 
(...)
```

---
# Encapsulamento
>[!quote] Definição
>- É um princípio que consiste em esconder detalhes de implementação de uma classe, expondo apenas operações seguras e que mantenham os objetos em um estado consistente;
>- É como um aparelho eletrônico, onde o usuário só possui acesso aos botões de interface, porém, seus componentes internos são são acessados com facilidade.
## Regra básica
- Um objeto NÃO deve expor nenhum atributo (modificador de acesso private);
- Os atributos devem ser acessados por meio de métodos get e set:
	- Padrão JavaBeans: https://en.wikipedia.org/wiki/JavaBeans

```Java title:"Exemplo de get e set na classe Product" destaque:10,13
package entities; 

public class Product { 
	private String name; // variáveis privadas
	private double price;
	private int quantity; 
	
	(...)
	
	public String getName() { 
		return name;
	} // torna a chamada da variável possível
	public void setName(String name) { 
		this.name = name;
	} // torna possível alterar o valor da variável
	public double getPrice() {
		return price;
	} 
	public void setPrice(double price) { 
		this.price = price;
	} 
	public int getQuantity() {
		return quantity;
	}
(...)
```

---
