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