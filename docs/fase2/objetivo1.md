# Objetivo de Medição 1: Usabilidade

<font size="2"><p style="text-align: center">**Tabela 1-** Objetivo de Medição 1: Usabilidade.</p></font>

| Analisar    | o AgroMart | 
| ---- | ------ |
| Para o propósito de | Avaliar se a aplicação é acessível para usuários com necessidades específicas      |
| Com respeito a | Usabilidade       |
| Do ponto de vista da | Equipe de desenvolvimento e usuários finais       |
| No contexto da | Disciplina de Qualidade de Software     |

## Questões Objetivo de Medição 1: Usabilidade

**Perguntas (Questions):**

> Q1: O design foi pensado para ser utilizável por todas as pessoas, independentemente de suas limitações físicas, sensoriais ou cognitivas?
> Hipótese 1:Espera-se que a taxa de sucesso na conclusão de tarefas essenciais por usuários com deficiências (visuais, motoras, etc.) seja de, no mínimo, 85%.

> Q2: Informações importantes não dependem apenas de cor?
> Hipótese 2: Espera-se que 100% dos elementos de feedback (como mensagens de erro/sucesso) utilizem, além da cor, um ícone ou texto explícito para comunicar seu status.

> Q3: Botões, campos e ícones possuem contraste suficiente?
> Hipótese 3: Espera-se que 98% dos elementos de texto e componentes de interface (botões, campos) atendam à taxa de contraste mínima de 4.5:1 (WCAG AA).

> Q4: Todo conteúdo não-textual que transmite informação (como imagens, ícones e gráficos) possui uma alternativa textual equivalente que descreve seu propósito para tecnologias assistivas?
> Hipótese 4: Espera-se que 100% das imagens que comunicam informações relevantes possuam um texto alternativo (alt) preenchido com uma descrição concisa e fiel ao conteúdo da imagem.

> Q5: Botões mudam de cor ou estado ao serem clicados?
> Hipótese 5: Espera-se que 100% dos botões interativos do sistema apresentem uma mudança visual distinta (alteração de cor, sombra ou contorno) no estado :active, ou seja, enquanto estão sendo clicados.


## Relação entre Objetivos de Medição - Questões e Métricas - Objetivo de Medição 1: Usabilidade

<font size="2"><p style="text-align: center">**Figura 1 -** Diagrama de Questões e Métricas para Usabilidade.</p></font>

![Diagrama1](../assets/Diagrama-1.jpg)

## Seleção das Métricas

Com base na abordagem Goal-Question-Metric (GQM), selecionamos as seguintes métricas para a avaliação:

#### Usabilidade

- **M1: Taxa de Sucesso da Tarefa para Usuários com Deficiências**
- **M2: Índice de Conformidade de Feedback Não-Dependente de Cor**
- **M3: Índice de Conformidade de Contraste (WCAG)**
- **M4: Cobertura de Alternativas Textuais em Imagens Informativas**
- **M5: Índice de Conformidade de Feedback de Interação (Estado Ativo)**

## Níveis de Pontuação das Métricas

Para cada métrica definida com a metodologia GQM, foram criados níveis de pontuação que ajudam a interpretar os resultados de forma clara e padronizada. Essa escala facilita a comparação entre métricas e orienta melhor as decisões sobre a qualidade da solução. Os valores foram definidos com base em boas práticas, referências da área e nas expectativas dos usuários.

A tabela abaixo mostra a escala adotada:

| **Desempenho da Métrica** | **Faixa de Valores** | **Interpretação Qualitativa**                                                   |
| ------------------------- | -------------------- | ------------------------------------------------------------------------------- |
| **Excelente**             | 10                   | Atende completamente aos padrões de qualidade esperados.                                 |
| **Bom**                   | 7 - 9                | Funciona bem, com poucos pontos que podem ser melhorados.           |
| **Regular**               | 4 - 6                | 	Tem falhas visíveis, mas ainda pode ser usado de forma aceitável. |
| **Insatisfatório**        | 1 - 3                | Prejudica bastante a experiência ou confiança do usuário.          |

## Critérios de Avaliação

Com os níveis de pontuação definidos, a equipe criou critérios simples para julgar o desempenho da plataforma em dois aspectos principais: usabilidade e confiabilidade. Esses critérios são baseados na média de desempenho das métricas avaliadas.

### Usabilidade

Avalia se o sistema é fácil de usar, entender e navegar.

- Aceitável: ≥ 70% das métricas classificadas como "Bom" ou "Excelente".
- Parcialmente aceitável: Entre 50% e 69% das métricas com nível "Bom" ou superior.
- Inaceitável: < 50% das métricas atingindo "Bom" ou "Excelente".