# Fase 3: Projeto da Avaliação

Nesta fase, é criado o plano de avaliação detalhado, que servirá como um guia para a execução dos testes e a coleta de dados. O plano define os procedimentos, recursos, responsabilidades e o cronograma das atividades.

## 1. Introdução e Objetivos
O objetivo deste plano é projetar as atividades necessárias para avaliar a qualidade do software AgroMart, com foco principal na característica de **Portabilidade**. A avaliação seguirá as métricas especificadas na Fase 2 para garantir a coleta de dados objetivos e consistentes.

## 2. Escopo da Avaliação
- **Produto:** Software AgroMart (Interface Web e Aplicativo Móvel).
- **Características Avaliadas:** O foco principal será em Portabilidade e suas características de apoio como Usabilidade e Confiabilidade em diferentes plataformas.

## 3. Plano de Coleta de Métricas do Produto (AgroMart)

A coleta de dados será realizada seguindo os procedimentos abaixo para cada métrica definida no GQM da Fase 2.

| Métrica | Procedimento de Coleta |
| :--- | :--- |
| **M1: Taxa de sucesso em tarefas** | Realizar um teste de usabilidade com um grupo de 3-5 usuários. Eles executarão um roteiro de tarefas pré-definido (ex: buscar produto, cadastrar loja) no desktop e no mobile. A taxa será calculada como (tarefas concluídas / total de tarefas) * 100. |
| **M2: Índice de responsividade** | Utilizar as ferramentas de desenvolvedor dos navegadores para simular diferentes resoluções de tela. O índice será "Passa" se não houver problemas visuais significativos e "Falha" caso contrário. |
| **M3: Número de erros visuais** | Realizar inspeção visual das principais telas da aplicação em múltiplos navegadores (Chrome, Firefox, Safari, Edge) e contabilizar cada desalinhamento ou elemento quebrado. |
| **M4: % de conformidade visual**| Calcular a conformidade com base nos erros de M3. |
| **M5: Tempo de resposta médio** | Utilizar a aba "Network" das ferramentas de desenvolvedor para medir o tempo de carregamento das 5 principais páginas em desktop e em uma conexão 4G simulada. |
| **M6: Taxa de erro/performance por SO**| Executar testes funcionais em diferentes SOs/Dispositivos e calcular a taxa de falha. |
| **M7: Nº de funcionalidades não disponíveis** | Comparar funcionalmente a interface web com o aplicativo móvel e listar as diferenças. |
| **M8 a M11 (Instalação)**| Simular o processo de instalação em um ambiente limpo, seguindo a documentação, para medir a quantidade de dependências, passos manuais, tempo e erros. |

---

## 4. Plano de Gerenciamento do Projeto (Framework PSM/CID)

Para gerenciar o **nosso próprio projeto de avaliação**, aplicaremos métricas do framework **CID (Continuous Iterative Development)**. O objetivo é monitorar nosso progresso, eficiência e garantir a entrega de um trabalho de qualidade.

### Métricas de Gerenciamento a Serem Adotadas:

- **Committed vs. Completed (Comprometido vs. Concluído):**
  - **O que é:** Mede se a equipe está entregando o que planejou.
  - **Como usaremos:** As quatro fases do trabalho são nossos "work items" comprometidos. Vamos rastrear a data de conclusão de cada fase em relação a um cronograma planejado. Isso nos dará uma medida da nossa previsibilidade.

- **Burndown:**
  - **O que é:** Um gráfico que visualiza o trabalho restante versus o tempo.
  - **Como usaremos:** Utilizaremos as *Issues* e *Milestones* do GitHub para criar um backlog de tarefas para cada fase. O fechamento das issues alimentará um gráfico de burndown, mostrando visualmente se estamos no caminho certo para concluir o projeto no prazo.

- **Cycle Time (Tempo de Ciclo):**
  - **O que é:** O tempo decorrido desde o início de um trabalho até a sua conclusão.
  - **Como usaremos:** Mediremos especificamente o *Cycle Time* da **"ação de melhoria"** obrigatória da Fase 4. O tempo será contado desde o primeiro *commit* de código ou a criação do protótipo até a sua finalização e entrega.

- **Defect Detection & Resolution (Detecção e Resolução de Defeitos):**
  - **O que é:** Mede a capacidade da equipe de encontrar e corrigir seus próprios erros.
  - **Como usaremos:** Qualquer problema ou erro significativo encontrado em nossa própria documentação, planejamento ou código (da ação de melhoria) será registrado como uma *Issue* no GitHub. Mediremos quantos desses "defeitos" são encontrados e o tempo para resolvê-los. O objetivo é ter um processo de auto-correção eficiente.

### Recursos e Cronograma

**Recursos Necessários:**

  - **Humanos:** Membros da equipe do projeto.
  - **Software:** Navegadores, Ferramentas de Desenvolvedor, Git, GitHub.
  - **Hardware:** Computadores com Windows/Linux, dispositivos móveis Android/iOS.

**Cronograma e Responsabilidades:**
A tabela a seguir apresenta a divisão de trabalho e deve ser preenchida pela equipe com os prazos.

| Atividade | Responsável(is) | Prazo de Início | Prazo de Fim |
| :--- | :--- | :--- | :--- |
| Preparação do Ambiente de Teste | Brenno, Igor | | |
| Execução dos Testes de Usabilidade (M1) | Caio, João S. | | |
| Execução dos Testes de Compatibilidade (M2-M7)| João L., Rodrigo | | |
| Execução dos Testes de Instalação (M8-M11)| Caio, Rodrigo | | |
| Análise e Consolidação dos Dados | Todos | | |
| Elaboração do Relatório Final | Todos | | |
| Implementação da Ação de Melhoria | A definir | | |