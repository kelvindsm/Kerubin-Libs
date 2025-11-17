---
tags:
  - "#Emprogresso"
  - OrgArc2306
---
# Introdução
>[!quote] Conceito
>- Cloud computing é o fornecimento de serviços de computação, incluindo servidores, armazenamento, banco de dados, rede, software, análise e inteligência pela Internet ("A nuvem") para fornecer inovações mais rápidas, recursos flexíveis e economias de escala.
>- Normalmente se paga apenas pelos serviços de nuvem usados, ajudando a reduzir os custos operacionais, a executar sua infraestrutura com mais eficiência e a escalonar conforme a mudança das necessidades.
>- A "nuvem" fica armazenada em grandes data centers espalhados pelo mundo, gerida por grandes empresas conhecidas do mercado, fornecendo serviços de computação gratis ou pagos
>>[!info]
>>A palavra nuvem, referindo ao armazenamento de dados em servidores, surgiu por meio de como os recursos de computação são apresentados aos usuários, de modo que eles se mantenham "flutuando" em um ambiente virtual, como uma nuvem
# Características
- Mobilidade: várias formas de armazenar arquivos e acessá-los de qualquer lugar com internet;
- Multiplataforma: pode ser acessado de qualquer lugar e com diferentes plataformas físicas e lógicas;
- Escalabilidade/Elasticidade: é como o usuário pode aumentar e diminuir o consumo diante sua demanda
- Pay per use: só paga pelo que o usuário utiliza;
- Disponibilidade: capacidade de estar disponível constantemente.
# Local x Nuvem

# Modelos de Implementação em Cloud
## Public Cloud
- A nuvem pública pode ser definida como uma coleção de recursos e serviços computacionais oferecidos por diversos fornecedores por meio da internet. 
- Tecnologia disponibilizada por qualquer pessoa ou empresa que deseja utilizá-la, de acordo com a necessidade e a demanda a ser atendida em qualquer lugar do mundo.
### Características
- Elasticidade/escalável: permite que os recursos possam ser adaptados conforme a mudança da carga de trabalho, isso visa redução de custos, evitando desperdício e custo desnecessário.
- Multilocação: Deve servir uma infinidade de usuários, não apenas um;
- Autosserviço: Todo o gerenciamento necessário dos aplicativos e serviços é realizado em tempo integral, com facilidade e de forma automatizada. Dispensa interação humana entre provedor de serviço e cliente.
## Private Cloud
- Compreende uma infraestrutura operada e utilizada pela própria organização, não estando publicamente disponível para uso geral. Em alguns casos pode ser gerenciada por terceiros.
### Características
- Seguro: por ser própria de uma organização, que implementa e gerencia o ambiente, a probabilidade de vazamento de dados é menor, pois a própria empresa a controla. 
- Disponibilidade: são menores as chances de instabilidade e queda de sistemas, permite rápida recuperação caso ocorra problemas pois há uma equipe de técnicos própria.
- Provimento de recursos: garante tempo de uso do servidor, largura de banda, memória e uso da rede, sem que seja necessária interação humana.
## Hybrid Cloud
- Associa os dois modelos de implementação da computação em núvem, privada e pública, permitindo que os ambientes de infraestrutura de TI mais complexos sejam migrados sem maiores inconvenientes em relação à compatibilidade e à adaptabilidade do novo ambiente em relação ao antigo
- Desse modo, é possível adaptar as funcionalidades de ambas as nuvens em uma só, pois proporciona versatilidade e mobilidade.
### Características
- Ideal para cenários em que é necessário combinar as características e as vantagens de mais de um modelo de implementação
- É possível que a carga de trabalho mantida pelos diferentes ambientes possa ser movida entre eles sempre que seja conveniente, além de gerenciados de forma unificada utilizando a mesma ferramenta.
## Community Cloud
- A nuvem comunitária é uma infraestrutura compartilhada entre múltiplas organizações, herdando a característica principal da nuvem pública, que é o compartilhamento de recursos.
### Características
- Pool de recursos é menor que na nuvem pública, porém ele geralmente é mais extenso do que a nuvem privada, pois sua dimensão depende diretamente do número de organizações e usuários envolvidos.
- Envolve um menor custo, pois os recursos são otimizados com o uso da virtualização
- Infraestrutura ideal para organizações que compartilham preocupações em comum.
# Modelos de serviço na Cloud
- Infrastructure as a service (IaaS)
- Platform as a Service (PaaS)
- Software as a Service (SaaS)
## IaaS
>[!quote] Conceito
>- Infraestrutura computacional virtualizada oferecida para substituir ou complementar a estrutura computacional de empresas
>- Exemplos: Amazon Web Services (AWS), Microsoft Azure, Google Compute Engine

