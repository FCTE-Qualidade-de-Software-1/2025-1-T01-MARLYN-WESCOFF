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

## Resultados da Métrica M2

A análise da conformidade de feedback não-dependente de cor foi realizada através da inspeção visual e funcional da aplicação. O objetivo era identificar se informações críticas eram transmitidas unicamente através da cor, o que representa uma barreira de acessibilidade, conforme a diretriz **WCAG 1.4.1**.

### Cenário de Análise: Validação de Formulários

O principal cenário onde esta métrica foi avaliada foi nos formulários de **Login** e **Cadastro**. A metodologia consistiu em tentar submeter os formulários com campos obrigatórios não preenchidos para observar a resposta do sistema.

#### Observações

* **Identificação de Erro:** Foi observado que, ao deixar um campo obrigatório em branco, o sistema indica o erro alterando a cor dos campos para vermelho.
* **Análise de Conformidade:** A indicação de erro depende exclusivamente da cor vermelha. Não há um ícone de alerta ou um texto auxiliar que acompanhe a mudança de cor para descrever o erro (ex: "Este campo é obrigatório").

### Conclusão dos Resultados

A análise revelou uma **não conformidade** com o critério de acessibilidade. A confiança exclusiva na cor vermelha para sinalizar erros em formulários significa que um usuário com deficiência de visão de cores (como o daltonismo) pode não perceber qual campo precisa ser corrigido.

**Índice de Conformidade para este cenário: 0%** (considerando que o principal método de feedback de erro do formulário não é acompanhado por um indicador textual ou icônico).

**Recomendação:** Implementar um texto de erro visível abaixo de cada campo inválido e/ou um ícone de alerta ao lado do campo. Isso garantirá que a informação seja transmitida de forma redundante, atendendo aos requisitos de acessibilidade e melhorando a usabilidade para todos os usuários.

## Referências Bibliográficas

<a id="ref5"></a>
> WCAG 2.2 Understanding Docs. SC 1.4.1 Use of Color (Level A). Disponível em: [https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html). Acesso em: 1 Jul. 2025.

> [NBR] ABNT NBR 17225:2025, Acessibilidade em conteúdo e aplicações web – Requisitos. Disponível em: [https://mwpt.com.br/wp-content/uploads/2025/04/ABNT-NBR-17225-Acessibilidade-Digital.pdf](https://mwpt.com.br/wp-content/uploads/2025/04/ABNT-NBR-17225-Acessibilidade-Digital.pdf)
