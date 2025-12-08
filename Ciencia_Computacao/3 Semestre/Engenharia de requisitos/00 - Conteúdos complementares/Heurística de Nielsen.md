---
tags:
  - EngRequisitos
  - Concluido
---
# 10 Heurísticas de Usabilidade de Jakob Nielsen

## Heurística 1: Visibilidade do Status do Sistema

>[!info] Definição
>O design deve sempre manter os usuários informados sobre o que está acontecendo, através de feedback apropriado dentro de um tempo razoável.

- Saber o **status atual do sistema** ajuda os usuários a entenderem o resultado de suas interações anteriores e a determinar os **próximos passos**.
- Interações **previsíveis** criam **confiança** no produto e na marca.

>[!tip] Dicas
> - Comunique claramente o estado do sistema; nenhuma ação com consequências para os usuários deve ser tomada sem informá-los.
> - Apresente o feedback o mais rápido possível.
> - Construa **confiança** através de comunicação aberta e contínua.

>[!example] Exemplos
> - **Mapas "Você Está Aqui"**: Mapas interativos, como em shoppings, devem mostrar onde o usuário está atualmente para ajudá-lo a saber para onde ir em seguida.
> - **Fluxo de Checkout**: Processos de várias etapas mostram aos usuários quais etapas foram concluídas, qual está em andamento e o que vem a seguir.

---
## Heurística 2: Correspondência entre o Sistema e o Mundo Real

>[!info] Definição
>O design deve falar a **linguagem dos usuários**. Use palavras, frases e conceitos **familiares** a eles, em vez de **jargão interno**. Siga as **convenções do mundo real**, fazendo com que as informações apareçam em uma ordem natural e lógica.

- A linguagem a ser usada depende muito dos seus **usuários específicos**.

>[!tip] Dicas
> - Garanta que os usuários possam entender o significado sem ter que procurar a definição de uma palavra.
> - Nunca presuma que sua compreensão de palavras ou conceitos corresponderá à dos seus usuários.
> - A pesquisa com usuários ajuda a descobrir a **terminologia familiar** e os **modelos mentais** dos usuários sobre conceitos importantes.

>[!example] Exemplos
> - **Controles de Fogão**: Quando os controles do fogão correspondem ao layout dos elementos de aquecimento, os usuários podem rapidamente entender qual controle mapeia para cada elemento.
> - **Terminologia**: Se os usuários pensam em um objeto como "Carro", use essa palavra como rótulo em vez de "Automóvel".
> - **Ícone de Carrinho de Compras**: Um ícone de carrinho de compras é facilmente reconhecível porque o recurso tem o mesmo propósito que sua contraparte na vida real.

---

## Heurística 3: Controle e Liberdade do Usuário

>[!info] Definição
>Os usuários frequentemente cometem ações por engano. Eles precisam de uma **"saída de emergência"** claramente marcada para abandonar a ação indesejada sem ter que passar por um processo prolongado.

- Quando é fácil para as pessoas **voltar atrás** em um processo ou **desfazer** uma ação, isso promove uma sensação de **liberdade** e **confiança**.
- As saídas permitem que os usuários permaneçam no **controle** do sistema, evitando que fiquem presos e frustrados.

>[!tip] Dicas
> - Suporte as funções **Desfazer (Undo)** e **Refazer (Redo)**.
> - Mostre uma maneira clara de sair da interação atual, como um botão **"Cancelar"**.
> - Certifique-se de que a saída esteja **claramente rotulada** e **descoberta**.

>[!example] Exemplos
> - **Sinal de Saída**: Espaços digitais precisam de saídas de "emergência" rápidas, assim como espaços físicos.
> - **Desfazer e Refazer**: Essas funções dão liberdade aos usuários, pois eles não precisam se preocupar com suas ações — tudo é facilmente **reversível**.
> - **Botão Cancelar**: Os usuários não devem ser obrigados a se comprometer com um processo iniciado; devem ser capazes de **cancelar** e **abandonar** facilmente.

---

## Heurística 4: Consistência e Padrões

>[!info] Definição
>Os usuários não devem ter que se perguntar se diferentes palavras, situações ou ações significam a mesma coisa. **Siga as convenções** da plataforma e da indústria.

