Load Balancer para AWS Lambda
  <div align="center">
    <img src="https://coralogix.com/wp-content/uploads/2019/02/Load-balancer-icon.png" width="50%">
  </div>

Um balanceador de carga é um servidor ou um componente crítico que desempenha um papel fundamental na distribuição do tráfego de internet recebido para vários servidores (como instâncias EC2) a jusante. Esse processo otimiza a utilização de recursos, melhora o desempenho do sistema e garante alta disponibilidade, evitando que qualquer servidor único seja sobrecarregado. Os balanceadores de carga atuam como intermediários, gerenciando eficientemente a distribuição de solicitações, melhorando assim a confiabilidade geral e a capacidade de resposta do sistema.
<div align="center">
    <img src="https://thumbs2.imgbox.com/44/00/9bCV1Xo4_t.png">
</div>

O balanceamento de carga é um conceito versátil e pode ser aplicado a vários tipos de recursos além das instâncias EC2. Os balanceadores de carga são comumente usados em diferentes cenários para distribuir o tráfego entre uma variedade de recursos, visando melhorar o desempenho, a confiabilidade e a disponibilidade. Aqui estão alguns exemplos de recursos que podem ser combinados com o balanceamento de carga:
<ul>
    <li><strong>Servidores Web:</strong> Os balanceadores de carga podem distribuir o tráfego web recebido entre vários servidores web para garantir uma utilização eficiente dos recursos e melhorar o tempo de resposta para os usuários.</li>
    <li><strong>Servidores de Aplicativos:</strong> Se a sua aplicação estiver distribuída em vários servidores, um balanceador de carga pode distribuir de forma equitativa as solicitações dos usuários entre eles, evitando que um único servidor se torne um gargalo.</li>
    <li><strong>Servidores de Banco de Dados:</strong> Em alguns casos, o balanceamento de carga pode ser aplicado a servidores de banco de dados para distribuir consultas e transações de banco de dados, ajudando a dimensionar as operações do banco de dados e evitar a sobrecarga em um único servidor de banco de dados.</li>
    <li><strong>Microservices:</strong> Em uma arquitetura de microsserviços, onde uma aplicação é composta por pequenos serviços independentes, o balanceamento de carga pode ser usado para distribuir o tráfego entre os vários microsserviços.</li>
    <li><strong>Serviços de Nuvem:</strong> Além das instâncias EC2, os balanceadores de carga podem ser usados para distribuir o tráfego entre diferentes tipos de serviços de nuvem, como contêineres (por exemplo, clusters Kubernetes), funções serverless ou outras máquinas virtuais.</li>
    <li><strong>Ambientes Híbridos:</strong> O balanceamento de carga pode ser implementado em ambientes híbridos que abrangem tanto data centers locais quanto infraestrutura na nuvem, garantindo uma distribuição equilibrada do tráfego entre recursos diversos.</li>
    <li><strong>Balanceamento de Carga de Servidores Globais (GSLB):</strong> O balanceamento de carga também pode ser empregado em uma escala global, distribuindo o tráfego entre servidores localizados em diferentes regiões geográficas para otimizar o desempenho e fornecer tolerância a falhas.</li>
