# Relatório final de Avaliação - Proposta de melhoria


## Introdução

Este relatório tem como objetivo expor as considerações finais atingidas pelo grupo, após a análise do aplcativo Agromart. Neste tópico, será abordada uma análise geral da avaliação e propostas de melhoria, envolvendo protótipos de alta fidelidade e mudanças técnicas.

Todo o processo foi seguido de acordo com:

- A norma ISO/IEC 25000(SQuaRE).
- ISO/IEC 25010.
- GQM(Goal-Question-Metric) para guiar o formato da avaliação.
- Framework de gestão de projeto PSM/CID.

A seguir, serão abordadas todas as métricas utilizadas na avaliação do projeto e suas soluções.

## Usabilidade

### M1: Taxa de Sucesso da Tarefa utilizando ferramentas de acessibilidade

#### Problema Identificado
A taxa de sucesso para completar o fluxo de "buscar um produto" utilizando leitores de tela foi de apenas 20%. A análise revelou que os botões de filtro e as imagens dos produtos não possuíam descrições textuais, impedindo que os usuários da ferramenta entendessem como prosseguir.

#### Proposta de Melhoria
Mapear e adicionar descrições textuais claras e concisas (alternativas textuais) para todos os elementos interativos e imagens informativas do aplicativo, garantindo que a função de cada componente seja compreensível via áudio.

#### Implementação no Protótipo
O protótipo de alta fidelidade foi atualizado com uma camada de anotações de acessibilidade. Cada componente clicável agora possui sua descrição textual especificada, servindo como um guia claro para a equipe de desenvolvimento.

#### Solução Proposta
Implementar a propriedade `contentDescription` (ou equivalente) em todos os componentes interativos e visuais relevantes. Por exemplo, um botão com ícone de lupa terá a descrição "Buscar produtos", e a imagem de um tomate terá a descrição "Tomate Orgânico".

---

### M2: Índice de Conformidade de Feedback Não-Dependente de Cor

#### Problema Identificado
O aplicativo utiliza exclusivamente a cor vermelha para indicar erros em campos de formulário, como um e-mail inválido. Isso torna o feedback inacessível para usuários com daltonismo, que podem não perceber a indicação de erro.

#### Proposta de Melhoria
Complementar todo feedback baseado em cor com o uso de ícones e mensagens de texto explícitas, garantindo que a informação seja transmitida por múltiplos canais sensoriais.

#### Implementação no Protótipo
Os estados de "Erro" e "Sucesso" dos campos de formulário foram redesenhados. O novo protótipo mostra que, além da cor, um ícone de alerta e um texto auxiliar ("E-mail inválido") devem aparecer junto ao campo.

#### Solução Proposta
Implementar um sistema de feedback multicanal onde mudanças de estado são indicadas por uma combinação de cor, ícones (ex: "X" para erro, "✓" para sucesso) e mensagens de texto explícitas, garantindo redundância.

---

### M3: Índice de Conformidade de Contraste

#### Problema Identificado
A análise com ferramentas de verificação apontou que 40% dos textos do aplicativo, principalmente os textos secundários e placeholders, não atingem o nível de contraste mínimo (4.5:1) recomendado pela WCAG, dificultando a leitura.

#### Proposta de Melhoria
Revisar e ajustar a paleta de cores do aplicativo para garantir que todas as combinações de texto e fundo atendam ao mínimo de 4.5:1 de contraste.

#### Implementação no Protótipo
A paleta de cores no protótipo de alta fidelidade foi validada usando um plugin de contraste. As cores foram ajustadas e agora todos os novos designs seguem a paleta acessível, prevenindo novos problemas.

#### Solução Proposta
Refatorar os estilos do aplicativo para usar uma paleta de cores centralizada e acessível, garantindo que todo texto sobre fundo cumpra os critérios de contraste da WCAG 2.2 nível AA.

---

### M4: Cobertura de Alternativas Textuais em Imagens Informativas

#### Problema Identificado
Constatou-se que 60% das imagens que transmitem informações, como os banners de promoções na tela inicial, não possuem descrições textuais. Como resultado, usuários dependentes de leitores de tela não recebem a informação da promoção.