- A **[[Lei de Jakob]]** afirma que as pessoas gastam a maior parte do tempo em outros produtos além do seu.
- A falha em manter a **consistência** pode aumentar a **Carga Cognitiva** dos usuários, forçando-os a aprender algo novo.

>[!tip] Dicas
> - Melhore a **Apreensibilidade (Learnability)** mantendo a **consistência interna** (dentro do produto) e **externa** (seguindo convenções da indústria).

>[!example] Exemplos
> - **Balcão de Check-in**: Balcões de check-in são geralmente localizados na frente de hotéis. Essa consistência atende às expectativas dos clientes.
> - **Sistema de Design (Design System)**: Usar elementos do mesmo sistema de design em todas as linhas de produtos **reduz a curva de aprendizado** dos usuários.
> - **Notificações**: Um design de notificação padronizado fornece uma aparência e sensação semelhante, mas distinguível, para diferentes pop-ups de aplicativos.

---

## Heurística 5: Prevenção de Erros

>[!info] Definição
>Embora boas mensagens de erro sejam importantes, os melhores designs **previnem cuidadosamente** que problemas ocorram em primeiro lugar. Elimine condições propensas a erros ou verifique-as e apresente aos usuários uma **opção de confirmação** antes de se comprometerem com a ação.

- **Tipos de Erros**:
- **Lapsos (Slips)**: Erros inconscientes causados por desatenção.
- **Erros (Mistakes)**: Erros conscientes baseados em um descompasso entre o **modelo mental** do usuário e o design.

>[!tip] Dicas
> - Priorize o esforço: Previna **erros de alto custo** primeiro, depois pequenas frustrações.
> - Evite lapsos fornecendo **restrições úteis** e **bons padrões** (defaults).
> - Previna erros removendo **cargas de memória**, suportando **desfazer** e **avisando** os usuários.

>[!example] Exemplos
> - **Guarda-corpos**: Em estradas montanhosas, previnem que motoristas caiam de penhascos, representando a prevenção de erros.
> - **Confirmação de Reserva de Companhia Aérea**: A página de confirmação antes do checkout dá aos usuários outra chance de revisar os detalhes do voo.
> - **Seleção de Data no Calendário**: Oferecer bons padrões, definir limites e **esmaecer opções indisponíveis** ao selecionar datas.

---

## Heurística 6: Reconhecimento em Vez de Lembrete (Recall)

>[!info] Definição
>Minimize a **carga de memória** do usuário tornando elementos, ações e opções **visíveis**. O usuário não deve ter que se lembrar de informações de uma parte da interface para outra. As informações necessárias para usar o design devem estar **visíveis** ou **facilmente recuperáveis** quando necessário.

- Os humanos têm **memória de curto prazo limitada**. Interfaces que promovem o **reconhecimento** reduzem a quantidade de **esforço cognitivo** exigido dos usuários.
- É mais provável que as pessoas respondam corretamente à pergunta de **reconhecimento** ("Lisboa é a capital de Portugal?") do que à pergunta de **lembrete** ("Qual é a capital de Portugal?").

>[!tip] Dicas
> - Permita que as pessoas **reconheçam** informações na interface, em vez de terem que **lembrá-las** ("recall").
> - Ofereça **ajuda no contexto** (in-context), em vez de dar aos usuários um longo tutorial para memorizar.
> - Reduza a informação que os usuários têm que memorizar.

>[!example] Exemplos
> - **Tabelas de Comparação**: Listam as principais diferenças para que os usuários não precisem se lembrar delas para fazer comparações.
> - **Busca**: As consultas de busca são apresentadas juntamente com os resultados como uma **referência**.

---

## Heurística 7: Flexibilidade e Eficiência de Uso

>[!info] Definição
>Os **Atalhos (Shortcuts)** — escondidos de usuários novatos — podem **acelerar a interação** para o **usuário experiente**, permitindo que o design atenda tanto a usuários inexperientes quanto experientes. Permita que os usuários **personalizem** ações frequentes. Processos flexíveis podem ser realizados de diferentes maneiras, para que as pessoas possam escolher o método que funcione para elas.

>[!tip] Dicas
> - Forneça **aceleradores**, como atalhos de teclado e gestos de toque.
> - Ofereça **personalização** adaptando o conteúdo e a funcionalidade para usuários individuais.
> - Permita a **customização**, para que os usuários possam fazer seleções sobre como desejam que o produto funcione.

