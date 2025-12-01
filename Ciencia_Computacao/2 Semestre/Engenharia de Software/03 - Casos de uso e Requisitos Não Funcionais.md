# Engenharia de Requisitos: Casos de Uso e Requisitos Não Funcionais

## Requisitos - Propósito e Definição
### Propósito dos Requisitos
- Obter **acordo com cliente e usuários** sobre o que o sistema deve fazer.
- Dar aos desenvolvedores um melhor entendimento dos requisitos do sistema.
- Definir a **funcionalidade** do sistema.
- Prover base para:
    - Planejamento do conteúdo técnico e iterações.
    - Estimar custo e tempo de desenvolvimento.
    - Definir a interface do sistema.
### Considerações Importantes
- O sistema deve prover **valor** ao cliente e usuários.
- Os requisitos precisam ser definidos na **direção correta**.
- Os clientes precisam entender o resultado da captura de requisitos.
- Requisitos podem ser descritos de várias maneiras:
    - **Necessidades dos usuários**.
    - **Requisitos não funcionais**.
    - **Solicitações de mudanças**.
    - **Casos de uso**.
### Requisitos do Projeto
Os requisitos do projeto devem incluir:
- Requisitos Técnicos.
- **Requisitos Funcionais**.
- **Requisitos Não Funcionais**.
- Requisitos Não Técnicos.
---
## Requisitos Funcionais usando Casos de Uso
>[!quote] Conceito Chave: Caso de Uso
> - É uma forma específica de uso do sistema composta por uma sequência de ações que produz um **resultado de valor para algum agente externo**.
> - Mostram apenas **o que o sistema faz**, não como.
> - Capturam o comportamento pretendido para um sistema sem especificar como será implementado.
### Utilidade dos Casos de Uso
Casos de uso servem como guia para:
- Criação e validação da arquitetura do sistema.
- Definição de casos e procedimentos de **testes**.
- Planejamento das iterações, elaboração de cronograma e organização do time.
- Criação da documentação do usuário.
### Conceito Chave: Ator
- É **qualquer coisa que possui interface com o sistema** a ser desenvolvido.
- Definem um **papel particular**.
- São sempre **externos** ao sistema.
- Uma mesma pessoa pode desempenhar diferentes papéis (Ex: Joana como professora e Joana como diretora).
### Diagrama de Casos de Uso
- Diagrama com casos de uso do sistema e atores relacionados.
- Facilitam o entendimento do sistema mostrando a sua **"visão externa"**.
- A coleção de casos de uso deve especificar todas as formas existentes de uso do sistema.
#### Conceitos Relacionados
- **Cenários**: Em UML, significa um **caminho através de um caso de uso**. Cada caso de uso contém uma coleção de cenários (sucesso e falha).
- **Pacotes**: Servem para **agrupar casos de uso relacionados**. Critérios de agrupamento podem ser: Ator, funcionalidades correlatas, ou processos.
### Como Encontrar [[04 - Diagrama de caso de uso| Atores e casos de Uso]]
#### Encontrando Atores
Perguntas a fazer:
- Quem usa o sistema?
- Quem instala/mantém/inicia/desliga o sistema?
- Que outros sistemas usam o sistema?
- Quem recebe ou provê informação ao sistema?
#### Encontrando Casos de Uso
- Atores são fundamentais para a descoberta dos casos de uso.
- Perguntas a fazer:
    - Que funções o ator vai querer do sistema?
    - Que informações atores irão criar, ler, atualizar ou apagar?
    - O sistema precisa notificar o ator sobre mudanças no seu estado interno?
    - Existe algum evento externo que o sistema precisa saber? Que ator informa o sistema desses eventos?
#### Técnicas de Levantamento
- **Use-Case Workshop**: Requer a presença de um facilitador e pessoas com diferentes perfis. Deve-se aceitar todo tipo de sugestão (filtrar depois) e evitar pensar em detalhes.
- **Foco**: Os casos de uso levantados devem estar claros para todos, principalmente o **valor que cada um agrega ao usuário**.
- Outras Técnicas: Reuniões e conversas com usuários.
---
## Requisitos Não Funcionais (R.N.F.)
São **atributos ou qualidades do sistema**.
### Tipos de Requisitos Não Funcionais
| Tipo de R.N.F.                        | Relacionado Com:                                                                                         | Exemplos                                                                                       |
| :------------------------------------ | :------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------- |
| **Facilidade de uso (Usabilidade)**   | Interface com o usuário, material de treinamento e documentação.                                         | Help, Instalação automática.                                                                   |
| **Confiabilidade**                    | Frequência e severidade de falhas, habilidade de recuperação, corretude do sistema.                      | Disponibilidade $24/7$, prazo de tolerância máxima para volta do sistema.                      |
| **Desempenho (Performance)**          | Eficiência, tempo de resposta, uso de recursos.                                                          | -                                                                                              |
| **Segurança**                         | Privacidade, integridade, autenticidade dos dados do sistema.                                            | -                                                                                              |
| **Distribuição**                      | Distribuição da versão executável do sistema.                                                            | Crítico para sistemas com grande volume de usuários.                                           |
| **Adequação a padrões**               | Padrões ou normas que devem ser seguidos no sistema ou desenvolvimento (interface gráfica, arquitetura). | Deve-se referenciar o documento que define o padrão adotado.                                   |
| **Restrições de Hardware e Software** | Hardware e software utilizados para desenvolvimento do sistema.                                          | Plataforma cliente (Windows, Web), Servidor (Linux), Banco de Dados, Protocolo de comunicação. |
### RNF e Mensurabilidade (Critérios de Aceitação)
- Devem ser **testáveis** e, para isso, devem ser **mensuráveis**.
- É preciso especificar qual o seu **critério de aceitação**.
- Precisam estar definidos com **números e nomes** (evitando termos vagos como "rápido" ou "madura").
- **Exemplo de Redefinição (Mensurável):** "O sistema deve responder em menos de **10 segundos**".
### RNF X Casos de Uso
- Podem estar **associados a um caso de uso específico** ou **associados a todo o sistema**.
- Para serem atendidos, podem **gerar novos casos de uso**.
- **Exemplo:** O RNF de "tempo de resposta" para o caso de uso "Sacar dinheiro" não pode ser maior que 1 minuto.
---
## Critérios de Aceitação
- Devem ser definidos para **validar se os produtos de software satisfazem os requisitos** do projeto.
- O cliente deve se **comprometer** com estes critérios.
- São relativos a produtos desenvolvidos ou aspectos da execução do projeto.
- **Exemplo:** 100% da documentação segue padrão definido; Testes realizados com sucesso segundo critérios de conclusão de testes.
---