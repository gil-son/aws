EC2

<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/large/2x/aws-ec2-logo-svg-vector.svg" width="25%">
</div>

O Amazon EC2 (Elastic Compute Cloud) é um serviço de computação em nuvem que fornece capacidade de computação escalável na nuvem da Amazon. Ele permite que você configure e execute facilmente servidores virtuais na nuvem da Amazon, chamados de instâncias EC2. Com o Amazon EC2, você pode dimensionar verticalmente ou horizontalmente sua capacidade de computação de acordo com as necessidades da sua aplicação, pagando apenas pelos recursos que você usa.

EC2 = Elastic Compute Cloud = Infraestrutura como Serviço

Principalmente, consiste na capacidade de:
<ul>
    <li>Alugar máquinas virtuais (EC2).</li>
    <li>Armazenar dados em discos virtuais (EBS).</li>
    <li>Distribuir carga entre máquinas (ELB).</li>
    <li>Escalonar os serviços usando um grupo de autoescalonamento (ASG).</li>
</ul>

<details><summary> <h3>Recursos</h3></summary>
<ul>
    <li><b>Elasticidade:</b> O EC2 permite escalar verticalmente ou horizontalmente a capacidade de computação de acordo com as necessidades da sua aplicação.</li>
    <li><b>Flexibilidade:</b> O EC2 oferece uma ampla seleção de tipos de instância, sistemas operacionais, bancos de dados e outras opções de software para você escolher.</li>
    <li><b>Integração com outros serviços AWS:</b> O EC2 pode ser facilmente integrado com outros serviços AWS, como o Amazon S3, Elastic Load Balancing, Amazon RDS e outros.</li>
    <li><b>Segurança:</b> O EC2 oferece recursos avançados de segurança, como isolamento de instância, criptografia de dados, autenticação de usuário e muito mais.</li>
    <li><b>Gerenciamento:</b> O EC2 permite que você gerencie facilmente suas instâncias, com recursos como o Amazon EC2 Auto Scaling e o Amazon EC2 Systems Manager.</li>
</ul> 
</details>

