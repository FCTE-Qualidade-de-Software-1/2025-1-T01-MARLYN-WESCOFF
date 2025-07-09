# Usabilidade - M1: Taxa de Sucesso da Tarefa utilizando ferramentas de acessibilidade

## Introdução

 A métrica M1, Taxa de Sucesso da Tarefa (Task Success Rate - TSR), é um indicador fundamental para avaliar a usabilidade real e funcional 
 de uma plataforma sob a perspectiva da acessibilidade. Enquanto outras métricas podem focar em conformidade técnica, a M1 mede, 
 quantitativamente, a porcentagem de usuários que conseguem completar uma tarefa predefinida com sucesso, validando a eficácia do sistema no 
 mundo real.

## Referencial teórico 

A principal base para a definição de usabilidade vem da norma ISO 9241-11:2018 (Ergonomia da interação humano-sistema). Este padrão internacional define usabilidade como "a medida na qual um produto pode ser usado por usuários específicos para alcançar objetivos específicos com eficácia, eficiência e satisfação em um contexto de uso específico". A Métrica M1, Taxa de Sucesso da Tarefa (TSR), está diretamente ligada ao pilar da eficácia.

## Análise

Para a análise deste tópico, foi utilizada a ferramenta de acessibilidade **"Acessibility Scanner"**, fornecida pelo Google para plataformas Android. O objetivo foi simular a experiência de um usuário que depende de tecnologias assistivas e verificar, de forma prática, a eficácia do sistema na conclusão de tarefas essenciais.

A metodologia consistiu em executar um conjunto de tarefas predefinidas, que representam os fluxos mais críticos da aplicação, enquanto o **Acessibility Scanner** estava ativo. A ferramenta identifica e sugere melhorias em tempo real para diversos elementos da interface, como:

* **Rótulos de conteúdo:** Verifica se ícones e botões possuem descrições textuais claras para leitores de tela.
* **Área de toque:** Garante que elementos interativos tenham um tamanho adequado para usuários com dificuldades motoras.
* **Contraste de itens:** Analisa se o contraste entre texto, imagens e o fundo atende aos requisitos mínimos, beneficiando usuários com baixa visão.

O sucesso na tarefa foi considerado quando o usuário conseguia completar o fluxo do início ao fim sem encontrar barreiras de acessibilidade que o impedissem de prosseguir, mesmo que a ferramenta apontasse sugestões de melhoria que não bloqueavam a ação.

As tarefas selecionadas para análise foram:

* **Tarefa 1:** *[Descreva aqui a primeira tarefa. Ex: Realizar o login na aplicação utilizando as credenciais salvas.]*
* **Tarefa 2:** *[Descreva aqui a segunda tarefa. Ex: Navegar até a seção de produtos e adicionar um item ao carrinho de compras.]*
* **Tarefa 3:** *[Descreva aqui a terceira tarefa. Ex: Acessar o perfil do usuário e editar o endereço de entrega.]*

A seguir, serão apresentados os resultados detalhados da execução de cada uma dessas tarefas, documentando os pontos de sucesso e as barreiras encontradas.

## Resultados da Métrica M1

A análise da **Taxa de Sucesso da Tarefa (TSR)** utilizando ferramentas de acessibilidade buscou verificar se um usuário com deficiência conseguiria completar os fluxos essenciais da aplicação. A avaliação, baseada nas observações manuais e nos problemas técnicos encontrados, revelou a existência de barreiras críticas que levam a uma baixa ou nula taxa de sucesso em tarefas fundamentais.

### Análise de Tarefas Essenciais

Foram avaliados os seguintes cenários de tarefas, com base nos problemas documentados:

* **Tarefa 1: Realizar Login ou Cadastro**
    * **Observação:** Foi identificado que a "Navegação por telas não funciona em alguns campos" e que o "Contraste falho no botão de criar conta" dificulta a leitura. Adicionalmente, o fluxo de login se mostrou confuso, com o sistema navegando entre telas de forma inesperada.
    * **Análise de Sucesso:** A incapacidade de navegar para campos essenciais do formulário via teclado representa uma **barreira bloqueadora**. Um usuário que depende do teclado **não consegue** completar o cadastro ou login. Portanto, a taxa de sucesso para este perfil de usuário é de **0%**.

* **Tarefa 2: Acessar Conteúdo Informativo na Tela Inicial**
    * **Observação:** Foi constatado que o "Leitor de telas não lê o carrossel" , que é um componente de destaque na tela inicial.
    * **Análise de Sucesso:** Qualquer tarefa que dependa da informação contida no carrossel (ex: "encontrar a promoção X" ou "ver as novidades") é **impossível** para um usuário com deficiência visual que utiliza leitor de telas. A taxa de sucesso para este perfil de usuário nesta tarefa é de **0%**.

### Conclusão dos Resultados

A combinação de falhas críticas de navegação e componentes inacessíveis resulta em uma **Taxa de Sucesso da Tarefa (TSR) extremamente baixa** para usuários que dependem de tecnologias assistivas. Para múltiplos fluxos essenciais da aplicação, a taxa de sucesso para esses usuários é efetivamente **0%**, pois eles são completamente impedidos de prosseguir.

**Recomendação:** A correção das barreiras bloqueadoras identificadas nas outras métricas (especialmente as de navegação por teclado e acessibilidade de componentes) é de **prioridade máxima**. Enquanto estes problemas não forem resolvidos, a aplicação não pode ser considerada funcionalmente eficaz para usuários com deficiências motoras ou visuais.

## Referências Bibliográficas

> [1] ISO/IEC. ISO/IEC 25010:2011 — Systems and software engineering – Systems and software Quality Requirements and Evaluation (SQuaRE) – System and software quality models. International Organization for Standardization, 2011.

> [2] NIELSEN, Jakob. Mobile Usability. Berkeley: New Riders Pub, 2012.
