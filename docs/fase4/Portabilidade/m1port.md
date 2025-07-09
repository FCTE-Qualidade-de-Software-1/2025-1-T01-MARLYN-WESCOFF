# Portabilidade - M1: Índice de Responsividade

## Introdução

A métrica M1, Índice de Responsividade, é o principal indicador para avaliar a Portabilidade de uma aplicação web no que tange à sua 
adaptabilidade a diferentes ambientes de visualização. Este índice mede a capacidade da interface de se ajustar de forma fluida e funcional 
a uma ampla gama de tamanhos de tela e resoluções, desde pequenos dispositivos móveis até monitores de desktop de alta resolução.

## Referencial Teórico

A base para esta métrica vem da norma **ISO/IEC 25010**, que define a **Portabilidade** como uma característica de qualidade. Especificamente, a M1 está ligada à sub-característica de **Adaptabilidade**, que é a capacidade do produto de ser utilizado de forma eficaz em diferentes ambientes de hardware, software ou de uso. Um aplicativo que não se adapta à rotação ou ao zoom falha neste quesito.

## Análise

Para a análise deste tópico, foi utilizado o **Android Emulator** para simular um ambiente de dispositivo móvel e suas funcionalidades nativas. A metodologia consistiu em executar um conjunto de tarefas que exploram a adaptabilidade da interface em tempo real.

As ferramentas e procedimentos utilizados foram:

* **Controle de Rotação do Emulador:** Para alternar a visualização entre os modos retrato e paisagem.
* **Gestos de Magnificação do Android:** Para simular o gesto de pinça para zoom, ativado nas configurações de Acessibilidade do sistema.
* **Inspeção Visual:** Observação direta do comportamento da interface durante a execução das tarefas.

As tarefas selecionadas para análise foram:

* **Tarefa 1:** Abrir a tela inicial e rotacionar o dispositivo para o modo paisagem, observando a reorganização dos componentes.
* **Tarefa 2:** Acessar a tela de detalhes de um produtor, que contém blocos de texto longos.
* **Tarefa 3:** Na tela de detalhes, ativar o zoom de magnificação e tentar ler a descrição completa do produtor.

A seguir, serão apresentados os resultados detalhados da execução de cada uma dessas tarefas.

## Resultados

A partir da execução das tarefas, observou-se que o aplicativo apresenta falhas críticas de responsividade. Primeiramente, a **rotação de tela está completamente bloqueada**, impedindo a execução da Tarefa 1. A aplicação força o usuário a permanecer no modo retrato.

Na Tarefa 3, ao tentar utilizar o zoom, o problema se manifestou de forma severa: o conteúdo textual e os botões foram **cortados e empurrados para fora da área visível**, sem a possibilidade de rolagem horizontal para acessá-los. Isso torna a funcionalidade de zoom inutilizável e prejudica massivamente a acessibilidade.

Dessa forma, considerando que a funcionalidade é severamente comprometida em contextos de uso comuns, a métrica M1 foi classificada com a **pontuação 2 (Muito Ruim)**. A aplicação falha em se adaptar, tornando partes de sua interface inutilizáveis sob certas condições.

## Referencias Bibliográficas

>  ISO/IEC 25010. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards/iso-25010>. Acesso em: 19 de maio de 2025.