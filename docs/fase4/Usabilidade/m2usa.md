# Usabilidade - M2: Índice de Conformidade de Feedback Não-Dependente de Cor

## Introdução

  A métrica M2, Índice de Conformidade de Feedback Não-Dependente de Cor, avalia um dos princípios mais importantes da acessibilidade digital: 
  garantir que a cor não seja o único meio utilizado para transmitir informações críticas, indicar uma ação ou solicitar uma resposta. Este 
  índice mede, de forma percentual, a quantidade de componentes e elementos de feedback da interface que utilizam um reforço visual — como 
  ícones, texto explícito ou padrões — para complementar a informação transmitida pela cor.

## Referencial teórico 

  Esta abordagem, fundamentada na diretriz 1.4.1 do WCAG (Web Content Accessibility Guidelines), é essencial para assegurar que usuários com 
  deficiências de visão de cores, como o daltonismo, ou aqueles que utilizam telas monocromáticas, possam perceber e interpretar corretamente 
  o status de uma ação, alertas de erro ou dados em um gráfico. A falha em prover um canal de informação redundante pode tornar partes da 
  interface incompreensíveis para uma parcela significativa dos usuários.

## Análise

A análise para o **Índice de Conformidade de Feedback Não-Dependente de Cor** foi conduzida através de uma **metodologia híbrida**, combinando uma rigorosa **inspeção visual manual** com o suporte da ferramenta **Accessibility Scanner** do Google para Android. O objetivo foi identificar de forma exaustiva todos os componentes da interface que utilizam a cor como único meio para transmitir informações importantes.

O principal método de avaliação consistiu na navegação sistemática por todas as telas e fluxos da aplicação. Durante esta inspeção, foi aplicado um filtro de **escala de cinza** para simular a experiência de um usuário que não consegue distinguir cores. Este teste prático permite verificar instantaneamente se alguma informação ou contexto é perdido quando a cor é removida da interface.

Complementarmente, o **Accessibility Scanner** foi executado nas telas onde foram identificados potenciais problemas. Embora a ferramenta não possua uma verificação direta para `"uso exclusivo de cor"`, suas outras análises, como a de contraste, ajudaram a confirmar e a fornecer dados adicionais sobre os componentes que já estavam sob investigação, reforçando a necessidade de melhorias.

A inspeção focou em verificar um checklist de elementos críticos, incluindo:

* **Alertas e Notificações:** Verificação se mensagens de sucesso, erro ou aviso possuem um ícone ou prefixo textual além da cor de fundo (verde, vermelho, amarelo).
* **Validação de Formulários:** Análise se campos com erros ou obrigatórios são indicados apenas por uma borda colorida ou se há também um texto descritivo e um ícone.
* **Links em Texto:** Checagem se links inseridos em parágrafos são diferenciados do resto do texto por um sublinhado ou outra forma que não seja apenas a cor.
* **Gráficos e Visualização de Dados:** Investigação se diferentes categorias em gráficos são distinguíveis por meio de padrões, hachuras ou legendas textuais, além das cores.

Os resultados compilados a partir desta análise combinada serão detalhados a seguir, apontando cada componente que falha em prover um canal de informação redundante à cor.

## Resultados

A partir da execução da métrica M1, observou-se que a tarefa de Realizar Cadastro na CSA pôde ser completada com relativa fluidez, apresentando um tempo médio de 26,10 segundos, indicando um bom desempenho da interface quanto à agilidade e simplicidade de interação.

No entanto, durante a análise prática, foi identificada uma interferência significativa no fluxo da tarefa: ao tocar no botão "Criar uma conta", a tela de cadastro pisca brevemente e é sobreposta por um modal de busca de CSA, forçando o usuário a uma etapa manualmente para retomar o processo. Esse tipo de comportamento pode causar confusão e frustração, além de violar o princípio de previsibilidade da interface.

Dessa forma, considerando os critérios definidos na Fase 2, a métrica M1 foi classificada com a **pontuação 7 (Bom)**, o que significa que a aplicação atende de forma satisfatória, mas apresenta oportunidades claras de melhoria, especialmente relacionadas ao fluxo de navegação e comportamento da interface.

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