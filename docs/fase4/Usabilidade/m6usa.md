# Usabilidade - M6: Cobertura de navegação por teclado

## Introdução

  A métrica M6, Cobertura de Navegação por Teclado, avalia um requisito não-negociável da acessibilidade web: a capacidade de um usuário 
  operar 100% da interface sem depender de um mouse. Este indicador mede a porcentagem de todos os elementos interativos — como links, botões, 
  campos de formulário e componentes complexos — que são plenamente alcançáveis e funcionais utilizando exclusivamente comandos de teclado.

## Referencial teórico 

  A avaliação da navegabilidade via teclado, foco da Métrica M6, é um dos requisitos mais críticos da acessibilidade digital e está 
  diretamente ancorada no Princípio 2: Operável das Diretrizes de Acessibilidade para Conteúdo Web (WCAG) 2.1. O pilar desta análise é o 
  critério de sucesso de nível A, 2.1.1 Teclado (Keyboard). 
 
  A intenção deste critério de sucesso é garantir que, sempre que possível, o conteúdo possa ser operado por meio de um teclado ou interface 
  de teclado (para que um teclado alternativo possa ser usado). Quando o conteúdo pode ser operado por meio de um teclado ou teclado 
  alternativo, ele é operável por pessoas sem visão (que não podem usar dispositivos como mouses que exigem coordenação olho-mão), bem como 
  por pessoas que precisam usar teclados alternativos ou dispositivos de entrada que atuam como emuladores de teclado. Os emuladores de 
  teclado incluem software de entrada de voz, software de sopro e sopro, teclados na tela, software de digitalização e uma variedade de 
  tecnologias assistivas e teclados alternativos. Indivíduos com baixa visão também podem ter dificuldade em rastrear um ponteiro e achar o 
  uso do software muito mais fácil (ou somente possível) se puderem controlá-lo pelo teclado.

## Análise

A análise da Métrica M6 foi executada através de uma auditoria funcional completa e manual, com o objetivo de verificar na prática a cobertura e a qualidade da navegação por teclado na aplicação. O método consistiu em simular integralmente a experiência de um usuário que não utiliza um mouse, dependendo exclusivamente do teclado para navegação e interação.

O avaliador navegou por todas as telas e fluxos de trabalho da aplicação utilizando um conjunto padrão de comandos de teclado. A tecla `Tab` foi usada para avançar o foco entre os elementos interativos, `Shift+Tab` para retroceder, `Enter` e `Barra de Espaço` para ativar botões e links, e as `Teclas de Seta` para interagir com componentes complexos como menus e grupos de opções.

Durante a navegação, cada componente interativo foi avaliado com base em um checklist de critérios essenciais, derivados diretamente do critério WCAG 2.1.1 e de boas práticas de acessibilidade:

* **Alcançabilidade:** O elemento é focável via teclado?
* **Visibilidade do Foco:** O elemento em foco possui um indicador visual claro (`outline`) que o diferencia dos demais?
* **Operabilidade:** O elemento focado pode ser ativado ou manipulado com as teclas apropriadas (`Enter`, `Espaço`, setas)?
* **Ordem Lógica:** A sequência de foco (`tab order`) corresponde à ordem visual e lógica da página?
* **Ausência de Armadilhas (Keyboard Trap):** O foco do teclado nunca fica preso em um componente, permitindo sempre a navegação contínua?

Os resultados desta auditoria serão apresentados a seguir, com um levantamento detalhado de cada elemento que falhou em um ou mais dos critérios listados. Esta documentação servirá como um guia de alta prioridade para a correção das barreiras de navegação encontradas.


## Resultados da Métrica M6

A análise da cobertura de navegação por teclado, realizada através da inspeção funcional da aplicação, revelou barreiras de acessibilidade críticas que impedem a operação completa da interface sem o uso de um mouse. Os resultados indicam uma não conformidade com o critério **WCAG 2.1.1**, que exige que toda funcionalidade seja operável via teclado.

Os problemas identificados foram:

### 1. Componentes Complexos Inacessíveis

Certos componentes da interface não são reconhecidos ou operáveis por tecnologias assistivas, o que na prática os torna invisíveis para a navegação por teclado.

* **Observação:** Foi constatado que o "Leitor de telas não lê o carrossel" na tela inicial.
* **Análise:** A inacessibilidade do carrossel para leitores de tela é um forte indicativo de que o componente não foi construído com a semântica de código apropriada (seja HTML ou atributos nativos). Como resultado, o foco do teclado provavelmente ignora este componente por completo, impedindo que um usuário de teclado navegue por seus itens ou os ative.

### 2. Falhas na Navegação entre Campos

A auditoria manual identificou quebras no fluxo de navegação, impedindo o usuário de acessar todos os elementos interativos de forma sequencial.

* **Observação:** Foi reportado que a "Navegação por telas não funciona em alguns campos".
* **Análise:** Esta é uma falha de operabilidade grave. Ela sugere a existência de "focos fantasmas" (quando o foco do teclado desaparece), "armadilhas de teclado" (quando o foco fica preso em um elemento) ou que certos elementos que parecem interativos não são de fato focáveis. O resultado prático é que o usuário é bloqueado e não consegue completar sua jornada na aplicação.

### Conclusão dos Resultados

As falhas encontradas representam barreiras críticas que tornam a aplicação **inutilizável** para pessoas que dependem exclusivamente do teclado para navegar, como usuários com deficiências motoras.

O **Índice de Cobertura de Navegação por Teclado** é considerado **Insatisfatório**, pois problemas fundamentais foram encontrados em componentes importantes e no fluxo de navegação geral.

**Recomendação:** É necessária uma auditoria manual completa de teclado em todas as telas da aplicação para mapear cada falha na ordem de foco, na operabilidade dos componentes e para identificar "armadilhas". O componente de carrossel precisa ser refatorado ou substituído por uma alternativa acessível.

## Referências Bibliográficas

> [1] ISO/IEC. ISO/IEC 25010:2011 — Systems and software engineering – Systems and software Quality Requirements and Evaluation (SQuaRE) – System and software quality models. International Organization for Standardization, 2011.

> [2] NIELSEN, Jakob. Mobile Usability. Berkeley: New Riders Pub, 2012.

