---
tags:
  - Concluido
---
# Engenharia de Requisitos: Processo de Produção e Gerenciamento

## 1. O Processo da Engenharia de Requisitos

A **Engenharia de Requisitos** é uma "engenharia dentro da Engenharia de Software" , cujo objetivo é criar e manter a documentação de requisitos do sistema.

O trabalho da ER se divide em dois grandes blocos: **Produção/Desenvolvimento de Requisitos** e **Gerenciamento de Requisitos**.

>[!quote] Citação de Edward V. Berard
> "Caminhar sobre a água e desenvolver software a partir de uma especificação de requisitos é fácil se ambos estão congelados".
> 
> *Esta citação sublinha a volatilidade inerente aos requisitos.*
### 1. Etapas da Produção ou Desenvolvimento de Requisitos
O processo de produção envolve quatro macro-etapas, que são cíclicas e inter-relacionadas:
1. **Elicitação:** Investigação, busca, descoberta dos requisitos.
2. **Análise:** Avaliação de possíveis conflitos, identificação das relações com o contexto, definição dos requisitos.
3. **Especificação:** Documentação e detalhamento das especificações dos requisitos.
4. **Validação:** Validação dos requisitos em relação aos propósitos do produto de software.
## I. Elicitação de Requisitos
A Elicitação é a etapa de investigação dos requisitos e é o ponto mais crítico da **Engenharia de Requisitos**.
- **Conceito:** Denota uma <mark style="background: #FF5582A6;">busca ativa pelos requisitos</mark>, exigindo uma postura proativa do analista.
- **Termos Alternativos:** Captura de requisitos, descoberta de requisitos ou aquisição de requisitos.
- **Comunicação:** O processo <mark style="background: #FF5582A6;">exige intensa comunicação com os Stakeholders</mark>. *Comunicação ineficaz pode levar a requisitos incompletos e incorretos*.
- **Abordagens Ágeis:** Em projetos ágeis, <mark style="background: #FF5582A6;">os requisitos podem emergir em diversos momentos, compondo o product backlog.</mark> Não é necessário ter todos os requisitos detalhados no início.

>[!note] Quanto à elicitação de requisitos
>- É uma fase que busca descobrir, coletar e refinar as necessidades dos *stakeholders* para descobrir o que o sistema deverá fazer;
>- É um processo fundamental para identificar o escopo do projeto e as funcionalidades, regras e restrições que a solução final precisa ter;
>- O analista de requisitos deve adotar uma postura proativa para descobrir e entender os requisitos;
>- **Termos comuns para elicitações: captura de requisitos, descoberta de requisitos ou aquisição de requisitos;**
>- Para produtos inovadores, podem ser utilizadas técnicas de [[Brainstorming]] ou [[Design thinking]] para despertar a criatividade;
>	- Podem ser empregadas combinações de diversas técnicas para gerar soluções.
### Fontes de Informação dos Requisitos
Diferentes produtos de software exigem diferentes fontes de informação.
1. **Stakeholders:** <mark style="background: #FF5582A6;">pessoas ou organizações que influenciam direta ou indiretamente nos requisitos do sistema</mark> (usuários, operadores, clientes).
2. **Documentos:** <mark style="background: #FF5582A6;">informações importantes que podem se tornar requisitos</mark>: documentos de ordem legal ou regulatória, normas e padrões ou documentos internos da empresa ou negócio.
3. **Sistemas em Operação:** <mark style="background: #FF5582A6;">sistemas legados, predecessores ou concorrentes</mark>, podem ser fonte de informações sobre funcionalidades desejadas pelo cliente.

>[!tip] Quanto aos *stakeholders*
>- **Níveis de Envolvimento (Leffingwell):** *stakeholders* devem ser mantidos informados, devem ser consultados, serão parceiros no desenvolvimento ou controlam os resultados.
### Personas
O mapeamento de **Personas** é sugerido por Leffingwell para determinados casos:
- **Persona Primária:** alguém que interage com o software e <mark style="background: #FF5582A6;">necessita de uma interface projetada especificamente para ela</mark>.
- **Persona Secundária:** um usuário que <mark style="background: #FF5582A6;">utiliza o software com uma interface projetada para outro tipo de usuário</mark>.

