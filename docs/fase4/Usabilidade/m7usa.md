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

## Resultados da Métrica M7

A análise do código da aplicação, realizada com base nos relatórios do Accessibility Scanner e nos logs de console presentes no documento, revelou diversas oportunidades de melhoria na estrutura técnica, semântica e de navegação da plataforma.

Os resultados foram categorizados da seguinte forma:

### 1. Rótulos de Componente Duplicados e Ausentes

A análise apontou falhas na forma como os componentes são descritos para tecnologias assistivas, um pilar do critério WCAG 2.4.6 (Títulos e Rótulos).

* **Descrições Duplicadas:** Na tela de senha, a ferramenta identificou que "múltiplos itens têm a mesma descrição". Isso confunde usuários de leitores de tela, que não conseguem diferenciar campos como "Senha" e "Confirmar Senha" se ambos forem anunciados da mesma forma.
* **Componentes Sem Leitura:** Foi observado que o "leitor de telas não lê o carrossel" presente na tela inicial. Isso indica que o componente do carrossel foi construído sem os atributos de acessibilidade necessários (como papéis ARIA ou `contentDescription` adequados), tornando seu conteúdo invisível para usuários com deficiência visual.
* **Ponto Positivo:** Em uma nota positiva, foi verificado que o sistema identifica corretamente os papéis básicos de botões e campos de texto na maioria das telas.

### 2. Arquitetura de Navegação

Os logs do console da aplicação revelaram um problema estrutural na forma como as telas de navegação são nomeadas.

* **Nomes de Tela Aninhados:** O sistema emite um aviso de que foram "encontradas telas com o mesmo nome aninhadas umas nas outras", especificamente `Home, Home > Home`.
* **Impacto no Usuário:** O próprio log de erro alerta que este problema "pode causar um comportamento confuso durante a navegação", recomendando o uso de nomes únicos para cada tela.
* **Falha Funcional:** A observação de que a "navegação por telas não funciona em alguns campos" pode ser um sintoma direto desse problema de arquitetura.

### 3. Qualidade e Manutenção do Código

Foram identificados avisos que apontam para o uso de código que precisa de atualização.

* **Código Depreciado:** Um aviso no console indica que `ViewPropTypes` será removido de futuras versões do React Native. Embora não seja um erro de acessibilidade direto, o uso de padrões de código depreciados é um indicador de dívida técnica e pode levar a problemas de compatibilidade e manutenção no futuro.

### Conclusão dos Resultados

A análise do código revela que, embora os elementos básicos sejam reconhecidos, existem falhas estruturais significativas que comprometem a acessibilidade e a usabilidade. Problemas com rótulos duplicados/ausentes e a arquitetura de navegação criam barreiras diretas para usuários de tecnologias assistivas e podem gerar confusão para todos os usuários.

**Recomendação:** Recomenda-se uma refatoração técnica focada em:
1.  Garantir que todos os componentes interativos, especialmente em formulários, tenham rótulos únicos e descritivos.
2.  Corrigir a estrutura de navegação para que todas as telas possuam nomes exclusivos.
3.  Atualizar o código para remover o uso de propriedades depreciadas e seguir as práticas atuais do framework.

## Referências Bibliográficas

> [1] ISO/IEC. ISO/IEC 25010:2011 — Systems and software engineering – Systems and software Quality Requirements and Evaluation (SQuaRE) – System and software quality models. International Organization for Standardization, 2011.

> [2] NIELSEN, Jakob. Mobile Usability. Berkeley: New Riders Pub, 2012.
