Melhores Práticas do AWS CloudFront
<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/large/2x/aws-cloudfront-logo-png-transparent.png" width="25%">
</div>
<br/>
O AWS CloudFront fornece um serviço de rede de entrega de conteúdo (CDN) que entrega dados, vídeos, aplicativos e APIs globalmente com baixa latência e altas velocidades de transferência. Ele oferece um conjunto de melhores práticas para garantir uma entrega eficiente de conteúdo e alto desempenho.
As melhores práticas do CloudFront são baseadas em áreas-chave: Entrega de Conteúdo, Segurança, Confiabilidade, Otimização de Desempenho, Gerenciamento de Custos e Escalabilidade.

<details><summary><h3>Componentes</h3></summary>
  
#### Entrega de Conteúdo

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/8166/8166342.png" width="25%">
</div>
Entrega de Conteúdo foca na distribuição eficiente de conteúdo para os usuários finais. Este pilar inclui estratégias para otimização de cache, roteamento inteligente de conteúdo e aproveitamento de Localizações de Borda para reduzir a latência e melhorar as velocidades de entrega.

#### Segurança

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/4744/4744315.png" width="25%">
</div>
O pilar de Segurança abrange a proteção de conteúdo e aplicativos servidos através do CloudFront. Inclui a implementação de criptografia, controles de acesso e a prevenção de acesso ou distribuição não autorizada de conteúdo.

#### Confiabilidade

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/12376/12376658.png" width="25%">
</div>
Confiabilidade foca em garantir disponibilidade contínua e desempenho. Este pilar inclui estratégias para tolerância a falhas, balanceamento de carga e configuração do CloudFront para roteamento automático em torno de falhas.

#### Otimização de Desempenho

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/9732/9732828.png" width="25%">
</div>
Otimização de Desempenho visa maximizar as velocidades de entrega de conteúdo e minimizar a latência. Inclui a otimização do comportamento de cache, aproveitamento de técnicas de compressão e utilização de funcionalidades do CloudFront como Lambda@Edge para aceleração de conteúdo dinâmico.
Gerenciamento de Custos
<div align="center">
  <img src="http://cdn-icons-png.flaticon.com/512/6745/6745218.png" width="25%">
</div>
Gerenciamento de Custos envolve otimizar o uso do CloudFront para minimizar despesas. Este pilar inclui estratégias para uso eficiente do cache, seleção de níveis de preços adequados e monitoramento do uso para identificar oportunidades de economia de custos.

#### Escalabilidade

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/3295/3295524.png" width="25%">
</div>
Escalabilidade foca em garantir que o CloudFront possa lidar com demandas crescentes sem degradação de desempenho. Este pilar inclui o design para escalabilidade horizontal, aproveitamento dos serviços da AWS para escalabilidade automática e otimização para picos de tráfego.
</details>
<details><summary><h3>Sub-Recursos</h3></summary>
Sub-Recursos do AWS CloudFront
  
#### 1. Localizações de Borda:
  <div align="center">
    <img src="https://cdn-icons-png.flaticon.com/512/15758/15758526.png" width="25%">
  </div>
Descrição: Localizações de borda são pontos de extremidade do AWS CloudFront usados para armazenar conteúdo em cache mais próximo dos usuários. Elas atendem solicitações de conteúdo e armazenam cópias do seu conteúdo para entrega mais rápida aos usuários.
Funcionalidade: As localizações de borda são distribuídas globalmente e são responsáveis por armazenar em cache o conteúdo, entregar conteúdo aos usuários finais e lidar com várias funcionalidades de CDN, como aceleração de conteúdo dinâmico e terminação SSL.
Importância: As localizações de borda desempenham um papel crucial na redução da latência e melhora do desempenho da entrega de conteúdo, servindo conteúdo em cache de locais mais próximos dos usuários finais.
Exemplo de Caso de Uso: Quando um usuário solicita conteúdo servido pelo CloudFront, a solicitação é roteada para a localização de borda mais próxima, que entrega o conteúdo em cache se disponível, reduzindo o tempo de ida e volta e melhorando a experiência do usuário.
  <div align="center">
    <img src="https://intellipaat.com/blog/wp-content/uploads/2021/07/ACFDC_822X280-1.jpg">
  </div>
  
#### 2. Servidores de Origem:
  <div align="center">
    <img src="https://cdn-icons-png.flaticon.com/512/2920/2920231.png" width="15%">
  </div>
Descrição: Servidores de origem são a fonte do conteúdo que o CloudFront distribui. Eles podem ser um bucket do Amazon S3, uma instância EC2, um Elastic Load Balancer ou um servidor de origem personalizado fora da AWS.
Funcionalidade: Servidores de origem armazenam as versões originais e definitivas do conteúdo que o CloudFront distribui. O CloudFront recupera conteúdo dos servidores de origem sob demanda ou com base em diretivas de controle de cache.
Importância: Servidores de origem são críticos para a entrega de conteúdo, pois fornecem o conteúdo fonte que o CloudFront armazena em cache e distribui para as localizações de borda. Eles também podem gerar conteúdo dinamicamente em resposta às solicitações dos usuários.
Exemplo de Caso de Uso: Um bucket do Amazon S3 que serve conteúdo estático de um site atua como servidor de origem para o CloudFront. Quando um usuário solicita uma página da web, o CloudFront recupera os arquivos correspondentes do bucket S3 e os armazena em cache nas localizações de borda para solicitações subsequentes.

#### 3. Distribuição:
  <div align="center">
      <img src="https://cdn-icons-png.flaticon.com/512/1447/1447098.png" width="20%">
  </div>