>[!note] Quanto às personas
>- Mapear uma persona significa caracterizar um representante hipotético de uma classe de usuários;
>- Personas devem ser caracterizadas considerando características como: comportamentos sociais e demográficos, preferências, preocupações e informações similares.
### Técnicas de Elicitação
O analista deve **selecionar a técnica mais apropriada** ou uma combinação de várias técnicas.

| Técnica           | Objetivo Principal                                                                                                       | Quando Usar                                                                                                                 | Cuidados/Características                                                                      |
| :---------------- | :----------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------- |
| **Entrevista**    | Obtenção de informações subjetivas (sentimentos, desabafos) e fluxo de trabalho que estão apenas na memória das pessoas. | Quando há pessoas com conhecimento disponível e para captar informações subjetivas.                                         | Exige preparo, prática de **escuta ativa** (Wiegers e Beatty) , e atenção a respostas falsas. |
| **Reunião**       | Coleta de sugestões, críticas, busca de **consenso** e alternativas.                                                     | Para obter resposta rápida de várias pessoas e resolver situações de conflito.                                              | Exige preparação. Objetivo é o consenso.                                                      |
| **Brainstorming** | Encontrar soluções **inovadoras e criativas**.                                                                           | Ambiente informal e propício para o desenvolvimento de atividades criativas.                                                | Ocorre em ambiente descontraído, **sem julgamentos ou análises** na fase de ideação.          |
| **Observação**    | Examinar fatos ou fenômenos em campo. Confirmação de informações obtidas de outras fontes.                               | Quando o fluxo de papéis, o ambiente real e problemas de desempenho são relevantes.                                         | A presença do observador pode interferir nas condições reais (limitação).                     |
| **Questionário**  | Coleta de sugestões e críticas de forma mais fria e impessoal.                                                           | Não há tempo para entrevistar todos, para fins estatísticos ou quando os *stakeholders* estão distribuídos geograficamente. | Não permite a riqueza de outras técnicas.                                                     |

>[!note] Quanto às técnicas de elicitação
>- Não se trata apenas de perguntar o que os usuários e *stakeholders* desejam, é necessário extrair informações importantes, investigar, instigar, questionar, descobrir e explorar as dores dos usuários;
>- Não se trata apenas da transcrição dos problemas, e sim entender o que o usuário relata para explorar, de forma colaborativa, todos os aspectos necessários para o entendimento correto do requisito;
>- É um constante exercício de "E se..." afim de explorar diversas soluções até encontrar uma que se encaixe melhor.
## II. Análise de Requisitos
A [[02 - Análise de negócio - BABOK|Análise de Requisitos]] é a <mark style="background: #FFB86CA6;">etapa para aprofundar o entendimento acerca dos requisitos</mark>.
- **Objetivos:** buscar possíveis **conflitos**, definir a **prioridade** dos requisitos, e realizar a **decomposição** de requisitos de alto nível em níveis de detalhe apropriados.
- **Criticidade:** a complexidade de um requisito funcional pode ser incompatível com a necessidade de desempenho exigida. <mark style="background: #FFB86CA6;">Requisitos com grande impacto na arquitetura devem ser tratados com cuidado redobrado</mark>.
	- Requisitos com grande impacto na arquitetura podem implicar em consequências para todos os demais requisitos, incluindo requisitos de qualidade, como o desempenho da aplicação.
