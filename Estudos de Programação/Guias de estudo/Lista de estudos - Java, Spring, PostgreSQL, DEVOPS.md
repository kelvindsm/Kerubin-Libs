# Roadmap: Engenharia de Software Corporativa (Java + DevSecOps)

## Fase 1: Domínio do Java Moderno (O Alicerce)

Antes de usar o framework, a linguagem precisa ser uma segunda natureza. Estude com base no **Java 17 ou 21** (versões de Suporte de Longo Prazo - LTS).
- **Orientação a Objetos Avançada:** Interfaces, classes abstratas, polimorfismo e o princípio de composição sobre herança.
- **Tratamento de Exceções:** Como criar suas próprias exceções (`Custom Exceptions`) e a diferença entre _Checked_ e _Unchecked exceptions_.
- **Java Collections Framework:** Entender profundamente quando usar `List`, `Set` (e as diferenças entre `HashSet` e `TreeSet`) e `Map` (`HashMap`).
- **Programação Funcional no Java:** Expressões Lambda, API de _Streams_ (map, filter, reduce, collect) e a classe `Optional` para evitar os temidos `NullPointerException`.
- **Concorrência Básica:** Como threads funcionam, o pacote `java.util.concurrent` e o conceito básico de concorrência.
## Fase 2: Banco de Dados e Persistência Profissional
Como você já sabe SQL básico, o foco aqui é em arquitetura e integração segura.
- **PostgreSQL Avançado:** Índices (como acelerar buscas), normalização de dados e _Constraints_ (chaves estrangeiras, restrições de unicidade).
- **Transações (ACID):** Entender o que é _commit_ e _rollback_. Essencial para garantir que, em uma transferência de fundos, o dinheiro não suma se o sistema cair no meio da operação.
- **Spring Data JPA:** Mapeamento objeto-relacional (`@Entity`, `@Table`, `@Column`), criação de repositórios (`JpaRepository`) e métodos de busca automatizados (`findByNome`).
- **Migrações de Banco de Dados:** Nunca crie tabelas manualmente na mão. Estude **Flyway** ou **Liquibase** para versionar o seu banco de dados junto com o código Java.
### Fase 2.1: Transição para PostgreSQL e Persistência Profissional
#### 1. O Choque de Realidade: MySQL vs. PostgreSQL
O MySQL é conhecido por ser rápido e flexível (às vezes até perdoando erros de tipagem). O PostgreSQL é estritamente aderente ao padrão SQL e não perdoa dados mal formatados.
- **Tipagem Rigorosa:** Entenda que o Postgres não fará conversões implícitas "silenciosas" (como aceitar uma string vazia em uma coluna de data).
- **Controle de Concorrência (MVCC):** Estude como o Postgres permite que milhares de usuários leiam e escrevam ao mesmo tempo sem bloquear as tabelas (Multi-Version Concurrency Control).
- **Sequences:** Diferente do `AUTO_INCREMENT` simples do MySQL, o Postgres gerencia chaves primárias numéricas através de objetos chamados _Sequences_. É importante entender como elas funcionam nos bastidores.
#### 2. Tipos de Dados Avançados (Superpoderes do Postgres)
O Postgres brilha quando sai do padrão tradicional de colunas e linhas. Aprenda a usar e mapear no Java:
- **UUID Nativo:** Em sistemas distribuídos modernos, chaves primárias sequenciais (`1, 2, 3...`) são um risco de segurança. Estude como usar o tipo genérico `UUID` nativo do Postgres.
- **JSONB:** O Postgres permite salvar documentos JSON inteiros em uma única coluna, indexá-los e fazer buscas SQL _dentro_ das chaves do JSON. É como ter um banco NoSQL (como o MongoDB) dentro do seu banco relacional.
#### 3. Transações e Consistência (ACID no Spring)
Aqui entra a garantia de que as operações de negócio não quebrem no meio do caminho.
- **A anotação `@Transactional`:** Como usá-la nas classes de `Service` do Spring Boot para garantir que, se um erro ocorrer na linha 10 do seu código, tudo o que foi gravado no banco nas linhas anteriores seja desfeito (_rollback_).
- **Níveis de Isolamento:** Estude fenômenos como _Dirty Reads_ e _Phantom Reads_, e como configurar o banco para evitar que uma transação leia dados que outra transação ainda não terminou de gravar.
#### 4. Spring Data JPA e os Perigos do ORM
Você não escreverá SQL puro na maior parte do tempo, mas precisa saber o que o framework está fazendo.
- **Mapeamento Básico:** Entidades (`@Entity`), relacionamentos (`@OneToMany`, `@ManyToOne`) e carregamento de dados (`FetchType.LAZY` vs `EAGER`).
- **O Problema do N+1 Queries:** Este é o erro de performance mais comum em Java. Estude como o JPA pode gerar 50 consultas no banco quando apenas 1 resolveria, e como consertar isso usando `JOIN FETCH` em métodos personalizados.
#### 5. Versionamento de Banco de Dados (Migrações)
Em produção, a configuração `spring.jpa.hibernate.ddl-auto=update` é estritamente proibida, pois o sistema não pode adivinhar como alterar tabelas em um banco de dados com milhões de registros.
- **Flyway ou Liquibase:** Escolha uma dessas ferramentas. Você aprenderá a escrever pequenos arquivos de script (ex: `V1__criar_tabela_clientes.sql`) que rodam automaticamente quando a aplicação inicia, garantindo que o banco de dados da sua máquina, do ambiente de testes e da produção estejam sempre na mesma versão.
## Fase 3: Arquitetura com Spring Boot
A construção da aplicação web em si, seguindo as boas práticas da indústria.
- **Padrão de Camadas:** Separar o projeto em Controllers (camada web), Services (regras de negócio) e Repositories (acesso a dados).
- **APIs RESTful:** Padrões de rotas, uso correto dos verbos HTTP (GET, POST, PUT, DELETE) e códigos de status (200, 201, 400, 404, 500).
- **DTOs (Data Transfer Objects):** Nunca retorne suas entidades do banco de dados diretamente na API. Estude como mapear entidades para DTOs (usando bibliotecas como MapStruct).
- **Validação de Dados:** Uso do _Bean Validation_ (`@NotNull`, `@Size`, `@Email`) para impedir que dados sujos entrem no seu sistema.
- **Tratamento Global de Erros:** Usar `@ControllerAdvice` para capturar exceções em qualquer lugar do código e retornar JSONs de erro padronizados e elegantes.
- **Spring Security:** O módulo mais importante e complexo. Aprenda a bloquear rotas, criar autenticação via **Tokens JWT (JSON Web Tokens)** e gerenciar permissões (Role-based access).
## Fase 4: Qualidade e Testes Automatizados
Nenhum projeto de engenharia de software real existe sem testes.
- **Testes Unitários:** Usar o **JUnit 5** para testar seus métodos isoladamente.
- **Mocks:** Usar o **Mockito** para simular comportamentos de classes dependentes (por exemplo, testar um Service sem precisar conectar no banco de dados real).
- **Testes de Integração com Testcontainers:** Uma ferramenta fantástica que sobe um container Docker de um PostgreSQL real, roda os testes batendo no banco e depois destrói o container automaticamente.
## Fase 5: DevOps e CI/CD
Transformando o código local em um artefato pronto para produção.
- **Docker Básico:** Como escrever um `Dockerfile` otimizado (Multi-stage build) para compilar a aplicação e gerar uma imagem leve apenas com o JRE.
- **Docker Compose:** Como criar um arquivo `docker-compose.yml` para subir a sua API Java e o PostgreSQL juntos com um único comando na máquina local.
- **Pipeline de CI (Continuous Integration):** Usar o GitHub Actions para: baixar o código, compilar, rodar testes (JUnit) e executar o **SonarQube** para análise de qualidade e segurança.
- **Pipeline de CD (Continuous Deployment):** Adicionar um passo no GitHub Actions para fazer o build da imagem Docker e enviá-la para o Docker Hub.
## Fase 6: Observabilidade e Monitoramento (O Diferencial)
Em produção, você precisa saber o que está acontecendo sem olhar o terminal. Para quem gosta de análise de dados e dashboards, esta é a parte mais visual do backend.
- **Logs Estruturados:** Como usar o Logback para gerar logs úteis.
- **Spring Boot Actuator:** Um módulo que expõe _endpoints_ de saúde da sua API (uso de CPU, memória, status do banco de dados).
- **Métricas com Prometheus:** Configurar o Prometheus para raspar esses dados do Actuator e armazená-los.
- **Dashboards com Grafana:** Conectar o Grafana ao Prometheus para criar painéis visuais em tempo real da saúde do seu sistema.
---

