---
tags:
  - MDS
  - Naoconcluido
  - NaoRevisado
---
# Extreme Programming (XP)

>[!info] Conceito de XP
> - O **Extreme Programming (XP)** é um processo de desenvolvimento que busca assegurar que o **cliente** receba o máximo de valor de cada dia de trabalho da equipe de desenvolvimento.
> - É organizado em torno de um conjunto de **valores e práticas** que atuam de forma harmônica e coesa.
> - Consiste na aplicação das **boas práticas de desenvolvimento de software levadas ao extremo**.
> - É uma **metodologia ágil** focada em **código** para equipes pequenas a médias que trabalham com requisitos vagos ou que mudam frequentemente.
> - Baseia-se em disciplina rigorosa e processos formais de desenvolvimento.

## Histórico
- O trabalho inicial sobre as ideias e métodos associados ao **XP** surge no final da década de **1980**.
- Autores-chave na formalização:
	- **Kent Beck** (1999)
	- **Jeffries** (2001), detalhando aspectos técnicos
	- **Beck e Fowler**, sobre o planejamento XP
## Valores Fundamentais do XP
- Os valores agem em harmonia para garantir um alto retorno do investimento em software para o cliente.
### Comunicação
- Não é limitada por procedimentos formais.
- Preferência à comunicação mais **ágil**.
### Simplicidade
- Incentiva práticas que reduzem a complexidade do sistema (Princípio: **Keep It Simple**).
- A solução adotada deve ser sempre a mais **simples** que alcance os objetivos esperados.
- É importante usar as tecnologias, design e técnicas mais simples que atendam aos requisitos do usuário.
- **"Prever o futuro"** é anti-XP e impossível, pois os requisitos mudam.
### Feedback
- Várias práticas garantem um **rápido feedback** sobre diversas etapas do processo.
- **Feedback sobre qualidade do código**:
	- Testes de Unidade
	- Programação em Pares
	- Posse Coletiva
	- **Feedback sobre estado de desenvolvimento**:
	- Histórias do usuário
	- **Integração Contínua**
	- Jogo do Planejamento
### Coragem
- É essencial para:
	- Melhorar o design de código que está funcionando para torná-lo mais simples (**Refatoramento**).
	- Jogar fora código desnecessário.
	- Investir tempo no desenvolvimento de testes.
	- Mexer no design em estágio avançado do projeto.
	- Pedir ajuda aos que sabem mais.
	- Abandonar processos formais, fazendo design e documentação em forma de código.
