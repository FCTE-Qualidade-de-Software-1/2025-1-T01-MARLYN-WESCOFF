# Fase 1: Estabelecer os Requisitos da Avaliação

Nesta fase inicial, são definidos o contexto do projeto, o produto a ser avaliado, o propósito da avaliação e os requisitos de qualidade que servirão como base para as fases subsequentes.

## Objetivo de negócio do AGROMART

O **AgroMart** foi a solução escolhida. Trata-se de uma aplicação que surgiu em 2020 para conectar agricultores familiares e consumidores, como resposta aos desafios da pandemia. O projeto evoluiu para atender também às necessidades de CSAs (Comunidades que Sustentam a Agricultura) e hoje é mantido como um projeto de código aberto pela UnB.

Tem como objetivo aprimorar a conexão entre agricultores familiares e consumidores, promovendo a divulgação eficiente de produtos agroecológicos por meio de uma plataforma digital acessível, com funcionalidades que atendem às necessidades de comunicação, localização e transações.

## Propósito da Avaliação e Melhoria de Qualidade

A avaliação visa garantir a qualidade da aplicação sob a perspectiva do usuário e dos desenvolvedores, considerando um público-alvo com mais de 30 anos e pouca familiaridade tecnológica. O principal propósito da avaliação é:

- Identificar limitações de uso em diferentes dispositivos ou sistemas operacionais.
- Diagnosticar problemas técnicos que dificultam a adaptação do software.
- Certificar de que as boas práticas de qualidade sejam atendidas, conforme a norma ISO/IEC 25010.

## Frameworks de Qualidade e Processo

### Modelo de Qualidade do Produto (Baseado em ISO/IEC 25010 e Q-RAPID)

Para selecionar e priorizar os aspectos de qualidade do **produto AgroMart**, este projeto se baseia nos princípios da norma **ISO/IEC 25010**. O framework **Q-RAPID** (Quality-Requirement-Analysis-and-Prioritization-in-agile-Development) operacionaliza essa norma, propondo um processo para coletar dados de ferramentas de desenvolvimento (como GitLab, Jira, SonarQube) e transformá-los em indicadores de qualidade.

Seguindo essa abordagem, as características de qualidade do AgroMart foram classificadas em uma escala de 1 (nenhum interesse) a 5 (grande interesse):

#### Portabilidade - 5 (Foco Principal)
- A aplicação precisa ser adaptável a diversos ambientes sem mudanças no código-fonte.
- Facilidade com que o software possa ser instalado em diversos ambientes.

#### Usabilidade - 4
- Sistema acessível para usuários com diversas capacidades.
- Facilidade de operar e controlar o sistema.

#### Manutenibilidade - 4
- Capacidade do sistema de ser dividido em componentes independentes.
- Facilidade de diagnosticar defeitos ou entender melhor o sistema.

#### Segurança (Confidencialidade, Integridade, Disponibilidade) - 4
Apesar do foco em Portabilidade, o objetivo de negócio do AgroMart de **"proteger os dados dos agricultores e consumidores"** torna a Segurança um requisito crítico. A análise de segurança considera a tríade:
- **Confidencialidade:** Proteção de dados pessoais e de transações.
- **Integridade:** Exatidão das informações de produtos, preços e estoques.
- **Disponibilidade:** Garantia de que a plataforma esteja online para uso.

#### Confiabilidade - 3 e Compatibilidade - 3
- Grau de funcionamento livre de falhas e capacidade de coexistir com outros sistemas.

### Framework de Medição de Processo (PSM/CID)

Para o **gerenciamento do nosso projeto de avaliação**, utilizaremos o framework **CID (Continuous Iterative Development)**, desenvolvido pelo PSM (Practical Software and Systems Measurement).

**Nota importante:** A sigla CID, neste contexto, refere-se a **Desenvolvimento Contínuo e Iterativo**, um método para gerenciar e medir o **processo** de desenvolvimento e entrega. Isso é diferente da tríade de segurança (Confidencialidade, Integridade, Disponibilidade), que é uma característica de **qualidade do produto**.

O framework CID oferece um conjunto de métricas práticas para avaliar o progresso, a eficiência e a qualidade do trabalho sob três perspectivas:

- **Equipe:** Mede o desempenho e a previsibilidade do time.
- **Produto:** Avalia a qualidade e o valor do que está sendo construído.
- **Empresa:** Analisa o alinhamento com os objetivos estratégicos.

Para o nosso projeto, isso significa que, além de avaliar a qualidade do AgroMart (o produto), devemos usar as métricas do framework CID (como *Burndown*, *Cycle Time* e *Team Velocity*) para monitorar o nosso próprio trabalho (o processo).