- **Atributos:** faz parte da análise a definição dos atributos associados ao requisito, como **volatilidade**, **impacto sobre a arquitetura** e **risco**.
## III. Especificação de Requisitos
A **Especificação** é a <mark style="background: #FFF3A3A6;">etapa dedicada a representar os requisitos de uma forma que eles possam ser verificados e validados</mark> posteriormente.
- **Formatos:** pode implicar em formatos diferentes que envolvem textos (linguagem natural), diagramas e tabelas.
- **Documentação em Ágil:** há um debate sobre a quantidade de documentação necessária. Agilistas mais radicais defendem que o único fiel é o código. A questão é: *quanto de especificação é necessário antes da implementação?*
	- A questão depende: 
		- da complexidade do produto que está sendo desenvolvido; 
		- da criticidade de cada requisito;
		- dos riscos de se ter um erro proveniente de uma má compreensão;
		- da experiência da equipe envolvida;
		- da fase em que o produto e a empresa se encontram
- **[[MVP (Minimum Viable Product):]]** empresas disruptivas de tecnologia frequentemente iniciam suas atividades a partir de versões iniciais e pouco elaboradas do produto.

>[!info] Sobre documentação em métodos ágeis
>- Há alguns anos que os métodos ágeis estão sendo amplamente utilizados na industria, e muitos entendem que a utilização de ágil é sinônimo para não realizar nenhum tipo de documentação;
>- "Documentação" (entre aspas) é um termo pejorativo no ambiente ágil, pois ela é tratada comum uma ação que agrega pouco ou nenhum valor ao produto final;
>- Por isso que, para os agilistas, apenas o código basta como documentação.
### Descrições e Modelos de Especificação

| Tipo de Descrição | Foco                                                                                                                              | Exemplo de Uso                                                        |
| :---------------- | :-------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------- |
| **Estática**      | Não descreve como os relacionamentos se modificam ao longo do tempo. O tempo não é o fator principal.                             | **Abstração de Dados** (Estrutura de classes).                        |
| **Dinâmica**      | Descreve como os relacionamentos modificam seu comportamento ao longo do tempo. O sistema muda de estado a partir de um estímulo. | **Diagramas de Transição/Estado** (Ex: sistema de reservas de hotel). |
### Protótipos
A **Prototipação** é a solução para validar o entendimento, a compreensão do problema ou quando o cliente não sabe expressar o que quer.
- **Tipos de Protótipos:**
	- **Descartável (Exploratório):** Não se pretende utilizá-lo como parte real do sistema.
	- **Evolutivo:** Servirá de base para o desenvolvimento real.
	- Podem ser de alta ou baixa fidelidade.
## IV. Validação de Requisitos
A Validação é <mark class="hltr-green">fundamental para garantir que existe uma compreensão correta e comum sobre os requisitos</mark> e que o produto irá satisfazer as necessidades do negócio.
- **Formas de Validação:**
	- **Revisão:** Revisão formal sobre as especificações por revisores designados.
	- **Workshops de Validação:** Envolvimento de diversos tipos de *stakeholders*.
	- **Protótipos Funcionais:** Visam confirmar os requisitos e podem apoiar a elicitação de novos requisitos.
	- **Casos de Teste:** Especificar um conjunto de casos de teste também faz parte desta etapa.
### Validação vs. Verificação (Modelo V de Teste)
- **Verificação:** Testar se o produto final **cumpre o que estava na especificação**.
- **Validação:** Testar se o produto **faz aquilo que deveria fazer** (atende ao propósito).

>[!note] Sobre validação dos requisitos
>- Precisam ser validadas entre os *stakeholders* e a equipe de desenvolvimento para **garantir que existe uma compreensão correta e comum sobre os requisitos** e que a equipe de desenvolvimento possui condições de implementar um produto que irá satisfazer as necessidades do negócio;
>- A **validação pode ser realizada por meio de revisões sobre as especificações**, feito por revisores designados, ou em **workshops de validação**, onde diversos tipos de *stakeholders* são envolvidos.
>- **Podem ser usados protótipos funcionais para a confirmação do requisito** e até para apoiar a elicitação de novos requisitos.
## 2. Gerenciamento de Requisitos
O **Gerenciamento de Requisitos é o enfoque sistemático para a elicitação, organização e documentação dos requisitos**, mantendo o acordo entre usuários e a equipe de projeto à medida que os requisitos se modificam.