>[!example] Exemplos
> - **Atalhos (Mapas)**: Rotas regulares são listadas em mapas, mas usuários com mais conhecimento da área podem pegar atalhos.
> - **Atalhos de Teclado**: Podem ajudar usuários experientes em produtos complexos a finalizar suas tarefas com mais eficiência.
> - **Tocar para Curtir**: Aplicativos sociais permitem duas formas de curtir postagens. Usuários experientes podem tocar duas vezes para curtir porque isso agiliza a navegação.

---

## Heurística 8: Design Estético e Minimalista

>[!info] Definição
>As interfaces **não devem conter informações irrelevantes** ou raramente necessárias. Cada unidade extra de informação em uma interface compete com as unidades de informação relevantes e **diminui sua visibilidade relativa**.

- O foco é garantir que o conteúdo e o design visual estejam **centrados no essencial**.
- Garanta que os elementos visuais da [[Interface do Usuário (UI)]] suportem os **objetivos primários** do usuário.

>[!tip] Dicas
> - Mantenha o conteúdo e o design visual da UI focados no essencial.
> - Não permita que elementos desnecessários **distraiam** os usuários das informações de que realmente precisam.
> - Priorize o conteúdo e os recursos para suportar os objetivos primários.

>[!example] Exemplos
> - **Chaleira Ornamentada vs. Simples**: Elementos decorativos excessivos podem interferir na usabilidade.
> - **"Comunique, Não Decore"**: O excesso de decoração pode causar distração e dificultar que as pessoas obtenham a informação essencial.
> - **UI Bagunçada vs. Organizada**: Uma UI desorganizada aumenta o **custo de interação** para os usuários encontrarem o conteúdo desejado; uma UI organizada **diminui o custo**.

---

## Heurística 9: Ajude os Usuários a Reconhecer, Diagnosticar e se Recuperar de Erros

>[!info] Definição
>As mensagens de erro devem ser expressas em **linguagem simples** (sem códigos de erro), indicar o problema com **precisão** e sugerir uma **solução construtiva**.

- As mensagens de erro devem ser apresentadas com **tratamentos visuais** que ajudem os usuários a notá-las e reconhecê-las.

>[!tip] Dicas
> - Use visuais tradicionais de mensagens de erro, como **texto em negrito e vermelho**.
> - Diga aos usuários o que deu errado em uma linguagem que eles entenderão — **evite jargão técnico**.
> - Ofereça aos usuários uma **solução**, como um atalho que possa resolver o erro imediatamente.

>[!example] Exemplos
> - **Sinal de Sentido Proibido**: Sinais de sentido proibido na estrada lembram os motoristas de que estão na direção errada e pedem que parem.
> - **Erro de Conexão com a Internet**: Boas páginas de erro de conexão mostram o que aconteceu e instruem os usuários construtivamente sobre como corrigir o problema.
> - **Sem Resultados de Busca**: Forneça ajuda útil quando as pessoas encontrarem páginas de resultados de busca que retornam zero resultados, como sugerir tópicos populares.

---

## Heurística 10: Ajuda e Documentação

>[!info] Definição
>É melhor se o design não precisar de nenhuma explicação adicional. No entanto, pode ser necessário fornecer **documentação** para ajudar os usuários a entender como completar suas tarefas.

- O conteúdo de ajuda e documentação deve ser **fácil de buscar** e focado na **tarefa do usuário**.
- Mantenha-o **conciso** e liste **etapas concretas** que precisam ser realizadas.

>[!tip] Dicas
> - Garanta que a documentação de ajuda seja **fácil de pesquisar**.
> - Sempre que possível, apresente a documentação **no contexto** (in-context), no momento exato em que o usuário precisar dela.
> - Liste **etapas concretas** a serem realizadas.

>[!example] Exemplos
> - **Centro de Informações do Aeroporto**: Quiosques de informação em aeroportos são facilmente reconhecíveis e resolvem os problemas dos clientes **no contexto** e **imediatamente**.
> - **Perguntas Frequentes (FAQ)**: Boas páginas de FAQ antecipam e fornecem as informações úteis que os usuários podem precisar.
> - **Ícone de Informação (Tooltip)**: Ícones de informação revelam tooltips (dicas de ferramentas) para explicar jargões quando os usuários tocam ou pairam sobre eles, o que fornece **ajuda contextual**.

---