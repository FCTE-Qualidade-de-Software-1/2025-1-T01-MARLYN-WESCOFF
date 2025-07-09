# Fase 3: Planejamento de avaliação

### **1. Introdução**

Este Plano de Avaliação descreve a abordagem e a metodologia para uma análise criteriosa da qualidade do sistema AgroMart. O documento serve como um roteiro para guiar o processo de análise, assegurando que os aspectos críticos da aplicação, como acessibilidade e portabilidade, sejam avaliados de forma sistemática e estruturada. O objetivo é identificar pontos fortes e áreas de melhoria com base em evidências, utilizando métricas, critérios e níveis de pontuação previamente definidos.

### **2. Objetivo da Avaliação**

Conforme os artefatos de medição, o objetivo desta avaliação é duplo:

* **Analisar** o AgroMart com o propósito de **avaliar se a aplicação é acessível para usuários com necessidades específicas**.
* **Analisar** o AgroMart com o propósito de **avaliar o comportamento do aplicativo em diferentes ambientes** para melhorar a experiência do usuário.

A avaliação será conduzida sob o ponto de vista da **equipe de desenvolvimento**.

### **3. Escopo da Avaliação**

A avaliação abrangerá as seguintes áreas do sistema AgroMart:

* **Usabilidade e Acessibilidade:** Foco na legibilidade, navegação, contraste de cores, alternativas textuais e suporte a tecnologias assistivas.
* **Portabilidade:** Responsividade da interface em diferentes dispositivos (desktop e mobile) e consistência visual entre navegadores.

### **4. Método de Avaliação**

A avaliação será realizada pela própria equipe de desenvolvimento por meio de testes internos de usabilidade, acessibilidade e portabilidade, simulando cenários reais de uso. A metodologia combina os seguintes pontos:

* **Testes de Tarefas:** Os membros da equipe executarão tarefas comuns (ex: navegar entre telas) para medir a eficácia e eficiência.
* **Análise Observacional:** Durante os testes, serão coletados dados quantitativos (tempo para concluir tarefas, erros) e qualitativos (comentários, dificuldades encontradas).
* **Testes de Acessibilidade:** Serão utilizadas ferramentas de acessibilidade para verificar a navegabilidade e a compreensão da interface por meio de leitores de tela, focando em alternativas textuais e feedback não visual.
* **Testes de Portabilidade:** A aplicação será testada em diferentes dispositivos (computador pessoal e celular) e em, no mínimo, dois navegadores distintos (ex: Chrome, Firefox) para verificar a consistência do layout e a responsividade.

### **5. Métricas a Serem Avaliadas**

Com base na abordagem GQM dos documentos de objetivo, as seguintes métricas serão avaliadas:

**Usabilidade (Foco em Acessibilidade):**

- **M1:** Taxa de Sucesso da Tarefa utilizando ferramentas de acessibilidade
- **M2:** Índice de Conformidade de Feedback Não-Dependente de Cor
- **M3:** Índice de Conformidade de Contraste 
- **M4:** Cobertura de Alternativas Textuais em Imagens Informativas
- **M5:** Índice de Conformidade de Feedback de Interação (Estado Ativo)
- **M6:** Cobertura de navegação por teclado
- **M7:** Análise do código

**Portabilidade:**

* **M1:** Índice de responsividade, avaliando a adaptação da interface em dispositivos mobile e desktop.
* **M2:** Número de erros visuais encontrados por navegador.
- **M3:** Número de funções que funcionam sem internet
- **M4:** Clareza e Completude da Documentação de Instalação

### **6. Recursos Necessários**

* **Materiais de Apoio:**
    * Documentos de Objetivos do projeto para guiar a aplicação das métricas.
    * Documentação do Agromart.
    * WCAG 2.2.
    * ABNT NBR 17225.
* **Ferramentas Técnicas:**
    * Dispositivos de teste: computador pessoal e celular.
    * Navegadores distintos (ex: Google Chrome, Mozilla Firefox).
    * Cronômetro digital para medição de tempo das tarefas.
    * Ferramenta de verificação de acessibilidade **TalkBack (Android)** e **Acessibility Scanner**.
    * Ferramenta de captura de tela para documentar evidências.

### **7. Critérios de Julgamento**

Os resultados serão interpretados com base nos critérios de avaliação:

* **Usabilidade/Acessibilidade:**
    * **Conforme / Aceitável:** Todas as métricas de acessibilidade (M1, M2, M3) devem atingir uma pontuação "Bom" ou "Excelente".
    * **Não Conforme / Inaceitável:** Se pelo menos uma métrica de acessibilidade receber a pontuação "Insatisfatório", indicando uma falha crítica que impede o uso por um grupo de usuários.
* **Portabilidade:**
    * **Aceitável:** 70% ou mais das métricas de portabilidade (M4, M5) classificadas como "Bom" ou "Excelente".
    * **Inaceitável:** Menos de 50% das métricas de portabilidade atingindo o nível "Bom" ou "Excelente".


## Referências Bibliográficas

> WCAG 2.2 Understanding Docs. SC 1.4.1 Use of Color (Level A). Disponível em: <https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html>. Acesso em 7 de julho de 2025.

> ABNT NBR 17225:2025, Acessibilidade em conteúdo e aplicações web – Requisitos. Disponível em: <https://mwpt.com.br/wp-content/uploads/2025/04/ABNT-NBR-17225-Acessibilidade-Digital.pdf>. Acesso em 7 de julho de 2025.

### Histórico de Versão

| Versão | Data       | Descrição                                                                              | Autor               |
| :----- | :--------- | :------------------------------------------------------------------------------------- | :------------------ |
| 1.0    | 07/07/2025 | Criação do documento de planejamento de avaliação com base nos objetivos de Usabilidade e Portabilidade. | Caio Sabino |