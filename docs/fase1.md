# Fase 1: Estabelecer os Requisitos da Avaliação

Nesta fase inicial, são definidos o contexto do projeto, o produto a ser avaliado, o propósito da avaliação e os requisitos de qualidade que servirão como base para as fases subsequentes.

## Contexto do Projeto

Este projeto visa desenvolver a análise crítica e compreensão da equipe, no contexto da disciplina de Qualidade de Software, para que assim possam-se aplicar técnicas e normas necessárias para assegurar a qualidade de produtos e processos de software
desde o começo do seu processo de desenvolvimento. Assim, foi feita uma análise crítica, considerando vários aspectos de qualidade em uma aplicação real.


## Objetivo de negócio do AGROMART

O **AgroMart** foi a solução escolhida. Trata-se de uma aplicação que surgiu em 2020 para conectar agricultores familiares e consumidores, como resposta aos desafios da pandemia. O projeto evoluiu para atender também às necessidades de CSAs (Comunidades que Sustentam a Agricultura) e hoje é mantido como um projeto de código aberto pela UnB.

Tem como objetivo aprimorar a conexão entre agricultores familiares e consumidores, promovendo a divulgação eficiente de produtos agroecológicos por meio de uma plataforma digital acessível, com funcionalidades que atendem às necessidades de comunicação, localização e transações.

## Propósito da Avaliação e Melhoria de Qualidade

A avaliação visa garantir a qualidade da aplicação sob a perspectiva do usuário e dos desenvolvedores, considerando um público-alvo com mais de 30 anos e pouca familiaridade tecnológica. O principal propósito da avaliação é:

- Diagnosticar erros de usabilidade e problemas técnicos que dificultam a adaptação do software.
- Diagnosticar a acessibilidade do software em geral.
- Identificar limitações de uso em diferentes dispositivos ou sistemas operacionais.
- Diagnosticar problemas técnicos que dificultam a adaptação do software.
- Certificar de que as boas práticas de qualidade sejam atendidas, conforme a norma ISO/IEC 25010.

## Conexão com ODS(Objetivo de Desenvolvimento Sustentável) da ONU

- **ODS 2 - Fome Zero e Agricultura Sustentável:** *Acabar com a fome, alcançar a segurança alimentar e melhoria da nutrição e promover a agricultura sustentável.* Ao utilizar recursos digitais para conectar produtores e consumidores, a aplicação impulsiona a modernização da agricultura familiar, otimizando a logística de comercialização e promovendo a digitalização de cadeias produtivas. Dessa forma, contribui para a construção de sistemas alimentares mais inteligentes, eficientes e sustentáveis, além de ampliar o acesso a alimentos de qualidade por meio da tecnologia.

- **ODS 8 - Trabalho Decente e Cresimento Econômico:** *Promover o crescimento econômico sustentado, inclusivo e sustentável, emprego pleno e produtivo e trabalho decente para todas e todos.* Além de impulsionar pequenos produtores, estimular a venda local e geração de renda familiar, o aplicativo abre espaço para inovação de práticas econômicas de forma sustentável e acessível.

- **ODD 9 - Indústria, inovação e infraestrutura:** *Construir infraestruturas resilientes, promover a industrialização inclusiva e sustentável e fomentar a inovação.* A tecnologia implementada é acessível e compatível com a vida do produtor familiar.
 
- **ODS 11 - Cidades e Comunidades Sustentáveis:** *Tornar as cidades e os assentamentos humanos inclusivos, seguros, resilientes e sustentáveis.* Com o objetivo de conectar diferentes produtores familiares e consumidores de forma digital, a aplicação incentiva as relações econômicas entre diferentes áreas, e reforça o planejamento nacional e regional de desenvolvimento.

- **ODS 12 - Consumo e Produção Responsáveis:** *Assegurar padrões de produção e de consumo sustentáveis.* O aplicativo auxilia o produtor a alcançar a gestão sustentável e o uso eficiente dos recursos naturais, evitando assim o desperdício de alimentos.

### Modelo de Qualidade do Produto (Baseado em ISO/IEC 25010)

Além da ISO/IEC 25010, o projeto também adota o framework **PSM/CID (Practical Software and Systems Measurement / Continuous Iterative Development)** para apoiar a avaliação e o monitoramento contínuo do processo de desenvolvimento. O PSM/CID auxilia a monitorar e avaliar continuamente como o processo de desenvolvimento atinge esses padrões.

Seguindo essa a ISO, as características de qualidade do AgroMart foram classificadas em uma escala de 1 (nenhum interesse) a 5 (grande interesse):

#### Usabilidade - 5 (Foco Principal)
- Sistema acessível para usuários com diversas capacidades.
- Facilidade de operar e controlar o sistema.

#### Portabilidade - 4 
- A aplicação precisa ser adaptável a diversos ambientes sem mudanças no código-fonte.
- Comportamento consistente em diversos ambientes.

#### Manutenibilidade - 4
- Capacidade do sistema de ser dividido em componentes independentes.
- Facilidade de diagnosticar defeitos ou entender melhor o sistema.

#### Confiabilidade e Compatibilidade - 3
- Grau de funcionamento livre de falhas e capacidade de coexistir com outros sistemas.

#### Segurança - 2

- **Integridade:** Exatidão das informações de produtos, preços e estoques.

## Framework de Medição de Processo (PSM/CID)

Para o **gerenciamento do nosso projeto de avaliação**, utilizaremos o framework **CID (Continuous Iterative Development)**, desenvolvido pelo PSM (Practical Software and Systems Measurement).

**Nota importante:** A sigla CID, neste contexto, refere-se a **Desenvolvimento Contínuo e Iterativo**, um método para gerenciar e medir o **processo** de desenvolvimento e entrega. Isso é diferente da tríade de segurança (Confidencialidade, Integridade, Disponibilidade), que é uma característica de **qualidade do produto**.

O framework CID oferece um conjunto de métricas práticas para avaliar o progresso, a eficiência e a qualidade do trabalho sob três perspectivas:

- **Equipe:** Mede o desempenho e a previsibilidade do time.
- **Produto:** Avalia a qualidade e o valor do que está sendo construído.
- **Empresa:** Analisa o alinhamento com os objetivos estratégicos.

Para o nosso projeto, isso significa que, além de avaliar a qualidade do AgroMart (o produto), devemos usar as métricas do framework CID (como *Burndown*, *Cycle Time* e *Team Velocity*) para monitorar o nosso próprio trabalho (o processo).

## Bibliografia
> \- ISO/IEC 25000 SQuaRE series Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE). Disponível em: <https://committee.iso.org/sites/jtc1sc7/home/projects/flagship-standards/iso-25000-square-series.html>. Acesso em: 22 de maio de 2025. 
 
> \- ISO/IEC 25010. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards/iso-25010>. Acesso em: 19 de maio de 2025.

> \- Documentação do AgroMart. Disponível em: <https://agromart.github.io/docs/docs/intro>. Acesso em: 29 de maio de 2025.

## Referências Bibliográficas

>  AgroMart. Disponível em: <https://github.com/AgroMart>. Acesso em: 19 de maio de 2025.

>  ISO/IEC 25010. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards/iso-25010>. Acesso em: 19 de maio de 2025.

>  ONU. Objetivos de Desenvolvimento Sustentável. Disponível em: <https://brasil.un.org/pt-br/sdgs>. Acesso em: 19 de maio de 2025.