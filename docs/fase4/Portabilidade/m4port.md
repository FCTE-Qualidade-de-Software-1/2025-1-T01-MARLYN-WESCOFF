# Portabilidade - M4: Clareza e Completude da Documentação de Instalação

## Introdução

A métrica M4 avalia a qualidade da documentação de instalação, um pilar essencial da portabilidade de qualquer projeto de software. Para um projeto ser verdadeiramente portável, não basta que seu código seja adaptável; ele precisa ser acompanhado de instruções que permitam a outros desenvolvedores "portar" o ambiente de desenvolvimento para suas próprias máquinas de forma eficiente e sem erros. Esta métrica mede o quão clara, completa e precisa é essa documentação.

## Referencial Teórico

Esta métrica avalia o software sob a ótica de múltiplas características de qualidade da norma **ISO/IEC 25010**, tornando-a um indicador robusto. A relação principal é com a **Confiabilidade**, que inclui as sub-características de:
* **Disponibilidade:** O grau em que um sistema está operacional e acessível quando requisitado para uso[cite: 297, 300]. Um aplicativo que não funciona sem internet tem sua disponibilidade severamente limitada.
* **Tolerância a Falhas:** O grau em que um sistema opera como pretendido apesar da presença de falhas de hardware ou software[cite: 297, 299]. A ausência de rede pode ser considerada uma "falha" do ambiente, e o aplicativo ideal deve tolerá-la, mantendo uma funcionalidade mínima.

Adicionalmente, esta métrica também se conecta à **Portabilidade** através da sub-característica de **Adaptabilidade**. Conforme definido na ISO/IEC 25010, um "ambiente de uso" é um dos contextos aos quais um software deve se adaptar[cite: 325, 1492]. Um ambiente sem conectividade é um contexto de uso válido e esperado para o público-alvo do AgroMart, e a capacidade de se adaptar a ele é uma medida direta da portabilidade do aplicativo para cenários do mundo real.

## Análise

A metodologia consistiu em uma tentativa de instalação "do zero" do projeto, realizada por um membro da equipe que simulou ser um novo desenvolvedor sem conhecimento prévio sobre a estrutura do AgroMart. O processo foi guiado estritamente pelas informações contidas no arquivo `README.md`.

As ferramentas e procedimentos utilizados foram:
* **Ambiente de Desenvolvimento Limpo:** Uma máquina virtual recém-configurada para garantir que não houvesse dependências pré-existentes.
* **Documento Guia:** Exclusivamente o arquivo `README.md` encontrado na raiz do repositório do projeto.
* **Registro de Falhas:** Anotação detalhada de cada passo que resultou em erro, cada informação ausente que impediu o progresso e cada configuração que teve de ser "adivinhada".

As tarefas selecionadas para análise foram:
* **Tarefa 1:** Identificar a lista completa de pré-requisitos (software e versões) na documentação.
* **Tarefa 2:** Seguir os passos para configurar as variáveis de ambiente necessárias.
* **Tarefa 3:** Executar os comandos de instalação e inicialização do projeto para a plataforma mobile (Android).

A seguir, serão apresentados os resultados desta tentativa de instalação.

## Resultados

A tentativa de instalar e executar o projeto falhou completamente. A análise da documentação (`README.md`) revelou as seguintes deficiências críticas, conforme identificado previamente:

* **Problema Identificado:** A documentação de instalação está incompleta e desatualizada. Ela não lista todas as dependências necessárias (como uma versão específica do Node.js, Yarn ou a versão para teste do SDK), não explica como configurar as variáveis de ambiente (como `ANDROID_HOME`) e não menciona a necessidade de clonar e rodar múltiplos repositórios, resultando em falha na instalação para novos desenvolvedores.

O resultado prático é que um novo contribuidor é incapaz de configurar um ambiente de desenvolvimento funcional, o que representa uma barreira intransponível para a colaboração e manutenção do projeto. A portabilidade do ambiente de desenvolvimento está severamente comprometida.

Considerando que a documentação atual não cumpre seu propósito fundamental de guiar uma instalação bem-sucedida, a métrica M4 foi classificada com a **pontuação 2 (Muito Ruim)**.

## Referencias Bibliográficas

>  ISO/IEC 25010. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards/iso-25010>. Acesso em: 19 de maio de 2025.