## Fase 1: A Base da Máquina e do Código
- [ ] **Sobrevivência no Linux (Terminal):** Dominar navegação (`cd`, `ls`), manipulação de arquivos, permissões octais (`chmod`, `chown`) e editores de texto de terminal (`nano`/`vim`). #infra/linux
- [ ] **Java Moderno (Core):** Aprofundar em Orientação a Objetos avançada, tratamento de exceções (Checked/Unchecked) e Java Collections Framework (List, Set, Map). #backend/java
- [ ] **Programação Funcional e Concorrência:** Dominar expressões Lambda, API de Streams e conceitos básicos de Threads. #backend/java
- [ ] **Criptografia Básica:** Entender a diferença prática e matemática entre algoritmos de Hashing (mão única) e Encriptação (duas mãos). #seguranca/fundamentos

## Fase 2: Dados e Ambiente Local
- [ ] **Docker Essencial:** Aprender a subir containers básicos na máquina local para evitar instalações poluídas no sistema operacional hospedeiro. #devops/docker
- [ ] **PostgreSQL - Fundamentos e Concorrência:** Subir o Postgres via Docker, entender a tipagem rigorosa, o controle de concorrência (MVCC) e o tipo UUID. #dados/postgres
- [ ] **PostgreSQL - Avançado:** Explorar colunas JSONB para dados não estruturados e o conceito de transações (ACID). #dados/postgres
- [ ] **AppSec (OWASP Top 10):** Estudar as principais vulnerabilidades web (especialmente Injeção de SQL e Quebra de Autenticação) e Modelagem de Ameaças. #seguranca/owasp