- Vantagens: Flexibilidade e controle sobre recursos; ideal para escalabilidade personalizada; pagamento por uso.
- Desvantagens: Exigem conhecimento técnico para gerenciamento de servidores e segurança; O gerenciamento da estrutura pode ser complexo.
## PaaS
>[!quote] Conceito
>- Oferece uma plataforma de desenvolvimento, permitindo o desenvolvimento, gerenciamento e entrega de aplicativos sem ter que lidar com a infraestrutura do projeto
>- Exemplos: Google Firebase, Microsoft Azure App Service, Heroku.

- Vantagens: Dev's focam no código sem se preocupar com a infraestrutura; fácil integração com outros serviços e plataformas; escalabilidade automática.
- Desvantagens: Menor controle sobre a infra e configurações; Dependência a um fornecedor específico e dificuldade de portabilidade; Não é possível personalizar completamente a infraestrutura.
## SaaS
>[!quote] Conceito
>- Aplicações prontas que podem ser usados diretamente sem a necessidade de configuração ou gerenciamento de servidores
>- Exemplos: Google Workspace, Microsoft 365, Slack, Zoom

- Vantagens: Simplicidade de uso, não necessita manutenção; atualização e manutenção feitas pelo fornecedor; Ideal para quem precisa de soluções rápidas e acessíveis.
- Desvantagens: Controle limitado sobre as funcionalidades e personalização; Dependem completamente de conexão à internet; Preocupação com privacidade e segurança dos dados por serem gerenciados por terceiros.
# Segurança em cloud computing
>[!tip] Importância da segurança em nuvem
>- Garantia de recuperação em caso de perda de dados
>- Proteção de dados e redes contra roubos e ataques
>- Determinação de ocorrência de erros
>- Redução de impactos em caso de comprometimento

## Principais ameaças e vulnerabilidades
### Ameaças
- DDoS;
- Phishing;
- Malwares:
- Hackers Black Hat;
### Vulnerabilidades
- Falta de visibilidade;
- Configuração incorreta;
- Vulnerabilidades de dia zero;
## Medidas de segurança e proteção
- Criptografia de dados em repouso e em trânsito
- Segurança de rede, com uso de firewalls, controle de acesso à rede, VPN
- Zero Trust
- "Segurança 6 layers deep" da Google
## Boas práticas e recomendações
- Criptografia de dados
- Atualizações de segurança
- Backups regulares dos dados
- Monitoramento de atividades suspeitas
- Treinamento de equipe
# Multicloud
>[!quote] Conceito
>- É o uso de serviços de cloud de dois ou mais provedores para rodar aplicações, combinando nuvens públicas e privadas
>>[!tip] Vantagens e desvantagens
>> - Vantagens: o melhor de cada cloud, eficiência de custo, evita dependências, facilita inovação, redundância e disponibilidade, latência reduzida
>> - Desvantagens: aumento da complexidade de gerenciamento, manter segurança constante e integração de ambientes de software
# Edge computing
- Distribbuição da computação pelos diversos aparelhos de uma rede
- Vantagens: Baixa latência e redução de banda;
- Desvantagens: Gerenciamento de dispositivos, segurança descentralizada e custo inicial.
# Tendências em Cloud Computing
- I.A.: 
- Serverless: 