<details><summary> <h3>Termos e conceitos</h3></summary>
<ul>
<li><b>Opções de Dimensionamento e Configurações:</b> As instâncias EC2 são servidores virtuais configuráveis que você pode iniciar na nuvem da Amazon:
    <ul>
        <li><b>Sistema Operacional (SO):</b> Linux, Windows ou Mac OS</li>
        <li>Quantidade de poder computacional e núcleos (CPU).</li>
        <li>Quantidade de memória de acesso aleatório (RAM).</li>
        <li>Quantidade de espaço de armazenamento:
            <ul>
                <li>Anexado à rede (EBS & EFS)</li>
                <li>Hardware (EC2 Instance Store)</li>
            </ul>
        </li>
        <li><b>Placa de rede:</b> velocidade da placa, Endereço IP público</li>
        <li><b>Grupo de Segurança (Regras de Firewall):</b>
            <ul>
                <li>Os Grupos de Segurança são fundamentais para a segurança de rede na AWS</li>
                <li>Eles controlam como o tráfego é permitido para dentro ou fora da Instância EC2:
                    <div align="center"> 
                        <img src="https://thumbs2.imgbox.com/a8/54/cSs3kUS3_t.png" />  
                    </div>
                </li>
                <li>Os Grupos de Segurança contêm <b>regras de permitir</b></li>
                <li>As regras dos Grupos de Segurança podem fazer referência a IP ou a outro Grupo de Segurança</li>
                <li>Os Grupos de Segurança atuam como um "firewall" nas instâncias EC2</li>
                <li>Eles regulam:  
                    <ul>
                        <li>Acesso às Portas</li>
                        <li>Faixas de IP autorizadas - IPv4 e IPv6</li>
                        <li>Controle de rede de entrada (de outros para a instância)</li>
                        <li>Controle de rede de saída (da instância para outros)</li>
                        <div align="center"> 
                            <img src="https://thumbs2.imgbox.com/9a/83/wrbTRumK_t.png" />  
                            <hr/>
                            Origem representa um intervalo de endereços IP e 0.0.0.0/0 significa que tudo pode acessar
                            (Isso é uma ilustração. Não compartilhe suas informações específicas)
                          <hr/>
                          Então, temos nossa instância EC2 e ela tem um Grupo de Segurança permitir anexado a ela,
                          que possui regras de entrada e regras de saída. Então, nosso computador será autorizado em, digamos, a                             porta 22. Assim, o tráfego pode passar do nosso computador para a instância EC2, mas o computador de                             outra pessoa, que não está usando meu endereço IP porque eles não moram onde eu moro (não possuem o                                mesmo IP), se tentarem acessar nossa instância EC2, eles não conseguirão, porque o firewall vai                                 bloquear e ocorrerá um timeout. Então, para as regras de saída, por padrão, nossa instância EC2 para                             qualquer Grupo de Segurança vai, por padrão, permitir qualquer tráfego saindo dela. Assim, se nossa                               instância EC2 tentar acessar um site e iniciar uma conexão, isso será permitido pelo Grupo de Segurança:
                          <img src="https://thumbs2.imgbox.com/c2/8a/AZQDOhCd_t.png" /> 
                          (Esses são os conceitos básicos de como o firewall funciona)
                          <hr/>
                          Sobre outros grupos de segurança. Então, temos uma instância EC2, e ela tem um grupo de segurança, que eu chamo de grupo número um, e as regras de entrada basicamente dizem que estou autorizando o grupo de segurança número um na entrada e o grupo de segurança número dois. Então, por que faríamos isso?
                          Bem, se lançarmos outra instância EC2 e ela tiver o grupo de segurança dois anexado a ela, usando a regra de grupo de segurança, basicamente permitimos que nossa instância EC2 se conecte diretamente na porta que decidimos para nossa primeira instância EC2.
                          Da mesma forma, se tivermos outra instância EC2 com o grupo de segurança um anexado, também autorizamos esta a se comunicar diretamente com nossas instâncias. E, independentemente do IP de nossas instâncias EC2, porque elas têm o grupo de segurança certo anexado a elas, podem se comunicar diretamente com outras instâncias. E isso é ótimo porque não faz você pensar em IPs o tempo todo. Assim como se tivermos outra instância EC2 talvez com o grupo de segurança número três anexado a ela, bem, como o grupo número três não foi autorizado nas regras de entrada do grupo de segurança número um, então está sendo negado e as coisas não funcionam. Isso é um recurso um pouco avançado, mas pode ser útil com balanceadores de carga:
                          <br/>
                          <img src="https://thumbs2.imgbox.com/c0/b8/HkkUiFUb_t.png" />  
                          </div> 
                          A notação "203.0.113.0/24" em CIDR representa um intervalo de endereços IP de 203.0.113.0 a 203.0.113.255. O "/24" indica que os primeiros 24 bits são a parte da rede, e os 8 bits restantes estão disponíveis para endereços de host.
                          Portanto, quando você especifica "203.0.113.0/24" como a origem na regra do seu grupo de segurança, ela abrange todos os endereços IP de 203.0.113.0 a 203.0.113.255, inclusivamente. Portanto, tanto 203.0.113.001 quanto 203.0.113.002 fazem parte deste intervalo.
                          <br/>
                          <ul>
                              Para esclarecer:
                              <li>203.0.113.0 é o endereço de rede.</li>
                              <li>203.0.113.255 é o endereço de transmissão.</li>
                              <li>O intervalo de endereços IP utilizáveis vai de 203.0.113.1 a 203.0.113.254.</li>
                              <li>Endereços IP fora desse intervalo, como 203.0.114.0, não são aceitáveis.</li>
                          </ul>
                        </div>
                    </ul>
                </li>
               <li>Restrito a uma combinação de região / VPC</li>
               <li>Existe "fora" da EC2 - se o tráfego for bloqueado, a instância EC2 não o verá</li>
               <li>É recomendável manter um grupo de segurança separado para acesso SSH</li>
               <li>Se sua aplicação não estiver acessível (timeout), então é um problema no grupo de segurança</li>
               <li>Se sua aplicação apresentar um erro de "conexão recusada", então é um erro na aplicação ou ela não foi iniciada</li>
               <li>Todo o tráfego de entrada é bloqueado por padrão</li>
               <li>Todo o tráfego de saída é autorizado por padrão</li>
              <li>Portas Clássicas para Conhecer
                  <ul>
                      <li>22 = SSH (Secure Shell) - fazer login em uma instância Linux.</li>
                      <li>21 = FTP (File Transfer Protocol) - enviar arquivos para um compartilhamento de arquivos.</li>
                      <li>22 = SFTP (Secure File Transfer Protocol) - enviar arquivos usando SSH.</li>
                      <li>80 = HTTP (Hypertext Transfer Protocol) - acessar sites não seguros.</li>
                      <li>443 = HTTPS (Hypertext Transfer Protocol Secure) - acessar sites seguros.</li>
                      <li>3389 = RDP (Remote Desktop Protocol) - fazer login em uma instância Windows.</li>
                  </ul>
              </li>
            </ul> 
        </li>
        <li><b>Script de inicialização (configurado no primeiro lançamento):</b> Dados do Usuário EC2.</li>
    </ul> 