### Respeito
- Saber ouvir, compreender e respeitar o ponto de vista do outro é fundamental.
- Envolve o respeito à **posse coletiva do código**, primando pela qualidade e design simples.
- Garante uma relação transparente e duradoura.
## Práticas Essenciais do XP
### 1. Equipe (Equipe e Cliente)
- Todos no projeto são parte de uma equipe, incluindo um representante do cliente (o **cliente no local**).
- O representante do cliente: estabelece requisitos, define prioridades e controla o rumo do projeto.
- Outros papéis: Programadores, Testadores, Analistas, Gerente, Coach, Tracker.
### 2. Jogo do Planejamento (Planning Game)
- Define prioridades e estimativa de prazo para cada tarefa.
- **Planejamento da Release**: Cliente propõe funcionalidades (histórias) e Programadores avaliam a dificuldade.
- **Planejamento da Iteração**: Cliente define funcionalidades prioritárias; Programadores as quebram em tarefas e avaliam o custo (tempo).
- Permite ao cliente dirigir o projeto com clareza sobre o avanço, o que reduz riscos e aumenta a chance de sucesso.
### 3. Testes de Aceitação
- Elaborados pelo **cliente**.
- São **testes automáticos** que, quando executados com sucesso, indicam que a funcionalidade foi implementada.
- Devem ser rodados novamente em cada iteração futura.
- Oferecem feedback em tempo real sobre o percentual de implementação do sistema.
### 4. Pequenos Lançamentos (Small Releases)
- A cada iteração, disponibiliza-se software **100% funcional**.
- Isso gera menor risco, permite que o cliente meça o que foi feito e garante que problemas sejam detectados cedo.
- Lançamentos frequentes são viabilizados por Design Simples e Integração Contínua.
### 5. Design Simples (Simple Design)
- O projeto começa e se mantém simples através de testes e **refatoramento**.
- Não se implementa nenhuma função adicional que não será usada na atual iteração.
- A implementação ideal deve: rodar todos os testes, expressar todas as ideias necessárias, não ter código duplicado e ter o mínimo de classes e métodos.
### 6. Programação em Duplas (Pair Programming)
- O desenvolvimento é feito em pares: um computador, um teclado, dois programadores (**piloto** e **co-piloto**).
- Papéis e pares são alternados frequentemente.
- **Benefícios**: Melhor qualidade do design/código/testes, revisão constante do código, nivelamento da equipe e maior comunicação.
- Pesquisas indicam que duplas produzem código de melhor qualidade em aproximadamente o mesmo tempo que programadores solo.
### 7. Desenvolvimento Orientado por Testes (Test-Driven Development - TDD)
- O desenvolvimento deve ser guiado por testes: **"Test first, then code"**.
- Programadores XP escrevem testes primeiro, depois o código, e rodam os testes para validar.
- O código só tem valor se seu teste funcionar 100%.
- Todos os testes são executados automaticamente e o tempo todo.
- Oferece maior **segurança e coragem** para mudar o código.
### 8. Refinamento do Design (Refactoring)
- O design é melhorado continuamente através de **refatoramento**.
- É a mudança proposital de código que está funcionando para melhorar o design, simplificar, remover duplicidade, aumentar a coesão e reduzir o acoplamento.
- É realizado o tempo todo, sendo um processo formal de etapas reversíveis.
- A existência prévia de testes é essencial para a segurança do refatoramento.
### 9. Integração Contínua (Continuous Integration - CI)
- O sistema é mantido integrado o tempo todo.
- A integração de todo o sistema pode ocorrer **várias vezes ao dia**.
- Todos os testes devem ser executados após cada integração.
- **Benefícios**: Reduz o tempo gasto na integração, viabiliza lançamentos pequenos e frequentes, estimula design simples, e permite encontrar problemas rapidamente.
### 10. Posse Coletiva (Collective Ownership)
- Qualquer dupla de programadores pode melhorar qualquer parte do sistema a qualquer momento.
- Todo o código pertence à **equipe**.
- Promove maior qualidade (menos duplicação) e reduz a dependência de indivíduos.
- A programação em pares ajuda a reduzir o risco de danos.
### 11. Padrões de Codificação (Coding Standards)
- O código segue um padrão de codificação definido pela equipe (nomes de classes, variáveis, métodos, organização do código).
- O objetivo é que o código pareça ter sido escrito por um único indivíduo competente.
- Facilita e estimula a Posse Coletiva, a Comunicação, a Simplicidade e a Programação em Pares.
### 12. Metáfora (Metaphor)
- A equipe mantém uma **visão compartilhada** do funcionamento do sistema.
- É uma analogia (ex: "o sistema funciona como uma agência de correios") que facilita a comunicação entre os membros da equipe e o cliente.
- Serve de base para a escolha de nomes de métodos, classes e para o estabelecimento de padrões de codificação.
### 13. Ritmo Saudável (Sustainable Pace)
- Projetos XP não têm cronogramas apertados que esgotam os programadores ("Semanas de 80 horas").
- A baixa produtividade resultante de ritmos insustentáveis leva a código ruim, relaxamento da disciplina e dificulta a comunicação.
- O projeto deve ter um **ritmo sustentável** por prazos longos.
## Dificuldades e Críticas
### Dificuldades
- **Vencer barreiras culturais**:
	- Deixar alguém mexer no seu código (Posse Coletiva).
	- Trabalhar em pares.
	- Ter coragem de admitir que não sabe ou pedir ajuda.
	- **Vencer hábitos antigos**:
	- Manter as coisas simples (não tentar prever o futuro com "design flexível").
	- Jogar fora código desnecessário.
	- Escrever testes antes de codificar (TDD).
	- Refatorar com frequência.
### Críticas
- Volatilidade de Requisitos.
- Necessidades conflitantes de clientes.
- Requisitos levantados de forma informal.
- Falta de projeto formal.
## Quando NÃO Usar XP
- **Equipes grandes e espalhadas geograficamente**: Dificuldade em garantir o nível de comunicação e coesão requeridos.
- **Situações sem controle sobre o código**: Exemplo: código legado que não pode ser modificado.
- **Situações onde o feedback é demorado**: Exemplo: processo de compilação-link-build-teste que leva 24 horas, ou testes muito difíceis e demorados.
- **Alta rotatividade de funcionários**.
- **Necessidade de certificação de qualidade** (devido à falta de documentação e processo bem definido).

>[!note] Conclusão
> - Para implementar XP, não é preciso usar diagramas ou processos formais.
> - É necessário que a equipe se una em torno de práticas simples, obtenha feedback suficiente e ajuste as práticas à sua situação.
> - XP é mais adequado a **equipes pequenas ou médias**.

---