</ul>
  <details>
    <summary>
      <h3>Recursos</h3>
    </summary>
    <ul>
      <li><b>Distribuição de Tráfego:</b> O balanceamento de carga distribui uniformemente as solicitações recebidas entre várias instâncias, evitando a sobrecarga de qualquer função única.</li>
      <li><b>Escala Aprimorada:</b> O balanceamento de carga facilita a escalabilidade horizontal, permitindo que sua arquitetura serverless lide com cargas de trabalho aumentadas de maneira transparente.</li>
      <li><b>Alta Disponibilidade:</b> Ao distribuir funções em várias zonas de disponibilidade, o balanceamento de carga garante operação contínua mesmo diante de falhas.</li>
      <li><b>Otimização de Custos:</b> O balanceamento de carga eficiente pode ajudar a otimizar custos garantindo a utilização eficaz dos recursos.</li>
      <li><b>Ponto Único:</b> Exponha um único ponto de acesso (DNS) para sua aplicação</li>
      <li><b>Manuseio de Falhas:</b> Lide perfeitamente com falhas de instâncias a jusante</li>
      <li><b>Verificações de Saúde:</b> Realize verificações regulares de saúde em suas instâncias</li>
      <li><b>Segurança:</b> Forneça terminação SSL (HTTPS) para seus sites</li>
     <li><b>Entre Zonas:</b> Alta disponibilidade entre zonas</li>
    </ul>
  </details>
   <details><summary><h3>Componentes e Configuração</h3></summary>
      <details><summary><h4>Por que usar um Elastic Load Balancer?</h4></summary>
       <ul>
          <li>Um ELB (Elastic Load Balancer) é um balanceador de carga gerenciado:
              <ul>
                <li>A AWS garante que ele estará funcionando</li>
                <li>A AWS cuida de atualizações, manutenção, alta disponibilidade</li>
                <li>A AWS fornece apenas algumas opções de configuração</li>
              </ul>
          </li>
          <li>Configurar seu próprio balanceador de carga custa menos, mas exigirá muito mais esforço da sua parte (manutenção, integrações)</li>
          <li>4 tipos de balanceadores de carga oferecidos pela AWS:
              <ul>
                <li>Balanceador de Carga de Aplicativos (apenas HTTP / STTPS) - Camada 7</li>
                <li>Balanceador de Carga de Rede (ultra-alto desempenho, permite TCP) - Camada 4</li>
                <li>Balanceador de Carga de Gateway - Camada 3</li>
                <li>Balanceador de Carga Clássico (aposentado em 2023) - Camada 4 & 7</li>
              </ul>
          </li>
       </ul>
      </details>
      <details><summary><h4>Tipos de Balanceadores de Carga</h4></summary>
        <ul>
           <li>Balanceador de Carga de Aplicativos:
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/40/ab/a5iXGjyz_t.png" width="25%">
               </div>
               <ul>
                 <li>Protocolos HTTP / HTTPS / gRPC (Camada 7)</li>
                 <li>Recursos de Roteamento HTTP</li>
                 <li>A AWS fornece apenas alguns recursos</li>
               </ul>
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/24/70/ait8gdLE_t.png">
               </div>
              <p>Escolha um Balanceador de Carga de Aplicativos quando você precisar de um conjunto flexível de recursos para suas aplicações com tráfego HTTP e HTTPS. Operando no nível da solicitação, os Balanceadores de Carga de Aplicativos fornecem recursos avançados de roteamento e visibilidade voltados para arquiteturas de aplicativos, incluindo microsserviços e contêineres.</p>
              <div align="center">
                 <img src="https://a.b.cdn.console.awsstatic.com/a/v1/5OBQRLTIGHMRUVN5XLKT5XU3JE4K6GTDZFDK5IPNT3GWUZTYJBOQ/2024-01-23T02-33-43_a88821a4018ec38/Static/591e55b0c20360da58ee3eee136b1fc6.svg" width="50%">
               </div>
              <hr/>
           </li>
           <li>Balanceador de Carga de Rede:
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/12/75/GWDh0X03_t.png" width="25%">
               </div>
               <ul>
                 <li>Protocolos TCP / UDP (Camada 4)</li>
                 <li>Alto desempenho, milhões de solicitações por segundo</li>
                 <li>IP estático por meio de IP elástico</li>
               </ul>
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/41/7e/6muve8z5_t.png">
               </div>
               <p>Escolha um Balanceador de Carga de Rede quando você precisar de ultra-alto desempenho, descarregamento TLS em escala, implantação centralizada de certificados, suporte para UDP e endereços IP estáticos para suas aplicações. Operando no nível da conexão, os Balanceadores de Carga de Rede são capazes de lidar com milhões de solicitações por segundo de forma segura, mantendo latências ultra baixas.
               </p>
               <div align="center">
                 <img src="https://a.b.cdn.console.awsstatic.com/a/v1/5OBQRLTIGHMRUVN5XLKT5XU3JE4K6GTDZFDK5IPNT3GWUZTYJBOQ/2024-01-23T02-33-43_a88821a4018ec38/Static/707c56b1d8a250c545ca7e2af0e770d7.svg" width="50%">
               </div>
               <hr/>
           </li>
            <li>Balanceador de Carga de Gateway:
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/b9/aa/ESBhKVPV_t.png" width="25%">
               </div>
               <ul>
                 <li>Protocolo GENEVE em Pacotes IP (Camada 3)</li>
                 <li>Roteamento de Tráfego para Firewalls que você gerencia em Instâncias EC2</li>
                 <li>Deteção de intrusões</li>
               </ul>
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/12/05/GFeWXg40_t.png">
               </div>
              <p>Escolha um Balanceador de Carga de Gateway quando precisar implantar e gerenciar uma frota de appliances virtuais de terceiros que suportam GENEVE. Esses appliances permitem melhorar a segurança, conformidade e controles de políticas.</p>
              <div align="center">
                 <img src="https://a.b.cdn.console.awsstatic.com/a/v1/5OBQRLTIGHMRUVN5XLKT5XU3JE4K6GTDZFDK5IPNT3GWUZTYJBOQ/2024-01-23T02-33-43_a88821a4018ec38/Static/2b583e8904605b0212959d386600bc20.svg" width="50%">
               </div>
           </li>
        </ul>
  </details>

  </details>
  <details>
    <summary>
      <h3>Termos e Conceitos</h3>
    </summary>
    <ul>
      <li><b>Funções:</b> Uma função AWS Lambda é uma unidade de código que é executada em resposta a eventos.</li>
      <li><b>Eventos:</b> Um evento é uma ação que ocorre em um serviço AWS, como upload de arquivo no S3 ou uma solicitação de API do Amazon API Gateway, que pode acionar a execução de uma função Lambda.</li>
      <li><b>Tempo de Execução:</b> O tempo de execução é o ambiente no qual o código da função Lambda é executado.</li>
      <li><b>Camadas:</b> As camadas permitem incluir bibliotecas, frameworks e outros arquivos de dependência em sua função Lambda, mantendo a separação do código de lógica de negócios.</li>
      <li><b>Política de Execução:</b> A política de execução controla as permissões que uma função Lambda tem para acessar outros recursos da AWS.</li>
      <li><b>Alias:</b> Um alias é um ponteiro para uma versão específica de uma função Lambda.</li>
    </ul>
  </details>
  <details>
    <summary>
      <h3>Melhores Práticas</h3>
    </summary>
    <ul>
      <li>Projete funções Lambda para serem pequenas e realizar tarefas específicas.</li>
      <li>Limite o tempo de execução das funções para evitar execuções desnecessárias ou falhas devido a limites de tempo.</li>
      <li>Use variáveis de ambiente para armazenar informações sensíveis, como chaves de API e senhas.</li>
      <li>Gerencie e monitore o registro de funções para solução de problemas e depuração.</li>
      <li>Utilize opções de versionamento e controle de acesso para rastrear e gerenciar alterações nas funções Lambda.</li>
      <li>Configure políticas de controle de acesso para limitar o acesso às funções Lambda e aos recursos que elas utilizam.</li>
      <li>Utilize recursos de monitoramento, como Métricas do CloudWatch e Logs do CloudWatch, para monitorar e analisar o desempenho e a eficiência das funções Lambda.</li>
      <li>Teste e valide funções Lambda antes de implantá-las em produção.</li>
    </ul>
  </details>
