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


## Protótipo de alta fidelidade

O protótipo foi feito com base nas métricas analisadas e as soluções encontradas. Está disponível no [link](https://www.figma.com/proto/lGOxQeUMYhSZFf3qds5pCK/qsw?page-id=0%3A1&node-id=11-130&p=f&viewport=831%2C336%2C0.42&t=RQrrLJV3Uk0Y5TA6-1&scaling=scale-down&content-scaling=fixed&starting-point-node-id=11%3A130).

<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="450" height="800" src="https://embed.figma.com/proto/lGOxQeUMYhSZFf3qds5pCK/qsw?page-id=0%3A1&node-id=11-130&viewport=717%2C320%2C0.45&scaling=scale-down&content-scaling=fixed&starting-point-node-id=11%3A130&embed-host=share" allowfullscreen></iframe>