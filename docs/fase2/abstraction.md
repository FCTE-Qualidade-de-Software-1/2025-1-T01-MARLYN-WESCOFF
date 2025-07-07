**Abstraction Sheet - Objetivo 1**

| Elemento | Descrição |
| --- | --- |
| **Object** | **Software Agromart** — Verificar a compatibilidade multiplataforma do sistema em diferentes ambientes (dispositivos e navegadores). |
| **Purpose** | Avaliar se o software mantém seu funcionamento, aparência e usabilidade de forma consistente em diferentes dispositivos e navegadores. |
| **Quality Focus** | - **Portabilidade**<br>- **Usabilidade multiplataforma**<br>- **Consistência visual e funcional** |
| **Baseline Hypotheses** | - O sistema deve manter sua usabilidade e consistência visual em diferentes dispositivos e navegadores.<br>- Não deve exigir configurações específicas para isso. |
| **Variation Factors** | - Tipo de dispositivo, Navegadores, Resoluções de tela, Sistemas operacionais. |
| **Impact of Variation Factors**| - A interface pode perder usabilidade se não se adaptar a telas menores.<br>- Elementos visuais podem quebrar ou se desalinharem em navegadores diferentes.<br>- Problemas de compatibilidade podem afetar a experiência do usuário. |


**Abstraction Sheet - Objetivo 2**

<table>
  <tr>
    <th>Object</th>
    <th>Purpose</th>
    <th>Quality Focus</th>
    <th>Viewpoint</th>
  </tr>
  <tr>
    <td>AgroMart</td>
    <td>Compreender a facilidade de adaptação e funcionamento do sistema em diferentes ambientes e plataformas.</td>
    <td>Portabilidade</td>
    <td>Equipe de desenvolvimento e usuários finais (agricultores e consumidores)</td>
  </tr>
  <tr>
    <th colspan="2">Quality Focus</th>
    <th colspan="2">Variation Factors</th>
  </tr>
  <tr>
    <td colspan="2">
        <ul>
            <li>Compatibilidade entre diferentes versões do Android  </li>
            <li>Adaptabilidade da interface a diferentes tamanhos de tela e resoluções</li>
            <li>Comportamento consistente em diferentes navegadores e dispositivos</li>
            <li>Independência de recursos específicos de hardware/software</li>
        </ul>
    </td>
    <td colspan="2">
        <ul>
            <li>Variedade de dispositivos Android com diferentes configurações (hardware, resolução, desempenho) </li>
            <li>Conectividade limitada ou intermitente em áreas rurais  </li>
            <li>Níveis variados de alfabetização digital dos usuários (baixo a intermediário)  </li>
            <li>Versões distintas do sistema operacional Android (10, 11, 12...)  </li>
            <li>Navegadores utilizados (Chrome, Firefox, navegadores nativos)</li>
        </ul>
    </td>
  </tr>
    <tr>
    <th colspan="2">Baseline Hypotheses (estimates)</th>
    <th colspan="2">Impact of Variation Factors</th>
  </tr>
  <tr>
    <td colspan="2">
        <ul>
            <li>A aplicação é compatível com ao menos 90% dos dispositivos Android utilizados em campo  </li>
            <li>70% das funcionalidades principais funcionam corretamente em modo offline  </li>
            <li>85% dos usuários conseguem realizar ações básicas sem necessidade de suporte técnico  </li>
            <li>Não há dependência crítica de APIs ou bibliotecas exclusivas de versões mais recentes do Android  </li>
            <li>O comportamento visual permanece estável em pelo menos 95% dos testes entre navegadores diferentes</li>
        </ul>
    </td>
    <td colspan="2">
        <ul>
            <li> Dispositivos de menor desempenho podem apresentar travamentos, falhas de layout ou lentidão perceptível </li> 
            <li> A falta de conectividade pode limitar recursos como atualização de dados em tempo real ou sincronização de pedidos  </li>
            <li> Usuários com menor familiaridade tecnológica podem enfrentar dificuldade para ajustar a interface em dispositivos não otimizados  </li>
            <li> Inconsistências entre versões do Android podem causar falhas visuais ou funcionais em certas ações  </li>
            <li> Navegadores distintos podem renderizar alguns elementos de forma incorreta, impactando a experiência</li>
        </ul>
    </td>
  </tr>
</table>