#### Proposta de Melhoria
Realizar uma auditoria completa de todos os recursos visuais do app e implementar alternativas textuais para todas as imagens que não são puramente decorativas.

#### Implementação no Protótipo
O protótipo inclui, na documentação de cada tela, uma tabela que especifica o texto alternativo para cada imagem informativa, garantindo que essa informação não se perca na passagem para o desenvolvimento.

#### Solução Proposta
Implementar a propriedade `contentDescription` em todas as imagens informativas com textos descritivos e objetivos. Imagens que são puramente estéticas ou decorativas receberão uma descrição nula (`android:contentDescription="@null"`) para que sejam corretamente ignoradas pelos leitores de tela.

---

### M5: Índice de Conformidade de Feedback de Interação (Estado Ativo)

#### Problema Identificado
Ao navegar pelo aplicativo via teclado ou ao tocar em abas e botões, não há uma indicação visual clara de qual elemento está "focado" ou "pressionado". Isso gera incerteza e pode levar o usuário a se perder na navegação.

#### Proposta de Melhoria
Implementar indicadores visuais distintos para os estados de "foco", "pressionado" e "ativo" em todos os componentes interativos.

#### Implementação no Protótipo
O Design System no protótipo foi expandido para incluir variantes para cada estado dos componentes. Por exemplo, um botão agora tem variantes visuais para "Default", "Hover", "Pressed" e, mais importante, **"Focused"**.

#### Solução Proposta
Adotar o uso de `StateListDrawables` ou `RippleDrawable` no Android para que todos os botões e itens de lista respondam visualmente ao toque. Além disso, garantir que a navegação por teclado exiba um anel de foco visível.

---

### M6: Cobertura de navegação por teclado

#### Problema Identificado
Testes revelaram que é impossível completar o fluxo de cadastro de um novo endereço usando apenas o teclado. O foco fica preso no segundo campo de texto e não avança para os botões de "Salvar" ou "Cancelar".

#### Proposta de Melhoria
Garantir que todos os elementos interativos sejam focáveis e que a ordem de navegação (via "Tab") seja lógica e previsível.

#### Implementação no Protótipo
Usando plugins de prototipação, a ordem da navegação por "Tab" foi desenhada e testada. O fluxo de foco agora segue uma ordem lógica e previsível, e esta especificação foi entregue aos desenvolvedores.

#### Solução Proposta
Revisar a hierarquia dos layouts XML e usar atributos como `android:nextFocusForward` para guiar a ordem da navegação. Componentes customizados serão tornados focáveis (`android:focusable="true"`) e terão tratamento para eventos de teclado.

---

### M7: Análise do código

#### Problema Identificado
A análise estática do código-fonte revelou uma alta concentração de "hardcoded strings" (textos fixos no código em vez de em arquivos de recursos), dificultando a tradução e a manutenção. Além disso, a complexidade de algumas classes está acima do recomendado, aumentando a dívida técnica.

#### Proposta de Melhoria
Refatorar os componentes mais complexos, extrair strings e dimensões para arquivos de recursos, e criar um guia de estilo para o desenvolvimento.

#### Solução Proposta
Estabelecer e documentar um guia de estilo de código para a equipe. Integrar uma ferramenta de análise estática (Lint) no processo de Integração Contínua (CI), configurando-a para falhar um build caso novas "hardcoded strings" ou violações de complexidade sejam adicionadas, prevenindo o aumento da dívida técnica.


## Portabilidade

### M1: Índice de responsividade

#### Problema Identificado
A análise da responsividade no dispositivo móvel revelou duas falhas críticas que afetam diretamente a usabilidade e acessibilidade:

1.  **Rotação de Tela Bloqueada:** O aplicativo está travado no modo retrato (em pé) e não se adapta quando o celular é girado para o modo paisagem (deitado).
2.  **Perda de Informação no Zoom:** Ao tentar usar o gesto de pinça para ampliar o conteúdo, partes do texto e botões são cortados ou empurrados para fora da tela, tornando a informação ilegível e inacessível.

#### Proposta de Melhoria
Habilitar a rotação de tela e desenvolver um layout adaptativo para o modo paisagem. Simultaneamente, garantir que todo o conteúdo textual seja escalável e se reorganize (reflow) de forma inteligente para caber na tela após o zoom.

