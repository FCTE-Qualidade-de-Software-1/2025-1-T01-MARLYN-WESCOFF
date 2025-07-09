# Usabilidade - M3: Índice de Conformidade de Contraste (WCAG)

## Introdução

  A métrica M3, Índice de Conformidade de Contraste (WCAG), foca em um dos pilares mais essenciais da acessibilidade e do design de 
  interfaces: a legibilidade. Um contraste adequado entre o texto e sua cor de fundo é fundamental para garantir que o conteúdo possa ser lido 
  confortavelmente por todos, sendo um fator crítico para a inclusão de usuários com baixa visão.

## Referencial teórico 

  Este indicador mede a porcentagem de elementos textuais e componentes de interface que atendem às taxas de contraste mínimo estabelecidas 
  pelas Diretrizes de Acessibilidade para Conteúdo Web (WCAG), especificamente o critério de sucesso 1.4.3, que exige uma taxa de 4.5:1 para 
  texto de tamanho normal (nível AA). A não conformidade com este critério pode tornar o conteúdo efetivamente ilegível, não apenas para 
  pessoas com deficiências visuais, mas também para qualquer usuário em condições de iluminação não ideais, como sob a luz do sol em um 
  dispositivo móvel.

## Análise

A análise do **Índice de Conformidade de Contraste** foi conduzida de forma sistemática, tendo como principal instrumento a ferramenta **Accessibility Scanner** do Google. A capacidade desta ferramenta de calcular e verificar automaticamente as taxas de contraste da interface a torna ideal para a aplicação precisa e eficiente desta métrica.

O processo de avaliação consistiu em navegar por todas as telas e fluxos principais da aplicação. Em cada tela, o **Accessibility Scanner** foi ativado para realizar uma varredura completa. Todos os erros de **"Contraste de texto"** e **"Contraste de imagem"** apontados pela ferramenta foram registrados e catalogados. Para cada erro, foram documentadas as seguintes informações: a descrição do elemento (ex: "Texto do menu principal"), a taxa de contraste medida pela ferramenta, a taxa de contraste exigida pelo WCAG e uma captura de tela para localização visual.

A análise considerou como falha qualquer elemento que não atendesse aos critérios do `WCAG 1.4.3` (**Nível AA**), especificamente:

* **Texto de tamanho normal:** Taxa de contraste inferior a `4.5:1`.
* **Texto grande (18pt ou 14pt em negrito):** Taxa de contraste inferior a `3:1`.
* **Componentes de interface e elementos gráficos:** Taxa de contraste inferior a `3:1` em relação às cores adjacentes.

A seguir, será apresentado o levantamento completo de todos os objetos e componentes que apresentaram contraste insuficiente, formando um backlog claro de itens a serem corrigidos pela equipe de design para garantir a legibilidade e a acessibilidade da plataforma.

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