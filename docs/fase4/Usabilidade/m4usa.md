# Usabilidade - M4: Cobertura de Alternativas Textuais em Imagens Informativas

## Introdução

 A métrica M4, Cobertura de Alternativas Textuais em Imagens Informativas, avalia o pilar fundamental da acessibilidade na web: a capacidade 
 de um sistema de prover equivalentes textuais para conteúdo visual. Este indicador mede a porcentagem de imagens que possuem uma função 
 informativa e que são acompanhadas de uma alternativa textual (por meio do atributo alt em HTML) que descreve de forma concisa e fiel o seu 
 conteúdo e propósito.

## Referencial teórico 

  O referencial teórico para a Métrica M4 é o critério de sucesso mais fundamental e conhecido das Diretrizes de Acessibilidade para Conteúdo 
  Web (WCAG) 2.1. Ele está situado no Princípio 1: Perceptível, que estabelece que a informação não pode ser invisível a todos os sentidos do 
  usuário. Especificamente, a métrica se baseia no critério de sucesso de nível A, 1.1.1 Conteúdo Não Textual (Non-text Content).

  Este critério exige que "todo conteúdo não textual que é apresentado ao usuário tenha uma alternativa em texto que sirva o mesmo propósito". 
  Para usuários com deficiência visual, que utilizam leitores de tela, essa alternativa textual é a única forma de compreender a informação 
  que uma imagem, gráfico ou ícone está transmitindo. Sem ela, o conteúdo visual é efetivamente inexistente para esses usuários, criando uma 
  barreira crítica de acesso à informação.

## Análise

A análise da Métrica M4 foi realizada em um ambiente de **aplicação móvel nativa (Android)**, focando na verificação da correta implementação de alternativas textuais para conteúdo visual. Para garantir uma avaliação completa e precisa, foi adotada uma metodologia híbrida que combina varredura automática e teste manual interativo.

Inicialmente, a ferramenta **Accessibility Scanner** foi utilizada para uma varredura geral da aplicação, identificando de forma rápida os componentes de imagem que não possuíam um "rótulo de conteúdo" (`contentDescription`) associado. Este passo serviu como um levantamento preliminar de falhas óbvias.

A etapa principal da análise, no entanto, consistiu no teste manual utilizando o **TalkBack**, o leitor de tela oficial do sistema operacional Android. Este teste é essencial, pois simula a experiência real de um usuário com deficiência visual e permite não apenas identificar a ausência de descrições, mas também avaliar a qualidade e a utilidade das que já existem. O processo seguiu os seguintes passos:

1. O **TalkBack** foi ativado nas configurações de acessibilidade do dispositivo.
2. A navegação pela aplicação foi feita utilizando os gestos padrão do **TalkBack** (deslizar para a direita/esquerda para mover o foco entre os elementos).
3. Ao focar em cada imagem ou componente visual, a descrição anunciada em áudio foi cuidadosamente ouvida e avaliada.

O critério de avaliação para cada imagem seguiu um processo de duas etapas:

1. **Classificação:** A imagem foi classificada como "**informativa**" (se transmite uma informação essencial) ou "**decorativa**" (se seu propósito é puramente estético).
2. **Verificação:**
    * Para imagens **informativas**, foi verificado se o texto anunciado pelo **TalkBack** era claro, conciso e transmitia o mesmo significado da imagem.
    * Para imagens **decorativas**, foi verificado se eram corretamente ignoradas pelo leitor de tela, evitando "ruído" desnecessário na navegação auditiva.

A compilação dos resultados desta análise dupla — varredura automática e validação auditiva com o **TalkBack** — será apresentada a seguir, com um inventário detalhado das imagens que requerem correção para estarem em plena conformidade.

## Resultados da Métrica M1

A análise da **Taxa de Sucesso da Tarefa (TSR)** utilizando ferramentas de acessibilidade buscou verificar se um usuário com deficiência conseguiria completar os fluxos essenciais da aplicação. A avaliação, baseada nas observações manuais e nos problemas técnicos encontrados, revelou a existência de barreiras críticas que levam a uma baixa ou nula taxa de sucesso em tarefas fundamentais.

### Análise de Tarefas Essenciais

Foram avaliados os seguintes cenários de tarefas, com base nos problemas documentados:

* **Tarefa 1: Realizar Login ou Cadastro**
    * **Observação:** Foi identificado que a "Navegação por telas não funciona em alguns campos" e que o "Contraste falho no botão de criar conta"  dificulta a leitura. Adicionalmente, o fluxo de login se mostrou confuso, com o sistema navegando entre telas de forma inesperada.
    * **Análise de Sucesso:** A incapacidade de navegar para campos essenciais do formulário via teclado representa uma **barreira bloqueadora**. Um usuário que depende do teclado **não consegue** completar o cadastro ou login. Portanto, a taxa de sucesso para este perfil de usuário é de **0%**.

* **Tarefa 2: Acessar Conteúdo Informativo na Tela Inicial**
    * **Observação:** Foi constatado que o "Leitor de telas não lê o carrossel", que é um componente de destaque na tela inicial.
    * **Análise de Sucesso:** Qualquer tarefa que dependa da informação contida no carrossel (ex: "encontrar a promoção X" ou "ver as novidades") é **impossível** para um usuário com deficiência visual que utiliza leitor de telas. A taxa de sucesso para este perfil de usuário nesta tarefa é de **0%**.

### Conclusão dos Resultados

A combinação de falhas críticas de navegação e componentes inacessíveis resulta em uma **Taxa de Sucesso da Tarefa (TSR) extremamente baixa** para usuários que dependem de tecnologias assistivas. Para múltiplos fluxos essenciais da aplicação, a taxa de sucesso para esses usuários é efetivamente **0%**, pois eles são completamente impedidos de prosseguir.

**Recomendação:** A correção das barreiras bloqueadoras identificadas nas outras métricas (especialmente as de navegação por teclado e acessibilidade de componentes) é de **prioridade máxima**. Enquanto estes problemas não forem resolvidos, a aplicação não pode ser considerada funcionalmente eficaz para usuários com deficiências motoras ou visuais.

## Bibliografia

> \- Documentação de histórias de usuário do AgroMart. Disponível em: <https://agromart.github.io/docs/docs/modelagem/historiaDeUsuario/co-agricultor>. Acesso em: 07 de julho de 2025.

## Referências Bibliográficas

> [1] ISO/IEC. ISO/IEC 25010:2011 — Systems and software engineering – Systems and software Quality Requirements and Evaluation (SQuaRE) – System and software quality models. International Organization for Standardization, 2011.

> [2] NIELSEN, Jakob. Mobile Usability. Berkeley: New Riders Pub, 2012.

## Histórico de Versões

|Versão|Data|Descrição|Autor|Revisor|
|:----:|----|---------|-----|:-------:|
|`1.0`|07/07/2025|Criação do documento| [Weverton Rodrigues](https://github.com/vevetin) | [Ana Júlia](https://github.com/ailujana) |
|`1.1`|07/07/2025|Melhoria da escrita|[Maria Clara](https://github.com/Oleari19)| [Maurício Ferreira](https://github.com/mauricio-araujoo) |