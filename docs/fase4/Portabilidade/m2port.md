# Portabilidade - M2: Número de Erros Visuais em Navegadores

## Introdução

A métrica M2, Número de erros visuais encontrados por navegador, continua a avaliação da Portabilidade da aplicação, focando na sua consistência e compatibilidade entre diferentes ambientes de software — especificamente, os navegadores web. Este indicador quantifica o número de discrepâncias visuais (como quebras de layout, estilos não aplicados ou elementos desalinhados) que ocorrem quando a aplicação é renderizada em um navegador em comparação com um navegador de referência.

## Referencial Teórico

Esta avaliação se baseia na sub-característica de **Instalabilidade**, parte da característica de **Portabilidade** da norma **ISO/IEC 25010**. A instalabilidade mede a facilidade com que o software pode ser executado em um ambiente especificado. Se o produto não pode ser executado, a análise de erros visuais é impossibilitada, indicando uma falha crítica de instalabilidade.

## Análise

A metodologia para avaliar esta métrica consistiu em uma tentativa de instalação e execução do projeto em um ambiente de desenvolvimento limpo, seguindo estritamente as instruções fornecidas pela documentação oficial. O objetivo era renderizar a aplicação em pelo menos dois navegadores diferentes (Chrome e Firefox) para a contagem dos erros visuais.

As ferramentas e procedimentos utilizados foram:

* **Ambiente de Desenvolvimento:** Máquina com Node.js v18 e Yarn v1.22.x.
* **Documentação Guia:** O arquivo `README.md` do repositório.
* **Comandos Executados:** `git clone`, `yarn install`, e `yarn web`.

As tarefas selecionadas para análise foram:

* **Tarefa 1:** Configurar o ambiente de desenvolvimento conforme o `README.md`.
* **Tarefa 2:** Iniciar o servidor de desenvolvimento da aplicação web.
* **Tarefa 3:** Acessar a aplicação no Chrome e Firefox para inspecionar visualmente.

A seguir, os resultados desta tentativa.

## Resultados

Durante a execução da Tarefa 2, o processo de build da versão web **falhou com múltiplos erros de compilação**, impedindo que o servidor fosse iniciado. A análise dos erros aponta para dependências desatualizadas e documentação incorreta, como detalhado na análise da métrica de documentação.

Como resultado, a Tarefa 3 não pôde ser executada, e **não foi possível renderizar nenhuma interface** para a contagem de erros visuais. A falha de execução precede qualquer análise visual.

Considerando que a aplicação web não pode ser executada, o número de erros visuais é, na prática, infinito ou não aplicável. A métrica foi classificada com a **pontuação 1 (Crítico)**, pois a portabilidade para a plataforma web está completamente quebrada no nível de execução.

## Referencias Bibliográficas

>  ISO/IEC 25010. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards/iso-25010>. Acesso em: 19 de maio de 2025.