</li>
<li>
    <b>Convenção:</b> A AWS segue a seguinte convenção de nomenclatura: <em>m</em><b>5</b>.2xlarge
    <ul>
        <li><em>m</em>: classe da instância</li>
        <li><b>5</b>: geração (a AWS as aprimora ao longo do tempo)</li>
        <li>2xlarge: tamanho dentro da classe da instância</li>
    </ul>
</li>
<li><b>Tipos de instância:</b> O EC2 oferece uma ampla seleção de tipos de instância, cada um com diferentes capacidades de CPU, memória, armazenamento e rede.
<div align="center"> 
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20220322144908/typesofec2instances768x384.png" width="70%">  
</div>
<ul>
<li><b>Uso geral:</b> 
  <ul>
    <li>Equilíbrio de recursos de computação, memória e rede.</li> 
    <li>Indicado para servidores de aplicativo, jogos, backend, banco de dados pequenos.</li>
  </ul>
<div align="center"> 
<img src="https://thumbs2.imgbox.com/ac/37/XseN96S8_t.png">  
</div>
 </li>
<li><b>Otimizadas para computação:</b>  
  <ul>
    <li>Ideal para cargas de trabalho que exigem processadores de alto desempenho.</li> 
    <li>Pode ser usado para os mesmos casos de uso da categoria de uso geral mas quando se deseja um melhor desempenho.</li>
    <li>Ideal também para processamento em lote.</li>
<div align="center"> 
<img src="https://news.mit.edu/sites/default/files/styles/news_article__image_gallery/public/images/202001/MIT-Evaluating-Performance_0.jpg?itok=qVXPQAya" width="50%">  
</div>
  </ul>
 </li>
</li>
<li><b>Otimizadas para memória:</b> 
    <ul>
    <li>Projeto para alto desempenho no processamento de grandes quantidades de informações na memória.</li> 
    <li>Por exemplo, banco de dados de alto desempenho, processamento em tempo real de dados.</li>
<div align="center"> 
<img src="https://thumbs2.imgbox.com/85/bb/AEbPZHGd_t.png">  
</div>
  </ul>
</li>
<li><b>Computação acelerada:</b> 
  <ul>
    <li>Usa acelaração de hardware ou coprocessadores para executar algumas funções mais eficiente do que em um software executado direto na CPU.</li> 
    <li>Muito usado em Cálculo de ponto flutuante, processamento de gráficos e correspondência de padrões de dados.</li>
  </ul>