Descrição: Uma distribuição representa a configuração e os recursos necessários para distribuir conteúdo com o CloudFront. Especifica os servidores de origem, o comportamento do cache, as configurações de segurança e as configurações de distribuição.
Funcionalidade: Distribuições definem como o conteúdo é entregue através do CloudFront, incluindo quais origens usar, como lidar com cache e entrega de conteúdo, e quaisquer configurações adicionais como configuração de SSL e controle de acesso.
Importância: Distribuições são centrais para a funcionalidade do CloudFront, pois determinam como o conteúdo é armazenado em cache, entregue e protegido. Múltiplas distribuições podem ser criadas para servir diferentes conteúdos ou para aplicar diferentes configurações.
Exemplo de Caso de Uso: Uma distribuição é criada para servir conteúdo estático de um site armazenado em um bucket do Amazon S3. A distribuição especifica o bucket S3 como a origem, define regras de cache para otimizar o desempenho e configura SSL para comunicação segura.

#### 4. Comportamento do Cache:
  <div align="center">
      <img src="https://cdn-icons-png.flaticon.com/512/9872/9872378.png" width="20%">
  </div>
Descrição: Comportamentos de cache definem como o CloudFront lida com solicitações para caminhos ou padrões específicos de conteúdo. Eles determinam se o CloudFront serve conteúdo do cache ou encaminha solicitações para o servidor de origem.
Funcionalidade: Comportamentos de cache permitem controle refinado sobre como o conteúdo é armazenado em cache e entregue com base em padrões de URL, strings de consulta, cabeçalhos ou cookies. Eles especificam o comportamento de cache, TTLs e configurações do servidor de origem.
Importância: Comportamentos de cache permitem otimização da entrega de conteúdo ao ajustar políticas de cache para diferentes tipos de conteúdo ou solicitações de usuários. Eles ajudam a melhorar o desempenho e a reduzir a carga no servidor de origem.
Exemplo de Caso de Uso: Um comportamento de cache é configurado para armazenar em cache todas as imagens (por exemplo, arquivos com extensões .jpg, .png, .gif) por uma hora. Solicitações para arquivos de imagem que correspondem a esse padrão são servidas diretamente do cache do CloudFront, reduzindo a latência e a carga no servidor de origem.
</details>

<details><summary><h3>Quais problemas as Melhores Práticas do AWS CloudFront resolvem?</h3></summary>
<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/4133/4133589.png" width="25%">
</div>  
  
As Melhores Práticas do AWS CloudFront abordam vários desafios na entrega de conteúdo e na distribuição de aplicativos, incluindo:

- Entrega lenta de conteúdo: Oferece técnicas para melhorar as velocidades de entrega de conteúdo e reduzir a latência.
- Vulnerabilidades de segurança: Fornece estratégias para proteger conteúdo e aplicativos contra acesso ou distribuição não autorizados.
- Preocupações com confiabilidade: Oferece mecanismos para garantir disponibilidade contínua e desempenho mesmo durante falhas ou períodos de tráfego intenso.
- Ineficiências de custo: Ajuda na otimização do uso do CloudFront para minimizar despesas e maximizar a eficácia de custos.
- Limitações de escalabilidade: Fornece diretrizes para projetar arquiteturas escaláveis que lidem eficientemente com diferentes níveis de demanda.

</details>

<details><summary><h3>Quais são os benefícios das Melhores Práticas do AWS CloudFront?</h3></summary>
<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/3588/3588592.png" width="25%">
</div>  

Alguns dos principais benefícios das Melhores Práticas do AWS CloudFront incluem:

- Melhoria na entrega de conteúdo: Ao seguir as melhores práticas, são aprimoradas as velocidades de entrega de conteúdo e a confiabilidade.
- Segurança aprimorada: Ajuda na implementação de medidas robustas de segurança para proteger conteúdo e aplicativos.
- Economia de custos: Auxilia na otimização do uso do CloudFront para minimizar despesas e maximizar a eficácia de custos.
- Escalabilidade: Fornece orientações para projetar arquiteturas escaláveis que lidem eficientemente com aumentos na demanda.
- Otimização de desempenho: Oferece estratégias para maximizar as velocidades de entrega de conteúdo e minimizar a latência.

</details>

<details><summary><h3>Como as Melhores Práticas do AWS CloudFront são utilizadas?</h3></summary>
<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/1705/1705312.png" width="25%">
</div>  

As Melhores Práticas do AWS CloudFront são utilizadas na arquitetura, implementação e otimização de soluções de entrega de conteúdo utilizando o CDN CloudFront. Elas servem como guia para configurar distribuições do CloudFront, otimizar o comportamento de cache, aprimorar medidas de segurança e garantir alto desempenho e confiabilidade.

</details>

<details><summary><h3>Quais são os casos típicos de uso para as Melhores Práticas do AWS CloudFront?</h3></summary>
<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/2833/2833807.png" width="25%">
</div>  

Os casos típicos de uso para as Melhores Práticas do AWS CloudFront incluem:

- Distribuição de conteúdo: Otimização da entrega de conteúdo estático e dinâmico, incluindo websites, imagens, vídeos e APIs.
- Aceleração de aplicativos: Aceleração da entrega de aplicações web e APIs para melhorar a experiência do usuário.
- Streaming ao vivo e sob demanda: Entrega de transmissões de vídeo ao vivo e sob demanda com baixa latência e alta confiabilidade.
- Entrega global de websites: Garantia de acesso rápido e confiável a websites e aplicações web para usuários em todo o mundo.
- Entrega segura: Implementação de entrega segura de conteúdo com recursos como HTTPS, identidade de acesso à origem e criptografia de nível de campo.
- Entrega econômica: Otimização do uso do CloudFront para minimizar custos enquanto maximiza desempenho e confiabilidade.

</details>





