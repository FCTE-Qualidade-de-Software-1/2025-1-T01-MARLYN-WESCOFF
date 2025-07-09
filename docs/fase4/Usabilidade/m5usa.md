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