---
tags:
  - EngRequisitos
  - Concluido
---
# Análise e Especificação de Requisitos: Modelagem UML e Abordagens Ágeis (SCRUM)

## 1. Abordagens Ágeis: O Framework SCRUM
- O [[0x - Scrum|SCRUM]] é um **framework leve** que ajuda a gerar valor por meio de soluções adaptativas para problemas complexos. É iterativo e incremental, baseado no empirismo e *lean thinking*.
### Pilares e Valores do Scrum
O Scrum se apoia em três pilares e cinco valores.

| Pilares           | Definição                                                |
| :---------------- | :------------------------------------------------------- |
| **Transparência** | Clareza sobre processos, requisitos de entrega e status. |
| **Inspeção**      | Constante avaliação de tudo o que está sendo feito.      |
| **Adaptação**     | Ajuste do processo e do produto às mudanças.             |
- Valores do SCRUM: Comprometimento, Coragem, Foco, Respeito e Abertura.
### Papéis, Eventos e Artefatos
![[Scrum.png|center|500]]
- Papéis (Time Scrum):
	- Product Owner (PO);
	- Scrum Master;
	- Desenvolvedores;
- Eventos (sprint):
	- Planejamento da Sprint;
	- Reunião diária (daily);
	- Revisão da Sprint;
	- Retrospectiva da Sprint;
- Artefatos:
	- Backlog do produto;
	- Backlog da Sprint;
	- Incremento;

| Papéis (Time Scrum)                                            | Eventos (Cerimônias)                                        | Artefatos (Requisitos)                                         |
| :------------------------------------------------------------- | :---------------------------------------------------------- | :------------------------------------------------------------- |
| **Product Owner (PO)**                                         | **Sprint** (2 a 4 semanas, duração constante) .             | **Backlog do Produto** (repositório de todos os requisitos) .  |
| **Scrum Master (SM)**                                          | **Planejamento da Sprint** (Max. 8h para Sprint de 4 sem.). | **Backlog da Sprint** (itens selecionados para o Incremento) . |
| **Desenvolvedores** (Time auto-gerenciado, multidisciplinar) . | **Reunião Diária** (Daily Scrum - 15 min.).                 | **Incremento** (item "Pronto" e potencialmente entregável) .   |

>[!tip] Foco dos Artefatos
> - **Backlog do Produto:** Contém todos os requisitos (funcionais e não funcionais). É priorizado pelo PO e está em constante evolução.
> - **Backlog da Sprint:** O escopo **não deve ser alterado** durante a Sprint.
> - **Incremento:** Nasce quando um item atende à **Definição de Pronto (DoD)**.
 
## 2. Especificação Ágil: Histórias de Usuário
As Histórias de Usuário (*"User Stories"*) são a forma padrão de expressar requisitos em ambientes ágeis.
- **Conceito:** Representa uma funcionalidade ou característica do produto "narrada" pelo ponto de vista do usuário.
![[PriorizacaoHistoriaUsuario.png|center|450]]
### Componentes de uma História de Usuário (3 C's)
1. **Cartão (*"Card"*):** A afirmação concisa que segue a "voz do usuário".
	- **Formato:** Como um **{ator}**, eu quero/preciso **{ação}** para **{funcionalidade / valor}**.
2. **Conversação (*"Conversation"*):** A discussão verbal e colaborativa que ocorre durante o projeto, complementada por documentação.
3. **Confirmação (*"Confirmation"*):** Os **testes de aceitação** que serão usados para demonstrar que a história foi implementada corretamente.
### Critérios de Qualidade INVEST (Bill Wake)
Um acrônimo para lembrar as características de uma boa história:
- **I**ndependent: Não deve haver dependência entre as histórias e as histórias não devem se sobrepor.
- **N**egotiable: A essência é capturada, não os detalhes, permitindo flexibilidade.
- **V**aluable: Deve ter valor para o cliente.
- **E**stimable: Deve ser possível estimar o esforço.
- **S**mall: Boas histórias são pequenas, representando, no máximo, algumas semanas de trabalho.
- **T**estable: Boas histórias são testáveis, o que ajuda a clareza.
### Priorização de Itens (MoSCoW e Matriz)
O **Product Owner (PO)** prioriza o backlog. A prioridade de um item diminui conforme ele desce na lista (Baixa prioridade $\rightarrow$ Alto Nível).

1. **Matriz Benefício x Esforço/Custo:**
![[MatrizPriorizacaoBacklog.png|center|450]]

2. **Técnica MoSCoW:** Must have, Should have, Could have, Will not have.![[PriorizacaoMoSCoW.png|center|450]]
## 3. Técnicas Ágeis de Descoberta
Para descobrir e detalhar as funcionalidades do produto, são utilizadas técnicas focadas na perspectiva e experiência do usuário:
### Personas e Jornada do Usuário
- **Persona (Análise):** Uma ideia fictícia do cliente ideal, criada com base em dados reais, que representa um segmento de usuário da solução.
- **Componentes:** Apelido/Nome, Perfil, Comportamentos e Necessidades/Dores.
- **Jornada do Usuário (Customer Journey):** Descreve o percurso de um usuário por uma sequência de passos dados para alcançar um objetivo.
- **Elementos:** Ações realizadas, Emoções/Pensamentos, Dores/Ganhos e Pontos de Contato com o sistema (Canais).
### Mapa de Empatia
Representação visual que aprofunda o conhecimento sobre o usuário, organizando-o a partir de seis perguntas-chave:
- O que ele **PENSA E SENTE** (preocupações e aspirações).
- O que ele **VÊ** (ambiente, amigos, mercado).
- O que ele **ESCURA** (amigos, chefe, influenciadores).
- O que ele **FALA E FAZ** (atitude em público, comportamento).
- **FRAQUEZAS** (medos, frustrações).
- **GANHOS** (desejos e necessidades).
## 4. Especificação com Modelagem UML
A **UML (Unified Modeling Language)** é uma linguagem gráfica de modelagem utilizada para: visualizar, especificar, construir e documentar artefatos de sistemas complexos.
- **Princípio:** Um modelo é uma simplificação (representação) da realidade, usado para compreender melhor o sistema.
- Leia mais sobre: [[05 - Diagrama de Classes UML|Diagrama de classes UML]], [[04 - Diagrama de caso de uso|Diagramas de caso de uso]] e [[UML (Unified Modeling Language)]]
---