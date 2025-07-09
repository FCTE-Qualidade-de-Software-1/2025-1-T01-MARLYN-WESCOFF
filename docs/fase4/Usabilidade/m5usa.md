# Usabilidade - M5: Índice de Conformidade de Feedback de Interação (Estado Ativo)

## Introdução

 A métrica M5, Índice de Conformidade de Feedback de Interação (Estado Ativo), avalia um princípio fundamental do design de interação, 
 conhecido como "Visibilidade do Status do Sistema". Este indicador quantifica a porcentagem de elementos interativos, como botões e links, 
 que fornecem um retorno visual imediato ao usuário no exato momento em que são ativados (o "clique").

## Referencial teórico 

  A recém-publicada norma ABNT NBR 17225:2025, que estabelece os requisitos de acessibilidade para conteúdo e aplicações web no Brasil, é diretamente baseada nas Diretrizes de Acessibilidade para Conteúdo Web (WCAG). Ambas tratam da assistência ao usuário na correção de erros, principalmente na Diretriz 3.3 - Assistência de Entrada. Os critérios de sucesso mais relevantes são:

  Critério 3.3.1 - Identificação de Erro (Nível A): Se um erro de entrada é detectado automaticamente, o item que contém o erro deve ser identificado e o erro deve ser descrito para o usuário em texto. Isso garante que usuários de tecnologias assistivas (como leitores de tela) sejam notificados sobre qual campo precisa de correção.

  Critério 3.3.3 - Sugestão de Erro (Nível AA): Se um erro é detectado e as sugestões para a correção são conhecidas, essas sugestões devem ser fornecidas ao usuário. Isso vai além de apenas apontar o erro, oferecendo um caminho claro para a solução.

## Análise

Conforme o referencial teórico, que se baseia nas diretrizes de **"Assistência de Entrada" (`WCAG 3.3`)** e na norma **ABNT NBR 17225**, a análise da Métrica M5 focou em avaliar a qualidade e a acessibilidade das mensagens de feedback do sistema, com ênfase no tratamento de erros. A metodologia consistiu em uma auditoria funcional manual, na qual foram simuladas interações que gerassem erros na aplicação para observar e avaliar a resposta do sistema.

O processo de análise envolveu a identificação dos principais fluxos de entrada de dados, como formulários de cadastro, login e painéis de configuração. Em cada fluxo, foram deliberadamente inseridos dados incorretos para provocar diferentes cenários de erro (ex: campos obrigatórios deixados em branco, formatos de dados inválidos, violação de regras de negócio). A resposta do sistema a cada ação foi então registrada.

Cada mensagem de feedback e erro foi avaliada com base nos seguintes critérios, derivados das boas práticas de usabilidade e acessibilidade:

* **Clareza e Visibilidade:** A mensagem é fácil de ver e escrita em linguagem simples, sem jargões técnicos?
* **Identificação Precisa (`WCAG 3.3.1`):** A mensagem aponta claramente qual campo está com erro e descreve a natureza do problema?
* **Sugestão Construtiva (`WCAG 3.3.3`):** A mensagem oferece uma sugestão útil de como o usuário pode corrigir a entrada?
* **Acessibilidade:** A mensagem de erro é associada programaticamente ao seu campo e anunciada de forma clara por leitores de tela (como o **TalkBack**)?

Os resultados desta auditoria serão apresentados a seguir, detalhando os cenários testados e a conformidade de cada feedback observado. O objetivo é identificar oportunidades para tornar o tratamento de erros da aplicação mais informativo, acessível e centrado no usuário.


## Resultados da Métrica M5

A análise da Métrica M5, focada na qualidade e acessibilidade das mensagens de feedback e erro, foi realizada através da simulação de erros nos fluxos de cadastro e login. A auditoria revelou não conformidades significativas com as diretrizes de usabilidade e acessibilidade (WCAG e NBR 17225).

Os problemas encontrados foram categorizados em duas frentes principais:

### 1. Validação de Formulários Dependente de Cor

Conforme observado durante os testes, o sistema utiliza a cor como único meio de sinalizar um erro em campos de formulário.

* **Observação:** Ao tentar submeter um formulário com um campo obrigatório não preenchido, o campo apenas altera sua cor para vermelho.
* **Análise:** Esta abordagem falha em dois critérios críticos de acessibilidade:
    * **Viola o WCAG 1.4.1 (Uso de Cor):** Usuários com deficiência de visão de cores (daltonismo) podem não perceber a mudança de cor, ficando sem saber qual campo precisa de correção.
    * **Viola o WCAG 3.3.1 (Identificação de Erro):** O erro não é descrito em texto. Uma prática acessível seria exibir uma mensagem clara abaixo do campo, como "Este campo é obrigatório".

### 2. Exposição de Mensagens de Erro Técnicas

Foi identificado que, em certas condições, o sistema exibe mensagens de estado técnico diretamente para o usuário, em vez de uma mensagem clara e compreensível.

* **Observação:** Na tela de login, foram observadas mensagens como `utilizando CSA: "undefined"` e `utilizando CSA: "null"`.
* **Análise:** Este tipo de feedback viola a heurística de usabilidade de "ajudar os usuários a reconhecer, diagnosticar e se recuperar de erros". Mensagens com jargões técnicos como "null" ou "undefined" não têm significado para o usuário final, gerando confusão e desconfiança em relação ao funcionamento da aplicação.

### Conclusão dos Resultados

O sistema de tratamento de erros da aplicação é considerado **Insatisfatório**. Ele falha em comunicar os erros de forma acessível e clara, dependendo apenas de cor e expondo jargões técnicos que não auxiliam o usuário.

**Recomendação:** É crucial refatorar o sistema de feedback. Todas as validações de erro devem ser acompanhadas de mensagens de texto explícitas e, sempre que possível, de um ícone. As mensagens de estado ou erro exibidas ao usuário devem ser reescritas em linguagem simples e humana, ocultando os detalhes de implementação do sistema.

## Referências Bibliográficas

> WCAG 2.2 Understanding Docs. SC 1.4.1 Use of Color (Level A). Disponível em: [https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html). Acesso em: 15 Jun. 2025.

> [NBR] ABNT NBR 17225:2025, Acessibilidade em conteúdo e aplicações web – Requisitos. Disponível em: [https://mwpt.com.br/wp-content/uploads/2025/04/ABNT-NBR-17225-Acessibilidade-Digital.pdf](https://mwpt.com.br/wp-content/uploads/2025/04/ABNT-NBR-17225-Acessibilidade-Digital.pdf)