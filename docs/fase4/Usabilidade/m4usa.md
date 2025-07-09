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

## Resultados

A partir da execução da métrica M1, observou-se que a tarefa de Realizar Cadastro na CSA pôde ser completada com relativa fluidez, apresentando um tempo médio de 26,10 segundos, indicando um bom desempenho da interface quanto à agilidade e simplicidade de interação.

No entanto, durante a análise prática, foi identificada uma interferência significativa no fluxo da tarefa: ao tocar no botão "Criar uma conta", a tela de cadastro pisca brevemente e é sobreposta por um modal de busca de CSA, forçando o usuário a uma etapa manualmente para retomar o processo. Esse tipo de comportamento pode causar confusão e frustração, além de violar o princípio de previsibilidade da interface.

Dessa forma, considerando os critérios definidos na Fase 2, a métrica M1 foi classificada com a **pontuação 7 (Bom)**, o que significa que a aplicação atende de forma satisfatória, mas apresenta oportunidades claras de melhoria, especialmente relacionadas ao fluxo de navegação e comportamento da interface.

## Bibliografia

> \- Documentação de histórias de usuário do AgroMart. Disponível em: <https://agromart.github.io/docs/docs/modelagem/historiaDeUsuario/co-agricultor>. Acesso em: 07 de julho de 2025.

## Referências Bibliográficas

> [1] ISO/IEC. ISO/IEC 25010:2011 — Systems and software engineering – Systems and software Quality Requirements and Evaluation (SQuaRE) – System and software quality models. International Organization for Standardization, 2011.

> [2] NIELSEN, Jakob. Mobile Usability. Berkeley: New Riders Pub, 2012.