>[!info] Natureza Volátil dos Requisitos
>Requisitos são voláteis. Fatores que contribuem para sua instabilidade:
>- Mudanças de legislação.
>- Erros incorridos no processo de requisitos.
>- Novas necessidades do cliente.

- **Objetivo:** Conduzir as alterações de forma ordenada e garantir que o impacto das mudanças seja avaliado e compreendido.
- **Base para Análise de Impacto:** É crucial manter a [[Rastreabilidade]] entre a fonte do requisito, as relações entre os requisitos, e os artefatos seguintes (como o código).
- **Fases:** Gerenciamento de Mudanças, Gerenciamento de Configuração, Gerência da Qualidade de Requisitos e Rastreabilidade.
## 3. Métodos Ágeis e Histórias de Usuário
Os métodos ágeis trouxeram uma forma diferente de organizar os requisitos, utilizando as **Histórias de Usuário**.
### Metodologia vs. Framework (Scrum)
- **Metodologia:** Conjunto estruturado e, normalmente, **mais rígido** de princípios, processos e práticas que define **passo a passo como fazer algo**.
- **Framework:** Estrutura **flexível** que fornece diretrizes e ferramentas, mas **sem um processo rígido**.
- **Conclusão:** <mark class="hltr-blue">Toda metodologia pode estar dentro de um framework, mas nem todo framework é uma metodologia</mark>.
### Scrum
O **[[Scrum]]** é o *framework* mais utilizado no mundo ágil , sendo iterativo e incremental.
- **Sprint:** O princípio básico é que o desenvolvimento é dividido em entregas menores (geralmente **2 a 4 semanas**) chamadas *sprints*.
- **Artefatos Chave:**
	- **[[Backlog do Produto]] (Product Backlog):** <mark class="hltr-purple">Repositório de todas as requisições dos clientes</mark> (requisitos funcionais e não funcionais), <mark class="hltr-purple">priorizado pelo Product Owner (PO)</mark>.
	- **Backlog da Sprint:** Contém os <mark class="hltr-purple">itens do Backlog do Produto que foram acordados e o plano para o seu desenvolvimento</mark>.
	- **Incremento:** O item potencialmente entregável gerado ao final de uma *sprint*.
### História de Usuário (User Story)
É a **forma pela qual os requisitos são geralmente expressos em equipes ágeis**.
- **Conceito:** É um cenário de uso de um produto, narrado pelo ponto de vista do usuário.
- **Os 3 C's (Criado por Roy Jeffrey):**
	1. **Cartão (*Card*):** Afirmação escrita na voz do usuário.
		- **Formato:** Como um (**papel - representa QUEM**), eu quero (**ação / atividade - O QUÊ**), para que eu possa (**resultado/valor - POR QUÊ**).
	2. **Conversa (*Conversation*):** O objetivo é ser o ponto de partida da conversa entre o negócio e a equipe.
	3. **Confirmação (Critérios de Aceitação):** Critérios complementares que ajudam a esclarecer como a história será validada (Testes de Aceitação).
#### Critérios INVEST para Histórias de Usuário
Toda história deve ser:
- **Independente (*Independent*):** Deve ser identificada, discutida, implementada e liberada de forma independente de outras histórias.
- **Negociável (*Negotiable*):** Não é um contrato imutável, podendo ser adaptada.
- **Valiosa (*Valuable*):** Deve agregar valor para alguém e ser liberada em intervalos curtos.
- **Estimável (*Estimable*):** Deve ser possível estabelecer uma estimativa de complexidade para verificar se cabe na *sprint* ou precisa ser dividida.
- **Pequena (*Small*):** Deve ser pequena o suficiente para caber em uma única *sprint*. Histórias grandes são chamadas de **Épicos** e devem ser particionadas.
- **Testável (*Testable*):** Deve-se conhecer seus critérios de avaliação para que possa ser implementada. Uma história só está pronta se for testável.
---