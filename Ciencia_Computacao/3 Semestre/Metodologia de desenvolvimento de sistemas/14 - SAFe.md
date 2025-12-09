---
tags:
  - MDS
  - Naoconcluido
  - NaoRevisado
---
# Scaled Agile Framework (SAFe)

>[!info] Conceito de SAFe
> - **SAFe (Scaled Agile Framework)** é um framework líder no mercado para alcançar a **Agilidade Organizacional** (Business Agility).
> - É uma base de conhecimento que integra princípios, práticas e competências do **Lean**, **Agilidade** e **DevOps** para ajudar as organizações a entregar valor em larga escala.
> - É configurável e escalável, possuindo 4 níveis prontos (Essential, Large Solution, Portfolio, Full).
## 1. Business Agility (Agilidade Organizacional)
- É a capacidade de uma organização de competir e prosperar na era digital, respondendo rapidamente às mudanças do mercado e às oportunidades emergentes com soluções de negócios inovadoras.
- O desenvolvimento tradicional levava 18-24 meses para entregar (e podia ser tarde demais), enquanto a abordagem com Agilidade Organizacional busca uma resposta rápida, entregando um **MVP** (Minimum Viable Product) em 2-6 meses.
### Princípios da Business Agility
- **Cliente como Foco**: O cliente está no centro da estratégia, é preciso ouvi-lo e adaptar-se às suas exigências.
- **Fluxo Ágil**: Projetar ou modificar fluxos de trabalho, identificar desperdícios e etapas essenciais para gerar valor. Inclui um processo de melhoria contínua.
- **Vontade de Inovar**: Criatividade como ativo de negócio, capacitação e autonomia como valores organizacionais.
- **Baseado em Dados**: Tomada de decisão fundamentada em provas e fatos, não apenas instinto, para obter resultados mais precisos.
## 2. Configurações do SAFe (4 Níveis)
O SAFe se adapta ao tamanho e complexidade da organização, estruturado em quatro níveis principais (do mais simples ao mais completo):
	1. **SAFe Essential**: Contém o bloco básico (Agile Release Train - ART) necessário para iniciar a entrega de soluções.
	2. **SAFe Large Solution**: Estende o Essential para a construção de grandes soluções que requerem a coordenação de múltiplos ARTs e fornecedores (**Solution Train**).
	3. **SAFe Portfolio**: Adiciona a gestão de portfólio (Estratégia e Financiamento de Investimento, Governança Lean) para alinhar a TI à estratégia do negócio.
	4. **SAFe Full**: Combina todos os níveis anteriores, sendo a configuração mais abrangente.

### Valores Essenciais do SAFe
- **Alinhamento**: Comunicar visão, missão e estratégia, conectando-as à execução. Verificar constantemente a compreensão do cliente e do plano.
- **Melhoria Implacável**: Criar senso de urgência, cultura de resolução de problemas, guiar melhorias por fatos e dar tempo para inovação.
- **Transparência**: Criar um ambiente baseado em segurança, transformar erros em aprendizado, visualizar o trabalho e fornecer acesso imediato às informações.
- **Respeito pelas Pessoas**: Valorizar a diversidade de opiniões, desenvolver o pessoal (mentoria) e formar parcerias de longo prazo.

### Princípios do SAFe (Base Lean-Agile)
1. Adote uma **visão econômica**.
2. Aplique o **pensamento sistêmico**.
3. Presuma variabilidade; preserve opções.
4. Crie incrementalmente com ciclos de aprendizado rápidos e integrados.
5. Baseie marcos na avaliação objetiva de sistemas em funcionamento.
6. Deixe o fluxo fluir sem interrupções.
7. Aplique cadência, sincronize com o planejamento entre domínios.
8. Desbloqueie a motivação intrínseca dos trabalhadores do conhecimento.
9. Descentralize a tomada de decisões.
10. Organize em torno do valor.

## 3. Estrutura dos Times no SAFe

### Times Ágeis Multifuncionais
- Entidades **auto-organizadas** otimizadas para comunicação e entrega de valor.
- Possuem 10 ou menos membros.
- **Papéis especializados**:
	- **Scrum Master/Team Coach**: Facilita o PI Planning, apoia a execução da iteração, cria times de alto desempenho e melhora o fluxo.
	- **Product Owner**: Gerencia e prioriza o **Backlog do Time**, conecta-se com o cliente e contribui com a visão e Roadmap.

### Agile Release Train (ART)
- Organização **virtual** que coordena de **5 a 12 times** (50 a 125+ pessoas).
- Sincronizados em uma cadência comum: o **PI Planning Interval** (geralmente 3 meses).
- Alinhados a uma missão comum por um único **Backlog do ART**.
- **Papéis Principais no ART**:
	- **RTE (Release Train Engineer)**: É o **coach do ART**.
	- **PM (Product Management)**: Proprietário do Backlog do ART (define e prioriza).
	- **BO (Business Owner)**: Stakeholders principais que conhecem o mercado e controlam o valor do negócio.
	- **SA (System Architect)**: Fornece orientação sobre arquitetura e capacitação técnica.
	- **SysTeam (System Team)**: Fornece processos e ferramentas para integrar e avaliar os ativos (Continuous Delivery Pipeline).
## 4. Eventos SAFe (Eventos do ART)
Os eventos do ART e dos times mantêm o trem nos trilhos:
### PI Planning (Planning Interval Planning)
- **Evento mais importante do ART**, com duração de 2 dias.
- Todos os times se reúnem para **planejar**, **alinhar** e se **comprometer** com os objetivos estratégicos do próximo **PI** (3 meses).
- **Inputs Principais**: Prioridades do negócio e Visão do Produto.
- **Outputs Principais**: Objetivos do PI do ART e Objetivos dos Times.
- **Benefícios**: Alinha todos em uma visão, resolve dependências e cria um plano realista.
- **Quadro de Planejamento do ART**: Visualiza o fluxo de valor e as dependências (fios vermelhos).
- **Riscos ROAM**: Riscos levantados são classificados como **R**esolvido, **O**wned (Assumido), **A**ccepted (Aceito) ou **M**itigated (Mitigado).
- **Voto de Confiança**: Votação ao final para expressar a crença na entrega do plano.
### ART Sync
- Evento contínuo para coordenar o progresso dentro do PI.
- Divide-se em:
	- **PO Sync**: Verifica status das features, trata priorização e coordena a integração funcional (Participantes: POs, PMs, Architect, RTE).
	- **Coach Sync**: Acompanha o progresso dos times, remove impedimentos intertimes, trata qualidade/agilidade/fluxo (Participantes: SMs, RTE, Agile Coach).
### System Demos
- Demonstração do **sistema integrado e funcionando** ao final de cada iteração (2 semanas).
- Demonstra o resultado das entregas da iteração, com suporte do SysTeam para a integração.
- Participantes: PMs e POs, Business Owners (BOs), clientes, etc..
### Inspect and Adapt (I&A)
- Ocorre no final do PI, com duração de 3 a 4 horas.
- Envolve os times e stakeholders.
- Composto por 3 partes:
	1. **System Demo do PI**: Demonstração final do incremento completo.
	2. **Medições**: Avaliação da entrega (valor de negócio alcançado para cada objetivo do PI) e da **Previsibilidade do ART** (ex: Program Predictability Measure).
	3. **Workshop de Resolução de Problemas**: Usa técnicas como a **Análise de Causa Raiz** (Diagrama de Ishikawa) e o **5 Porquês** para identificar a principal causa dos problemas (ex: falha na previsibilidade) e criar itens de backlog de melhoria.

---