## Fase 3: O Coração da Aplicação (Spring Boot)
- [ ] **Arquitetura de API RESTful:** Criar o projeto no Spring Initializr, estruturar em camadas (Controllers, Services, Repositories) e padronizar DTOs. #backend/spring
- [ ] **Spring Data JPA:** Configurar a conexão com o Postgres, fazer o mapeamento objeto-relacional (`@Entity`) e entender o problema de N+1 consultas. #dados/jpa
- [ ] **Validação e Tratamento de Erros:** Implementar Bean Validation e um tratador global de exceções (`@ControllerAdvice`). #backend/spring
- [ ] **Migrações de Banco de Dados:** Integrar o Flyway (ou Liquibase) para versionar estruturalmente o banco de dados sem intervenção manual. #dados/flyway

## Fase 4: A Blindagem da API
- [ ] **Spring Security (Filtros):** Entender a arquitetura de Filter Chain, CORS e proteções nativas contra CSRF. #seguranca/spring-security
- [ ] **Autenticação com JWT:** Implementar login seguro, gerar e validar Tokens JWT e garantir o hash seguro de senhas no banco (ex: BCrypt). #seguranca/autenticacao
- [ ] **Testes Unitários:** Isolar as regras de negócio usando JUnit 5 e Mockito. #backend/testes
- [ ] **Testes de Integração com Testcontainers:** Configurar testes automatizados que levantam um container PostgreSQL real temporário usando `@ServiceConnection`. #backend/testes

