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

## Resultados da Métrica M4

A análise da **Cobertura de Alternativas Textuais** foi realizada através de uma metodologia híbrida, combinando a varredura do Accessibility Scanner com a inspeção manual da experiência de um usuário de leitor de telas. A avaliação revelou falhas significativas na forma como os componentes visuais são descritos para tecnologias assistivas, o que viola o critério **WCAG 1.1.1 (Conteúdo Não Textual)**.

Os principais problemas identificados foram:

### 1. Descrições de Itens Duplicadas

A ferramenta Accessibility Scanner identificou um problema crítico em telas de formulário.

* **Observação:** Foi reportado o erro **"Item descriptions: Multiple items have the same description"** (Múltiplos itens têm a mesma descrição) na tela com os campos de "Senha" e "Confirmar Senha".
* **Análise:** Este erro geralmente ocorre quando múltiplos elementos, como os ícones de cadeado ao lado dos campos, possuem o mesmo rótulo acessível ou não possuem nenhum. Para um usuário de leitor de telas, isso torna impossível distinguir os dois campos, pois ambos seriam anunciados de forma idêntica, gerando grande confusão e potencial para erros.

### 2. Componentes Complexos sem Alternativa Textual

A avaliação manual, simulando o uso de um leitor de telas, identificou que componentes importantes da interface são completamente "invisíveis" para tecnologias assistivas.

* **Observação:** Foi constatado que o **"Leitor de telas não lê o carrossel"** da tela inicial.
* **Análise:** A inacessibilidade do carrossel indica que o componente foi construído sem os atributos de acessibilidade necessários para descrever seu conteúdo (as imagens e textos) e sua funcionalidade (os controles de navegação). Como resultado, todo o conteúdo informativo presente no carrossel é inacessível para usuários com deficiência visual.

### Conclusão dos Resultados

A aplicação possui falhas graves na implementação de alternativas textuais, tanto em componentes simples (ícones em formulários) quanto em componentes complexos (carrossel). Isso cria barreiras que impedem usuários de leitores de tela de compreender e interagir com partes essenciais da interface.

O **Índice de Cobertura de Alternativas Textuais** é considerado **Insatisfatório**, pois as falhas encontradas comprometem a funcionalidade e a percepção de informações críticas.

**Recomendação:** É necessária uma revisão completa de todos os componentes visuais e interativos da aplicação. Ícones e imagens informativas devem receber um rótulo acessível (`contentDescription` no Android) único e descritivo. Componentes complexos como o carrossel devem ser refatorados para serem totalmente compatíveis com leitores de tela.

## Referências Bibliográficas

> WCAG 2.2 SC 1.1.1. Disponível em: [https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html). Acesso em: 1 Jul. 2025

> [NBR] ABNT NBR 17225:2025, Acessibilidade em conteúdo e aplicações web – Requisitos. Disponível em: [https://mwpt.com.br/wp-content/uploads/2025/04/ABNT-NBR-17225-Acessibilidade-Digital.pdf](https://mwpt.com.br/wp-content/uploads/2025/04/ABNT-NBR-17225-Acessibilidade-Digital.pdf)