#### Implementação no Protótipo
O protótipo de alta fidelidade foi atualizado para demonstrar as soluções:`

1.  **Layout Paisagem:** Foram criadas variantes para as telas principais, mostrando como os componentes se reorganizam no modo paisagem.
2.  **Simulação de Zoom:** O protótipo agora simula o comportamento de "reflow". Ao aplicar um gesto de zoom, a fonte aumenta de tamanho e as quebras de linha são ajustadas dinamicamente.

#### Solução Proposta

##### **Arquivo a Modificar (Configuração):** `app.json`

Para habilitar a rotação de tela, a configuração de orientação no arquivo `app.json` deve ser alterada para `default`, permitindo que o aplicativo se adapte a ambas as orientações.

```json

{
  "expo": {
    "name": "AgroMart",
    "slug": "AgroMart",
    "version": "1.0.0",
    "orientation": "default",
    "icon": "./assets/icon.png"
  }
}
```

Uso do hook useWindowDimensions é padrão para layouts que se adaptam à orientação, é necessário aplicar em cada componente de tela. A seguir, um exemplo de aplicação desse hook:

```javascript

import { View, Text, useWindowDimensions, StyleSheet } from 'react-native';

export default function HomeScreen() {
  // Pega a largura e altura da tela em tempo real
  const { width, height } = useWindowDimensions();
  // Verifica se está em modo paisagem
  const isLandscape = width > height;

  return (
    // Aplica um estilo de container diferente para cada orientação
    <View style={isLandscape ? styles.containerLandscape : styles.containerPortrait}>
      <Text style={styles.title}>
        {isLandscape ? 'Bem-vindo (Paisagem)' : 'Bem-vindo (Retrato)'}
      </Text>
      {/* ...demais componentes com estilos condicionais... */}
    </View>
  );
}

const styles = StyleSheet.create({
  containerPortrait: {
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center',
  },
  containerLandscape: {
    flex: 1,
    flexDirection: 'row',
    alignItems: 'center',
    justifyContent: 'space-around',
  },
  title: {
    fontSize: 24,
  },
});