## Fase 5: O Servidor Bare Metal (Hardware Físico)
- [ ] **Instalação Headless:** Fazer o flash da imagem do Debian (ou OS otimizado da sua placa) no hardware físico e provisionar o acesso de rede inicial. #infra/baremetal
- [ ] **Acesso Remoto Seguro (SSH):** Gerar chaves criptográficas (`ssh-keygen`), transferir a chave pública e desativar o login via senha padrão. #seguranca/ssh
- [ ] **Segurança de Rede:** Configurar IP estático e levantar o firewall descomplicado (UFW), fechando tudo exceto as portas 22, 80 e 443. #infra/rede
- [ ] **Preparação do Hospedeiro:** Instalar a Docker Engine oficial e configurar as permissões para o seu usuário padrão. #infra/docker

## Fase 6: Automação e DevSecOps (CI/CD)
- [ ] **Otimização de Imagens (Dockerfile):** Escrever um Dockerfile enxuto usando Alpine Linux, apenas com o JRE, e definir o limite de memória da JVM (`-Xmx`). #devops/docker
- [ ] **Integração Contínua (CI):** Criar um workflow no GitHub Actions para compilar o código e rodar os testes automaticamente a cada commit. #devops/github-actions
- [ ] **Análise de Qualidade e Segurança (SAST):** Adicionar o SonarQube e ferramentas de scan de dependências no pipeline para bloquear código vulnerável. #seguranca/sast
- [ ] **Entrega Contínua (CD):** Configurar o pipeline para fazer o build da imagem Docker otimizada e enviar para um repositório (ex: Docker Hub). #devops/github-actions

## Fase 7: Deploy e Exposição Segura
- [ ] **Isolamento de Rede Lógica:** Escrever o `docker-compose.yml` final, subindo a API e o PostgreSQL em uma rede virtual fechada, onde a porta 5432 não é exposta ao host. #infra/deploy
- [ ] **Auditoria de Banco (Opcional corporativo):** Configurar políticas de acesso restrito (RBAC) e extensões como pgAudit no servidor de produção. #seguranca/dados
- [ ] **Túneis Seguros (Zero Trust):** Configurar o Cloudflare Tunnels (ou um proxy reverso) para expor a aplicação para a internet pública sem abrir portas no roteador da sua rede local. #infra/rede

## Fase 8: Observabilidade (A Torre de Controle)
- [ ] **Health Checks e Métricas:** Ativar e configurar o Spring Boot Actuator para exportar os dados de saúde da API. #backend/observabilidade
- [ ] **Coleta e Dashboards:** Subir instâncias do Prometheus e Grafana no servidor físico para gerar painéis visuais dinâmicos de consumo de CPU, RAM e acessos em tempo real. #infra/observabilidade

---
# Checklist de estudos

# Roadmap Pedagógico: Java, DevSecOps e Infraestrutura

## Trilha 1: Fundamentos e Persistência (Teoria e Prática Isolada)
*Objetivo: Dominar as regras da linguagem e as particularidades do novo banco de dados antes de tocar em qualquer framework.*
- [ ] **Java Core Avançado:** Revisar Generics, tratamento de exceções (Checked vs Unchecked) e Java Collections Framework (List, Set, Map). #estudo/java
- [ ] **Programação Funcional no Java:** Estudar expressões Lambda, API de Streams e a classe `Optional`. #estudo/java
- [ ] **Transição MySQL para PostgreSQL:** Entender a tipagem forte do Postgres, Sequences vs Auto Increment, e o tipo UUID. #estudo/postgres
- [ ] **Postgres Avançado (MVCC e JSONB):** Estudar o controle de concorrência e como realizar buscas em colunas JSON não estruturadas. #estudo/postgres

## Trilha 2: O Pilar da Segurança e Ferramental Local
*Objetivo: Preparar o ambiente local de desenvolvimento e entender como os hackers pensam antes de construir APIs.*
- [ ] **Docker Básico:** Aprender os comandos essenciais para baixar e rodar containers na própria máquina (foco em levantar o PostgreSQL sem sujar o sistema operacional). #estudo/docker
- [ ] **Criptografia e Hashing:** Entender matematicamente a diferença entre eles e por que senhas devem usar algoritmos como BCrypt. #estudo/seguranca
- [ ] **AppSec (OWASP Top 10):** Estudar Injeção de SQL, Quebra de Autenticação e exposição de dados, focando nas estratégias de mitigação. #estudo/seguranca

