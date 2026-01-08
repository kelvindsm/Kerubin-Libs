# Entendendo as versões do Java
- Existem versões mais atuais e existem versões mais antigas que possuem suporte a longo prazo, chamadas de LTS ("Long Term Support", suporte de longo tempo).
---
# Contextualização
## O que é o Java
- Linguagem de programação (Regras sintáticas: [[01 - Conceitos de programação]])
- Plataforma de desenvolvimento e execução:
	- Bibliotecas (API); Ambientes de execução;
## Histórico
- Problemas resolvidos e motivos de sucesso:
	- <mark style="background: #FF5582A6;">Ponteiros / gerenciamento de memória: </mark> Era necessário definir quais variáveis eram Ponteiro e quais eram de valor, eram controlados manualmente, causando dificuldades para o programador e tornando os softwares mais suscetíveis a erros;
	- <mark style="background: #FF5582A6;">Portabilidade falha:</mark> reescrever parte do código ao mudar de SO - alteração obrigatória para que o código funcione em outros sistemas;
	- <mark style="background: #FF5582A6;">Utilização em dispositivos diversos:</mark> não era possível rodar o mesmo programa em vários dispositivos;
	- <mark style="background: #FF5582A6;">Custo</mark>.
- Criado pela Sun Microsystems no meio da década de 1990 e adquirida pela Oracle em 2010.
## Aspectos notáveis
- <mark style="background: #FFB86CA6;">Código compilado para bytecode e executado em máquina virtual (JVM);</mark>
- Portável, segura, robusta;
- **Roda em vários tipos de dispositivos;**
- Domina o mercado corporativo desde o fim do século 20;
- **Padrão Android por muitos anos - após um tempo, o sistema android mudou suas aplicações para Kotlin.**
## Edições 
- Java ME: Java Micro Edition - dispositivos embarcados e móveis - IoT
- Java SE: Java Standard Edition - core - desktop e servidores
- Java EE: Java Enterprise Edition - aplicações corporativas
---
# Máquina virtual do Java
- <mark style="background: #FFF3A3A6;">JVM - Java Virtual Machine: necessário para executar sistemas Java;</mark>
- Por ser uma **abordagem híbrida, a linguagem Java foi inovadora por funcionar em diversos sistemas sem que haja grande mudança no código fonte;** ^[leia mais em [[01 - Conceitos de programação]]]
---
# Estrutura de uma aplicação Java
- Java é uma linguagem orientada a objetos, composta por classes. **Todo o código deve estar dentro de classes;**
- <mark style="background: #BBFABBA6;">Packages: agrupamento lógico de classes relacionadas</mark> - Exemplos: entities (produtos, clientes, pedidos...), Services (email, pedidos, logins) e Repositories(acessam os dados)
- Módulos (Java9+): agrupamento lógico de pacotes relacionais - Nível conceitual
	- Runtime: agrupamento físico, representado por arquivos, que rodam nos dispositivos
- **Aplicação: Agrupamento de módulo relacionados**

```java title:"Primeira aplicação Java" 
public class Main {  
  
    public static void main(String[] args) {  
    
        System.out.println("Hello World");  
        
    } // declaração de função: um programa Java deve ter ao menos uma;  
    // É onde a execução do programa se inicia, aqui é onde se coloca o algorítmo}
```

---