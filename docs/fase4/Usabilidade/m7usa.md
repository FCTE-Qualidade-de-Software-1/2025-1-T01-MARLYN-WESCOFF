# Usabilidade - M7: Análise do código

## Introdução

  A métrica M7, Análise do Código, representa uma avaliação fundamental da qualidade técnica da plataforma, focando na estrutura que serve de 
  alicerce para toda a experiência do usuário. Diferente das métricas anteriores que avaliam a interface renderizada ou a interação do 
  usuário, esta análise mergulha no código-fonte (especificamente HTML e o uso de atributos ARIA) para avaliar sua conformidade com as 
  melhores práticas de acessibilidade e semântica.

## Referencial teórico 

  A análise é fundamentada diretamente nas diretrizes do WCAG (Web Content Accessibility Guidelines) 2.1, o padrão internacional para 
  acessibilidade na web. Para esta avaliação, um dos pilares centrais é o critério de sucesso 2.4.6 Títulos e Rótulos (Headings and Labels), 
  pertencente à diretriz de tornar o conteúdo navegável.

  O objetivo deste critério de sucesso é ajudar os usuários a entender quais informações estão contidas nas páginas da web e como essas 
  informações estão organizadas. Quando os títulos são claros e descritivos, os usuários encontram as informações que procuram com mais 
  facilidade e entendem as relações entre as diferentes partes do conteúdo com mais facilidade. Rótulos descritivos ajudam os usuários a 
  identificar componentes específicos dentro do conteúdo.

## Análise

A análise da Métrica M7 foi conduzida através de uma **revisão manual do código-fonte** das principais telas e componentes da aplicação. Utilizando as ferramentas de desenvolvedor do navegador para inspecionar o DOM (Document Object Model), o objetivo foi avaliar a qualidade da estrutura semântica do HTML e o uso de rótulos, tendo como base o critério WCAG 2.4.6.

A análise foi dividida em duas frentes principais, correspondendo às duas partes do critério:

### 1. Análise da Estrutura de Títulos (`<h1>` - `<h6>`)

Foi verificado se a hierarquia de títulos era utilizada de forma lógica para organizar o conteúdo da página, funcionando como um sumário para tecnologias assistivas. Os principais pontos de verificação foram:

* **Uso do `<h1>`:** Existência de um único `<h1>` por página, representando seu título principal.
* **Hierarquia Lógica:** Ausência de saltos na hierarquia (ex: um `<h4>` diretamente após um `<h2>`).
* **Uso Semântico:** Confirmação de que as tags de título foram usadas para titular seções e não apenas para fins de estilização visual.

### 2. Análise de Rótulos de Componentes

A segunda parte da análise concentrou-se nos rótulos de componentes interativos. Para cada elemento de formulário ou controle (como botões e links), foi verificado se existia um nome acessível claro e corretamente associado. Os critérios de avaliação incluíram:

* **Rótulos Explícitos:** Verificação se campos de formulário (`<input>`, etc.) possuíam uma tag `<label>` associada através do atributo `for`.
* **Nomes Acessíveis para Elementos Visuais:** Análise se botões e links que utilizam apenas ícones possuíam um rótulo alternativo fornecido via `aria-label` ou texto para leitores de tela.
* **Clareza do Rótulo:** Avaliação se o texto do rótulo descrevia de forma precisa e inequívoca a função do componente.

Os resultados desta revisão de código, incluindo exemplos de boas práticas e de pontos que necessitam de refatoração para estar em conformidade com o critério 2.4.6, serão apresentados a seguir. O objetivo é fornecer um guia técnico para a equipe de desenvolvimento aprimorar a base semântica da aplicação.
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