<div align="center"> 
<img src="https://thumbs2.imgbox.com/33/18/Sg9mLdO3_t.png">  
</div>
</li>
<li><b>Otimizadas para armazenamento:</b> 
  <ul>
    <li>Ideal para cargas de trabalho que exigem acesso de leitura e gravação com grande volume de dados.</li> 
    <li>Muito usado em Sistema de arquivos distribuídos, Data warehouse, sistema de processamento de transações on-line.</li>
<div align="center"> 
<img src="https://thumbs2.imgbox.com/76/f9/NAK8q2sT_t.png">  
</div>
  </ul>
</li>  
<a href="https://aws.amazon.com/ec2/instance-types/"/> Mais informações</a>
 </ul>
<li><b>Regiões:</b> O EC2 está disponível em várias regiões ao redor do mundo. Cada região é uma área geográfica independente, com várias zonas de disponibilidade para aumentar a resiliência e a disponibilidade.</li>
<li><b>Zonas de disponibilidade:</b> Cada região do EC2 tem várias zonas de disponibilidade, que são data centers separados fisicamente, mas conectados por uma rede de baixa latência e alta largura de banda.</li>
<li><b>Elastic IP:</b> Um Elastic IP é um endereço IP estático que você pode associar a uma instância EC2. Ele permite que você mantenha o mesmo endereço IP mesmo se a instância for interrompida ou reiniciada.</li>
<li><b>Imagens AMI:</b> As Imagens de Máquina da Amazon (AMI) são imagens pré-configuradas que você pode usar para iniciar instâncias EC2. Elas contêm o sistema operacional, software necessário e configurações de aplicativos.
  <ul>
      <li> AMI é uma personalização de uma instância EC2
           <ul>
            <li>Você adiciona seu próprio software, configuração, sistema operacional, monitoramento...</li>
            <li>
              Tempo de inicialização/configuração mais rápido porque todo o seu software está pré-empacotado
            </li>
        </ul>
      </li>
      <li>
        AMI é construída para uma <b>região específica</b> (e pode ser copiada entre regiões)
      </li>
      <li>
         Você pode iniciar instâncias EC2 a partir de:
          <ul>
          <li>Uma AMI Pública: fornecida pela AWS</li>
          <li>Sua própria AMI: que você cria e mantém</li>
          <li>Uma AMI do AWS Marketplace: uma AMI feita por outra pessoa (e potencialmente à venda)</li>
        </ul>
      </li>
      <li>
         Processo AMI (de uma instância EC2):
          <ul>
          <li>Inicie uma instância EC2 e a personalize</li>
          <li>Pare a instância (para integridade dos dados)</li>
          <li>Crie uma AMI - isso também criará snapshots do EBS</li>
          <li>Inicie instâncias a partir de outras AMIs
            <hr/>
            Assim, existe uma instância EC2 em us-east-1a e a mesma instância em us-east-1b
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/9d/35/d3mKBbbJ_t.png">  
            </div>
            <hr/>
            O processo consiste em iniciar a instância em us-east-1a, mas é necessário personalizá-la, depois criar uma AMI a partir dela
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/ff/d8/5SdUhHBy_t.png">  
            </div>
            <hr/>
            Esta será sua AMI personalizada. E então, em us-east-1b, você poderá iniciar uma instância a partir dessa AMI. É uma cópia da sua instância EC2
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/22/28/0HABL0sI_t.png">  
            </div>
          </li>  
        </ul>
      </li>
  </ul>
</li>
<li><b>Load Balancers:</b> O EC2 oferece balanceadores de carga, que distribuem o tráfego de rede entre várias instâncias EC2 em uma região.</li>
</ul>
</details>