```

### M2: Número de erros visuais em navegadores

#### Problema Identificado
A análise revelou uma falha crítica de portabilidade: **a versão web do AgroMart não pôde ser executada**. Ao seguir os passos da documentação e tentar iniciar o servidor web com o comando apropriado, o processo falha, mesmo após a instalação de todas as dependências listadas. Isso impede completamente a verificação de qualquer funcionalidade ou erro visual na plataforma web. A investigação aponta para duas causas prováveis, dado que o repositório não é atualizado há três anos:

1.  **Documentação Desatualizada:** As instruções no `README.md` podem não refletir mais os comandos ou as configurações necessárias para iniciar o projeto com as versões atuais das ferramentas (Node.js, Expo, etc.).
2.  **Dependências Incompatíveis:** As versões das bibliotecas listadas no `package.json` estão obsoletas e provavelmente geram conflitos com o ambiente de desenvolvimento moderno.

#### Proposta de Melhoria
Realizar uma auditoria completa das dependências do projeto e reescrever a documentação de instalação e execução para a plataforma web. O objetivo é criar um guia claro e funcional que permita a um desenvolvedor executar a versão web do projeto com sucesso e sem erros.

#### Mudanças sugeridas

1.  Um arquivo `README.md` atualizado com instruções corrigidas e detalhadas.
2.  Um `package.json` revisado, com as versões das dependências ajustadas para garantir a compatibilidade.

#### Solução Proposta
A solução é dividida em duas frentes de trabalho técnico para restaurar a portabilidade do ambiente de desenvolvimento web:

1.  **Auditoria e Atualização de Dependências:**

    * **Análise:** Utilizar ferramentas como `npm-check-updates` para identificar todas as dependências severamente desatualizadas no arquivo `package.json`.
    * **Ação:** Atualizar cuidadosamente as dependências principais relacionadas à web, como `react-native-web`, `react-dom` e `@expo/webpack-config`, para as versões estáveis mais recentes que sejam compatíveis entre si. O objetivo não é necessariamente usar a versão mais nova de tudo, mas sim uma combinação que funcione.
    * **Validação:** Após a atualização, rodar `yarn install` (ou `npm install`) para garantir que todas as dependências sejam instaladas sem conflitos.

2.  **Revisão e Correção da Documentação (`README.md`):**

    * **Análise:** Revisar a seção "Executando o Projeto" do `README.md` e compará-la com os comandos que de fato funcionam após a atualização das dependências.
    * **Ação:** Reescrever as instruções, tornando-as mais explícitas. Por exemplo, garantir que o comando para instalar as dependências web esteja claro.


---

### M3: Número de funções que funcionam sem internet

#### Problema Identificado
O aplicativo AgroMart depende 100% de uma conexão ativa com a internet. Se o usuário estiver em uma área rural com sinal fraco ou inexistente, o aplicativo não exibe nenhuma informação, nem mesmo os dados que foram visualizados na última sessão, mostrando apenas uma tela de erro ou de carregamento infinito.

#### Proposta de Melhoria
Implementar uma estratégia de cache local para que o aplicativo ofereça um modo offline funcional. O app deve salvar os últimos dados carregados (ex: lista de produtores, detalhes de produtos vistos) e exibi-los quando o usuário estiver sem conexão.


#### Solução Proposta
Utilizar uma biblioteca de armazenamento local como o **AsyncStorage** (para React Native) para salvar os dados recebidos da API. Antes de fazer uma chamada de rede, verificar se há conexão. Se não houver, carregar e exibir os dados salvos localmente, informando ao usuário que a informação pode não ser a mais recente.

---

### M4: Clareza e Completude da Documentação de Instalação

#### Problema Identificado
A documentação de instalação (`README.md`) está incompleta e desatualizada. Ela não lista todas as dependências necessárias (como uma versão específica do Node.js, Yarn ou a versão para teste do SDK), não explica como configurar as variáveis de ambiente e não menciona a necessidade de rodar múltiplos repositórios, resultando em falha na instalação para novos desenvolvedores.

#### Proposta de Melhoria
Reescrever completamente a documentação de instalação, criando um guia passo a passo claro, com seções dedicadas para pré-requisitos, configuração de ambiente e comandos de execução para cada plataforma (mobile e web).


#### Solução Proposta
Estruturar o novo `README.md` da seguinte forma:

1.  **Pré-requisitos:** Lista de softwares e versões necessárias (ex: Node.js v18+, Yarn v1.22+, Android Studio).
2.  **Configuração do Ambiente:** Instruções claras sobre como configurar variáveis de ambiente como `ANDROID_HOME`.
3.  **Instalação Passo a Passo:** Uma sequência numerada de comandos a serem executados (`git clone`, `yarn install`, etc.).
4.  **Executando o Projeto:** Comandos separados e claros para rodar em Android, iOS e Web (`yarn android`, `yarn web`).
5.  **Troubleshooting:** Uma seção com erros comuns e suas soluções.

## Bibliografia 

>  Basili, V. R., Caldiera, G., & Rombach, H. D. (1994). The Goal Question Metric Approach. In *Encyclopedia of Software Engineering*. John Wiley & Sons.

## Referências Bibliográficas
  

>  Practical Software and Systems Measurement (PSM). Department of Defense, 2003. Disponível em: <https://www.psmsc.com/>. Acesso em: 08 de julho de 2025.

>  ISO/IEC 25010. Disponível em: <https://iso25000.com/index.php/en/iso-25000-standards/iso-25010>. Acesso em: 19 de maio de 2025.

> \- ISO/IEC 25000 SQuaRE series Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE). Disponível em: <https://committee.iso.org/sites/jtc1sc7/home/projects/flagship-standards/iso-25000-square-series.html>. Acesso em: 22 de maio de 2025. 

>  AgroMart. Disponível em: <https://github.com/AgroMart>. Acesso em: 19 de maio de 2025.

>  Diretrizes de Acessibilidade para Conteúdo Web (WCAG) 2.2 . Michael Cooper; Andrew Kirkpatrick; Joshue O’Connor; Alastair Campbell. W3C. 12 de dezembro de 2024. Recomendação do W3C. Disponível em: <https://www.w3.org/TR/WCAG22/>. Acesso em 23 de junho de 2025.