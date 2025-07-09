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

## Resultados da Métrica M3

A análise do **Índice de Conformidade de Contraste** revelou que este é um dos pontos mais críticos de acessibilidade na aplicação. Utilizando a ferramenta Accessibility Scanner e a inspeção visual, foram encontrados múltiplos componentes com taxas de contraste insuficientes, violando diretamente o critério **WCAG 1.4.3**.

### Levantamento dos Problemas de Contraste Encontrados

Os seguintes elementos apresentaram falhas de contraste em diversas telas da aplicação:

* **Botão "Criar Conta" / "Cadastrar":** O texto sobre o botão principal de ação possui contraste falho, dificultando a leitura. A tela de cadastro com este botão pode ser vista na página 5 do documento de análise.
* **Carrossel de Imagens:** O carrossel presente na tela inicial apresenta um contraste ruim entre as imagens de fundo e os elementos sobrepostos.
* **Campos de Formulário:** Foi detectado baixo contraste no texto dos campos de "Senha" e "Confirmar"  na tela de cadastro.
* **Ícones de Navegação:** Diversos ícones que funcionam como botões apresentaram baixo contraste, incluindo o botão "Home" na barra de navegação inferior, os ícones da barra de navegação em geral e os ícones de seta ">".

### Conclusão dos Resultados

A recorrência de problemas de contraste em componentes essenciais (botões de ação, campos de formulário e ícones de navegação) indica que a paleta de cores principal da aplicação não foi otimizada para acessibilidade. Isso prejudica diretamente usuários com baixa visão e pode dificultar o uso para todos os usuários em ambientes com muita luz.

O **Índice de Conformidade de Contraste** da aplicação é considerado **Insatisfatório**, dado que as falhas ocorrem em múltiplos fluxos críticos, como login, cadastro e navegação principal.

**Recomendação:** É necessária uma revisão completa da paleta de cores do design system da aplicação. A equipe de design deve ajustar as cores primárias e secundárias para garantir que todo texto atenda à taxa de contraste mínima de `4.5:1` e que os componentes gráficos e de interface atinjam a taxa mínima de `3:1`, conforme exigido pelo WCAG.

## Bibliografia

> \- Documentação de histórias de usuário do AgroMart. Disponível em: <https://agromart.github.io/docs/docs/modelagem/historiaDeUsuario/co-agricultor>. Acesso em: 07 de julho de 2025.

## Referências Bibliográficas

> [1] ISO/IEC. ISO/IEC 25010:2011 — Systems and software engineering – Systems and software Quality Requirements and Evaluation (SQuaRE) – System and software quality models. International Organization for Standardization, 2011.

> [2] NIELSEN, Jakob. Mobile Usability. Berkeley: New Riders Pub, 2012.

