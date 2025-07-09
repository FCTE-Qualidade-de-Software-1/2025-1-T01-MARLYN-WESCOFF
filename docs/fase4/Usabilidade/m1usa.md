# Usabilidade - M1: Taxa de Sucesso da Tarefa utilizando ferramentas de acessibilidade

## Introdução

 A métrica M1, Taxa de Sucesso da Tarefa (Task Success Rate - TSR), é um indicador fundamental para avaliar a usabilidade real e funcional 
 de uma plataforma sob a perspectiva da acessibilidade. Enquanto outras métricas podem focar em conformidade técnica, a M1 mede, 
 quantitativamente, a porcentagem de usuários que conseguem completar uma tarefa predefinida com sucesso, validando a eficácia do sistema no 
 mundo real.

## Referencial teórico 

A principal base para a definição de usabilidade vem da norma ISO 9241-11:2018 (Ergonomia da interação humano-sistema). Este padrão internacional define usabilidade como "a medida na qual um produto pode ser usado por usuários específicos para alcançar objetivos específicos com eficácia, eficiência e satisfação em um contexto de uso específico". A Métrica M1, Taxa de Sucesso da Tarefa (TSR), está diretamente ligada ao pilar da eficácia.

## Análise

Para a análise deste tópico, foi utilizada a ferramenta de acessibilidade **"Acessibility Scanner"**, fornecida pelo Google para plataformas Android. O objetivo foi simular a experiência de um usuário que depende de tecnologias assistivas e verificar, de forma prática, a eficácia do sistema na conclusão de tarefas essenciais.

A metodologia consistiu em executar um conjunto de tarefas predefinidas, que representam os fluxos mais críticos da aplicação, enquanto o **Acessibility Scanner** estava ativo. A ferramenta identifica e sugere melhorias em tempo real para diversos elementos da interface, como:

* **Rótulos de conteúdo:** Verifica se ícones e botões possuem descrições textuais claras para leitores de tela.
* **Área de toque:** Garante que elementos interativos tenham um tamanho adequado para usuários com dificuldades motoras.
* **Contraste de itens:** Analisa se o contraste entre texto, imagens e o fundo atende aos requisitos mínimos, beneficiando usuários com baixa visão.

O sucesso na tarefa foi considerado quando o usuário conseguia completar o fluxo do início ao fim sem encontrar barreiras de acessibilidade que o impedissem de prosseguir, mesmo que a ferramenta apontasse sugestões de melhoria que não bloqueavam a ação.

As tarefas selecionadas para análise foram:

* **Tarefa 1:** *[Descreva aqui a primeira tarefa. Ex: Realizar o login na aplicação utilizando as credenciais salvas.]*
* **Tarefa 2:** *[Descreva aqui a segunda tarefa. Ex: Navegar até a seção de produtos e adicionar um item ao carrinho de compras.]*
* **Tarefa 3:** *[Descreva aqui a terceira tarefa. Ex: Acessar o perfil do usuário e editar o endereço de entrega.]*

A seguir, serão apresentados os resultados detalhados da execução de cada uma dessas tarefas, documentando os pontos de sucesso e as barreiras encontradas.

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