<details><summary> <h3>Boas práticas</h3></summary>
<ul>
   <li><b>Opção de Compra:</b> escolha o tipo de instância apropriado com base nas necessidades de recursos computacionais e na carga de trabalho esperada:
      <ul>
          <li>Instâncias Sob Demanda - carga de trabalho curta, precificação previsível, pagamento por segundo</li>
          <li>Reservadas (1 e 3 anos)
              <ul>
                  <li>Instâncias Reservadas - longas cargas de trabalho</li>
                  <li>Instâncias Reservadas Conversíveis - longas cargas de trabalho com instâncias flexíveis</li>
              </ul>
          </li>
          <li>Planos de Economia (1 e 3 anos) - compromisso com uma quantidade de uso, carga de trabalho longa</li>
          <li>Instâncias Spot - cargas de trabalho curtas, econômicas, podem perder instâncias (menos confiáveis)</li>
          <li>Hosts Dedicados - reserve um servidor físico inteiro, controle o posicionamento da instância</li>
          <li>Instâncias Dedicadas - nenhum outro cliente compartilhará seu hardware</li>
          <li>Reservas de Capacidade - reserve capacidade em uma Zona de Disponibilidade específica por qualquer duração</li>
        <hr/>
        <table>
          <tr>
            <th>Opção de Compra</th>
            <th>Descrição</th>
          </tr>
          <tr>
            <td>Instâncias Sob Demanda</td>
            <td>Carga de trabalho curta, precificação previsível, pagamento por segundo</td>
          </tr>
          <tr>
            <td>Instâncias Reservadas (1 e 3 anos)</td>
            <td>
              - Instâncias Reservadas: longas cargas de trabalho com compromisso a termo<br>
              - Instâncias Reservadas Convertíveis: longas cargas de trabalho com instâncias flexíveis
            </td>
          </tr>
          <tr>
            <td>Planos de Economia (1 e 3 anos)</td>
            <td>Compromisso com uma quantidade de uso, adequado para longas cargas de trabalho</td>
          </tr>
          <tr>
            <td>Instâncias Spot</td>
            <td>Cargas de trabalho curtas, econômicas, mas menos confiáveis</td>
          </tr>
          <tr>
            <td>Hosts Dedicados</td>
            <td>Reserve um servidor físico inteiro, controle a colocação das instâncias</td>
          </tr>
          <tr>
            <td>Instâncias Dedicadas</td>
            <td>Nenhum outro cliente compartilhará seu hardware</td>
          </tr>
          <tr>
            <td>Reservas de Capacidade</td>
            <td>Reserve capacidade em uma zona de disponibilidade específica por qualquer período</td>
          </tr>
        </table>
      </ul>
  </li> 
  <li>Configurar grupos de segurança para restringir o acesso à instância</li>
  <li>Usar chaves SSH para autenticar o acesso à instância</li>
  <li>Implementar backups regulares da instância para proteger dados críticos</li>
  <li>Monitorar o uso da instância e definir alertas para anomalias ou problemas de desempenho</li>
  <li>Usar o Elastic Load Balancing para distribuir a carga de trabalho entre várias instâncias e melhorar a disponibilidade</li>
  <li>Usar o Auto Scaling para aumentar ou diminuir a capacidade de instância com base na demanda de carga de trabalho, permitindo que a infraestrutura se ajuste automaticamente à demanda dos usuários</li>
  <li>Configurar as opções de segurança, como o CloudTrail e o CloudWatch, para monitorar e auditar o acesso à instância e proteger contra ameaças de segurança</li>
</ul>
</details>

<details><summary><h3>Modelo de Responsabilidade para EC2</h3></summary>

<table>
  <tr>
    <th>AWS</th>
    <th>USUÁRIO</th>
  </tr>
  <tr>
    <td>
        <ul>
          <li>Infraestrutura (segurança de rede global)</li>
          <li>Isolamento no host físico</li>
          <li>Substituição de hardware com defeito</li>
          <li>Validação de conformidade</li>
        </ul>
    </td>
    <td>
       <ul>
          <li>Regras de Grupos de Segurança</li>
          <li>Patches e atualizações do sistema operacional</li>
          <li>Software e utilitários instalados na instância EC2</li>
          <li>Funções IAM atribuídas à EC2 e gerenciamento de acesso do usuário IAM</li>
          <li>Segurança de dados na sua instância</li>
      </ul>
    </td>
  </tr>
</table>

</details>