## Trilha 3: O Ecossistema Spring (Desenvolvimento Backend)
*Objetivo: Juntar o Java e o PostgreSQL para construir a API, aplicando boas práticas de engenharia.*
- [ ] **Fundamentos do Spring Boot:** Padrão de injeção de dependências (Inversion of Control), anotações básicas e padrão de camadas (Controller, Service, Repository). #estudo/spring
- [ ] **Mapeamento e Spring Data JPA:** Conectar ao banco, mapear entidades (`@Entity`), entender o ciclo de vida do Hibernate e como evitar o problema de N+1 consultas. #estudo/jpa
- [ ] **Migrações e Validação:** Estudar o Flyway para versionamento de banco de dados e o Bean Validation para sanitização de dados de entrada na API. #estudo/spring
- [ ] **Testes de Integração:** Aprender a configurar o Testcontainers com `@ServiceConnection` para validar a lógica de banco de dados com um Postgres descartável. #estudo/testes

## Trilha 4: Blindagem Aplicada (Spring Security)
*Objetivo: Aplicar a teoria da Trilha 2 diretamente no código construído na Trilha 3.*
- [ ] **Arquitetura do Spring Security:** Estudar a Filter Chain e como o framework intercepta requisições HTTP. #estudo/spring-security
- [ ] **Autenticação Stateless (JWT):** Aprender a estrutura do JSON Web Token, como assiná-lo criptograficamente e como bloquear rotas da API baseadas em Roles. #estudo/seguranca

## Trilha 5: Infraestrutura Bare Metal (O Servidor Físico)
*Objetivo: Sair da nuvem e preparar o seu próprio hardware usando apenas a linha de comando.*
- [ ] **Sobrevivência no Linux:** Instalar o Debian/Raspberry OS Lite de forma *headless*, dominar a navegação (`cd`, `ls`), permissões (`chmod`, `chown`) e o editor `nano`/`vim`. #estudo/linux
- [ ] **Acesso Remoto e Redes:** Configurar IP estático, liberar portas essenciais no UFW (firewall) e monitorar consumo com o `htop`. #estudo/linux
- [ ] **Chaves SSH:** Gerar pares de chaves criptográficas (`ssh-keygen`), desativar o login por senha e garantir o acesso blindado ao servidor. #estudo/seguranca
- [ ] **Docker Host:** Instalar a Docker Engine no servidor físico e configurar o usuário para não depender do `sudo` a cada comando. #estudo/docker

## Trilha 6: Automação e Orquestração (DevSecOps)
*Objetivo: Fechar o ciclo. Fazer o código sair da sua máquina, ser testado automaticamente e rodar de forma isolada no servidor físico.*
- [ ] **Imagens Docker Otimizadas:** Estudar as diferenças entre JRE e JDK, a importância do Alpine Linux, e como limitar a memória do Java (`-Xmx`) no Dockerfile. #estudo/docker
- [ ] **GitHub Actions (CI/CD):** Criar um pipeline que roda `mvn clean test`, executa varredura de segurança (SonarQube) e publica a imagem Docker automaticamente. #estudo/devops
- [ ] **Orquestração com Docker Compose:** Escrever o arquivo YAML para rodar a API e o Postgres no servidor físico, garantindo que a rede virtual isole a porta 5432 do mundo externo. #estudo/devops
- [ ] **Túneis Zero Trust:** Estudar Cloudflare Tunnels para rotear o tráfego da internet de forma segura até a placa sem expor seu IP residencial. #estudo/redes
- [ ] **Observabilidade (Extra):** Ativar o Spring Boot Actuator e conectar ao Prometheus/Grafana para criar dashboards analíticos de performance. #estudo/observabilidade