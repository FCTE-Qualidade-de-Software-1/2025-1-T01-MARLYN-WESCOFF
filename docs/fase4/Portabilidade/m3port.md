# Portabilidade - M3: Número de Funções que Funcionam Sem Internet

## Introdução

A métrica M3, Número de funções que funcionam sem internet, explora uma dimensão avançada da Portabilidade: a resiliência e a autonomia da 
aplicação em ambientes de conectividade adversa. Este indicador quantifica o conjunto de funcionalidades que foram projetadas para 
permanecerem operacionais no dispositivo do usuário mesmo quando não há uma conexão ativa com a internet, uma abordagem conhecida como 
"offline-first".

## Referencial Teórico

Esta métrica se alinha a duas características de qualidade da norma **ISO/IEC 25010**. Primariamente, ela avalia a **Adequação Funcional**, especificamente a sua sub-característica de **Completude Funcional**. A completude é o grau em que o conjunto de funções cobre todas as tarefas e objetivos especificados pelo usuário. Do ponto de vista de um usuário da plataforma web, o produto AgroMart é funcionalmente incompleto em comparação com a versão mobile.

Secundariamente, uma grande disparidade funcional impacta a **Portabilidade**. Embora o código possa existir, a portabilidade estratégica do *valor* do produto entre as plataformas falhou. 
## Análise

A metodologia utilizada foi a simulação de um ambiente sem conexão de rede para observar o comportamento do aplicativo e inventariar as funções que permanecem ativas.

As ferramentas e procedimentos utilizados foram:

  - **Android Emulator:** Utilizado para rodar a aplicação.
  - **Modo Avião:** Ativado nas configurações do emulador para cortar todo o acesso à rede.
  - **Inspeção Funcional:** Tentativa de uso das funcionalidades básicas do aplicativo após a perda de conexão.

As tarefas selecionadas para análise foram:

- **Tarefa 1:** Com o aplicativo já tendo sido aberto com internet, ativar o "Modo Avião".
- **Tarefa 2:** Reabrir o aplicativo e observar a tela inicial.
- **Tarefa 3:** Tentar navegar para telas visitadas anteriormente, como a lista de produtores, e interagir com os dados.

A seguir, os resultados desta simulação.

## Resultados

Após a ativação do Modo Avião, o aplicativo AgroMart tornou-se **completamente inoperante**. Na reabertura, ele exibe uma tela de erro genérica ou fica em um estado de carregamento infinito, sem apresentar nenhum conteúdo previamente carregado. Não foi identificado nenhum mecanismo de cache local para exibir informações da última sessão.

O número de funções que funcionam sem internet é **zero**. A ausência total de um modo offline funcional significa que, para um usuário em uma área sem sinal (um cenário plausível para o público-alvo do AgroMart), o aplicativo não tem nenhuma utilidade.

Com base na falha total de operação em modo offline, a métrica M4 foi classificada com a **pontuação 1 (Crítico)**. O aplicativo não possui nenhuma capacidade de operação offline, comprometendo severamente sua utilidade e confiabilidade em cenários de conectividade intermitente ou inexistente.

## Referencias Bibliográficas

>  ISO/IEC 25010. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards/iso-25010>. Acesso em: 19 de maio de 2025.