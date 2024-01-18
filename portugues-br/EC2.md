EC2
<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/large/2x/aws-ec2-logo-svg-vector.svg" width="25%">
</div>

Amazon EC2 (Elastic Compute Cloud) é um serviço de computação em nuvem que oferece capacidade de computação escalável na nuvem da Amazon. Ele permite que você configure e execute facilmente servidores virtuais na nuvem da Amazon, chamados de Instâncias EC2. Com o Amazon EC2, você pode dimensionar sua capacidade de computação vertical ou horizontalmente de acordo com as necessidades de sua aplicação, pagando apenas pelos recursos que utiliza.

EC2 = Elastic Compute Cloud = Infraestrutura como Serviço

Isso consiste principalmente na capacidade de:

<ul>
    <li>Alugar máquinas virtuais (EC2).</li>
    <li>Armazenar dados em discos virtuais (EBS).</li>
    <li>Distribuir carga entre máquinas (ELB).</li>
    <li>Dimensionar os serviços usando um grupo de dimensionamento automático (ASG).</li>
</ul>

<details><summary> <h3>Recursos</h3></summary>
<hr/>
<ul>
    <li><b>Elasticidade:</b> O EC2 permite que você dimensione sua capacidade de computação vertical ou horizontalmente de acordo com as necessidades de sua aplicação.</li>
    <li><b>Flexibilidade:</b> O EC2 oferece uma ampla seleção de tipos de instância, sistemas operacionais, bancos de dados e outras opções de software para você escolher.</li>
    <li><b>Integração com outros serviços AWS:</b> O EC2 pode ser facilmente integrado a outros serviços da AWS, como Amazon S3, Elastic Load Balancing, Amazon RDS, entre outros.</li>
    <li><b>Segurança:</b> O EC2 oferece recursos avançados de segurança, como isolamento de instâncias, criptografia de dados, autenticação de usuários e muito mais.</li>
    <li><b>Gerenciamento:</b> O EC2 permite que você gerencie facilmente suas instâncias, com recursos como Amazon EC2 Auto Scaling e Amazon EC2 Systems Manager.</li>
</ul> 
<hr/>
</details>

<details><summary> <h3>Componentes e Configuração</h3></summary>
 <hr/>
 <p>As instâncias EC2 têm muitos componentes e recursos:</p>
   <details><summary> <h3>Sistema Operacional</h3></summary>
     <ul>
      <li><b>Sistema Operacional (SO):</b> Linux, Windows ou Mac OS</li>
      <li>Quantidade de poder de processamento e núcleos (CPU).</li>
      <li>Quantidade de memória de acesso aleatório (RAM).</li>
      <li>Espaço de armazenamento:
          <ul>
            <li>Conectado à rede (EBS & EFS)</li>
            <li>Hardware (EC2 Instance Store)</li>
          </ul>
      <li><b>Placa de rede:</b> velocidade da placa, endereço IP público</li>  
    </ul>
  </details>
    
  <details><summary> <h3>Grupo de Segurança (Regras do Firewall)</h3></summary>
    <ul>
        <li>Os Grupos de Segurança são fundamentais para a segurança de rede na AWS.</li>
        <li>Eles controlam como o tráfego é permitido dentro ou fora da Instância EC2:
        <div align="center"> 
        <img src="https://thumbs2.imgbox.com/71/d4/653laO96_t.png" />  
        </div>
        </li>
        <li>Os grupos de segurança contêm <b>regras de permissão</b>.</li>
        <li>As regras de grupos de segurança podem fazer referência a IP ou a outros grupos de segurança.</li>
        <li>Os grupos de segurança atuam como um "firewall" nas Instâncias EC2.</li>
        <li>Regulam:  
          <ul>
            <li>Acesso às Portas</li>
            <li>Faixas de IP autorizadas - IPv4 e IPv6</li>
            <li>Controle de rede de entrada (de outros para a instância)</li>
            <li>Controle de rede de saída (da instância para outros)</li>
            <div align="center"> 
            <img src="https://thumbs2.imgbox.com/9f/5d/nGp5IhhT_t.png" />  
              <hr/>
              A origem representa um intervalo de endereços IP e 0.0.0.0/0 significa tudo
              (Isso é uma ilustração. Não compartilhe suas informações específicas)
              <hr/>
              Então temos nossa Instância EC2 e ela possui um grupo de segurança permitido anexado a ela
              que possui regras de entrada e regras de saída. Assim, nosso computador será autorizado a dizer na porta 22.
              Assim, o tráfego pode passar do nosso computador para a Instância EC2, mas o computador de outra pessoa, que não está usando meu endereço IP porque não mora onde moro (não tem o mesmo IP), então se eles tentarem acessar nossa Instância EC2, eles não conseguirão, porque o firewall vai bloquear e será um timeout. Então, para as regras de saída por padrão, nossa Instância EC2 para qualquer grupo de segurança vai permitir por padrão qualquer tráfego fora dela. Então, se nossa Instância EC2 tentar acessar um site e iniciar uma conexão, ela será permitida pelo grupo de segurança:
            <img src="https://thumbs2.imgbox.com/8b/ab/I2BjxQMv_t.png" /> 
              <br/>
              (Então, este é o básico de como o firewall funciona) 
               <hr/>
               Sobre outros grupos de segurança. Então, temos uma Instância EC2, e ela tem um grupo de segurança, o que chamo de grupo número um, e as regras de entrada basicamente estão dizendo, estou autorizando o grupo de segurança número um na entrada e o grupo de segurança número dois. Então, por que faríamos isso? 
               Bem, se lançarmos outra Instância EC2 e ela tiver o grupo de segurança dois anexado a ela, bom, usando a regra de grupo de segurança (instinto), basicamente permitimos que nossa Instância EC2 se conecte diretamente na porta que decidimos para nossa primeira Instância EC2.
              Da mesma forma, se tivermos outra Instância EC2 com o grupo de segurança um anexado, bem,
              porque é o grupo número um, não foi autorizado nas regras de entrada do grupo de segurança número dois, então está sendo negado e as coisas não funcionam. Então isso é um recurso um pouco avançado. Enquanto pode ser útil com balanceadores de carga:
              <br/>
              <img src="https://thumbs2.imgbox.com/26/2c/GV6J2skK_t.png" />  
            </div> 
              A notação "203.0.113.0/24" em CIDR representa uma faixa de endereços IP de 203.0.113.0 a 203.0.113.255. O "/24" indica que os primeiros 24 bits são a parte da rede e os 8 bits restantes estão disponíveis para endereços de host.
              Portanto, ao especificar "203.0.113.0/24" como a origem na regra do grupo de segurança, ela abrange todos os endereços IP de 203.0.113.0 a 203.0.113.255, inclusivos. Portanto, tanto 203.0.113.001 quanto 203.0.113.002 fazem parte desta faixa.
              <br/>
                <ul>
                  Para esclarecer:
                  <li>203.0.113.0 é o endereço de rede.</li>
                  <li>203.0.113.255 é o endereço de broadcast.</li>
                  <li>A faixa de endereços IP utilizáveis é de 203.0.113.1 a 203.0.113.254.</li>
                  <li>Endereços IP fora dessa faixa, como 203.0.114.0, não são aceitáveis.</li>
                </ul>
          </ul>
        </li>
        <li>Restrito a uma combinação de região / VPC</li>
        <li>Não "vê" fora do EC2 - se o tráfego for bloqueado, a Instância EC2 não verá</li>
        <li>É bom manter um grupo de segurança separado para acesso SSH</li>
        <li>Se sua aplicação não for acessível (timeout), é um problema de grupo de segurança</li>
        <li>Se sua aplicação der um erro "connection refused", é um erro de aplicação ou ela não está iniciada</li>
        <li>Todo tráfego de entrada é bloqueado por padrão</li>
        <li>Todo tráfego de saída é autorizado por padrão</li>
        <li> Portas clássicas a conhecer
          <ul>
            <li>22 = SSH (Secure Shell) - entrar em uma instância Linux.</li>
            <li>21 = FTP (File Transfer Protocol) - enviar arquivos para um compartilhamento de arquivos.</li>
            <li>22 = SFTP (Secure File Transfer Protocol) - enviar arquivos usando SSH.</li>
            <li>80 = HTTP (Hypertext Transfer Protocol) - acessar sites não seguros.</li>
            <li>443 = HTTPS (Hypertext Transfer Protocol Secure) - acessar sites seguros </li>
            <li>3389 = RDP (Remote Desktop Protocol) - entrar em uma instância Windows</li>
          </ul>
        </li>
      </ul> 
    </li>  
    <li><b>Script de Inicialização (configuração no primeiro lançamento):</b> Dados do Usuário EC2.</li>
  </ul> 
</li>
<li>
    <b>Convenção:</b> A AWS segue a seguinte convenção de nomenclatura:  <em>m</em><b>5</b>.2xlarge
    <ul>
      <li><em>m</em>: classe da instância</li>
      <li><b>5</b>: geração (a AWS as melhora ao longo do tempo)</li>
      <li>2xlarge: tamanho dentro da classe da instância</li>
    </ul>
</ul>

</details>

 <details><summary> <h3>Instance Types</h3></summary>

  EC2 offers a wide selection of instance types, each with different CPU, memory, storage, and networking capabilities.
    <div align="center"> 
      <img src="https://media.geeksforgeeks.org/wp-content/uploads/20220322144908/typesofec2instances768x384.png" width="70%">  
      </div>
      <ul>
      <li><b>General Purpose:</b>
        <ul>
          <li>Balances compute, memory, and networking resources.</li> 
          <li>Recommended for application servers, gaming, backend, small databases.</li>
        </ul>
      <div align="center"> 
        <img src="https://thumbs2.imgbox.com/ac/37/XseN96S8_t.png">  
      </div>  
       </li>
      <li><b>Compute Optimized:</b>  
        <ul>
          <li>Ideal for workloads that require high-performance processors.</li> 
          <li>Can be used for the same use cases as general purpose but when higher performance is desired.</li>
          <li>Also ideal for batch processing.</li>
          <div align="center"> 
              <img src="https://news.mit.edu/sites/default/files/styles/news_article__image_gallery/public/images/202001/MIT-Evaluating-Performance_0.jpg?itok=qVXPQAya" width="50%">  
          </div>
          </ul>
         </li>
        </li>
        <li><b>Memory Optimized:</b> 
            <ul>
            <li>Designed for high performance in processing large amounts of in-memory data.</li> 
            <li>For example, high-performance databases, real-time data processing.</li>
        <div align="center"> 
          <img src="https://thumbs2.imgbox.com/85/bb/AEbPZHGd_t.png">  
        </div>      
      </ul>
    </li>
    <li><b>Accelerated Computing:</b> 
      <ul>
        <li>Uses hardware acceleration or coprocessors to perform certain functions more efficiently than in software running directly on the CPU.</li> 
        <li>Commonly used for floating-point calculations, graphics processing, and data pattern matching.</li>
    <div align="center"> 
    <img src="https://thumbs2.imgbox.com/33/18/Sg9mLdO3_t.png">  
    </div>
      </ul>
    </li>
    <li><b>Storage Optimized:</b> 
      <ul>
        <li>Ideal for workloads that require high read and write access to large volumes of data.</li> 
        <li>Commonly used in distributed file systems, data warehouses, online transaction processing systems.</li>
    <div align="center"> 
    <img src="https://thumbs2.imgbox.com/76/f9/NAK8q2sT_t.png">  
    </div>
  </ul>
    </li>
    <a href="https://aws.amazon.com/ec2/instance-types/"/> More information</a>
  </ul>
</li>

  </details>
  
  <details><summary> <h3>AMI images</h3></summary>

  <p>AMI images:</b> Amazon Machine Images (AMI) are pre-configured images that you can use to launch EC2 Instances. They contain the operating system, necessary software, and application settings.</p>
    <ul>
        <li> AMI are a customization of an EC2 Instance
             <ul>
              <li>You add your own software, configuration, operation system, monitoring...</li>
              <li>
                Faster boot / configuration time because all your software is pre-packaged
              </li>
          </ul>
        </li>
        <li>
          AMI are built for a <b>specific region</b> (and can be copied across regions)
        </li>
        <li>
           You can launch EC2 Instances from:
            <ul>
            <li>A Public AMI: AWS provided</li>
            <li>You own AMI: you make and maintain them yourself</li>
            <li>An AWS Marketplace AMI: an AMI someone else made (and potentially sells)</li>
          </ul>
        </li>
        <li>
           AMI Process (from an EC2 Instance):
            <ul>
            <li>Start an EC2 Instance and customize ir</li>
            <li>Stop the instance (for data integrity)</li>
            <li>Build an AMI - this will also create EBS snapshots</li>
            <li>Launch a instances from others AMIs
              <hr/>
              So exist a EC2 Instance in us-east-1a and the same instance as us-east-b
              <div align="center"> 
                <img src="https://thumbs2.imgbox.com/9d/35/d3mKBbbJ_t.png">  
              </div>
              <hr/>
              the proccess consist to launch the instance in us-east-1a, but are necessary customize, then create an AMI from it
              <div align="center"> 
                <img src="https://thumbs2.imgbox.com/ff/d8/5SdUhHBy_t.png">  
              </div>
              <hr/>
              this will be you custom AMI. And then in us-east-1b you will be able to launch from that AMI. It is a copy of your EC2 Instance
              <div align="center"> 
                <img src="https://thumbs2.imgbox.com/22/28/0HABL0sI_t.png">  
              </div>
            </li>  
          </ul>
        </li>
    </ul>
  
  </details>
  
  <details><summary> <h3>EC2 Image Builder</h3></summary>
    
  <p>EC2 Image Builder</p>
    <ul>
      <li>Used to automate the creation of Virtual Machines or container images</li>
      <li>Automate the creation, maintain, validate and test EC2 AMIs, and more</li>
      <li>Can be run on a schedule (weekly, whenever packages are updated, etc...)</li>
      <li>Free service (only pay for the underlying resources)</li>
      <li>Example:
        <hr/>
          So we have the EC2 Image Builder service and we're going to set it up. And it is automatically when it's going to run
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/c0/49/IuhxLYM2_t.png">  
            </div>
        <hr/>
          it is going to create an EC2 Instance called Builder EC2 Instance.
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/aa/f3/bgy59Cv0_t.png">  
            </div>
        <hr/>
          And that EC2 Instance is going to build components and customize the software. For example, install Java, update the CLI, update the software system,
          maybe install firewalls, whatever you define to happen on that EC2 Instance, maybe install your application.
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/b8/1c/DEjZt2tk_t.png">  
            </div>
        <hr/>
          An then once this is done, then an AMI is going to be created out of that EC2 Instance, but all of this is obviously automated.
         Then the AMI is created, but we want to validate it. 
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/de/f3/NtWjFoR1_t.png">  
            </div>
        <hr/>
          So EC2 Image Builder will automatically create a test EC2 Instance from that AMI and going to run a bunch of tests that you are defining in advance.
          And if you don't wanna run any tests, you can just skip that test. But the test can be asking, is the AMI working? Is it secure? Is my application running correctly?
          All these kind of things. 
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/68/15/BOE3J1if_t.png">  
            </div>
        <hr/>
          And then one the AMI is tested, then the AMI is going to be distributed, so while EC2 Image Builder is a regional service, it is possible for you to take that AMI and
          distribute it to multiple regions, therefore, allowing your application and workflow to be truly global. Next, EC2 Image Builder can be run on a schedule. So you can define a weekly schedule,
          or you can say you can run whenever packages are updated, or you can run it manually, etc. And it is a free service. So you're only going to pay for the underlying resources. What's means? That              means that if you create an EC2 Instance during this process, an EC2 Image Builder will create these EC2 Instances, then you're going to pay for these EC2 Instances. And when the AMI
          is created and distribuited youre going to pay for these storage of that AMI wherever it has been created, and wherever it has been distribuited.
            <div align="center">  
              <img src="https://thumbs2.imgbox.com/b9/ae/h2K8lKjU_t.png">  
            </div>
      </li>
    </ul>
  </li>
 
</details>

<details><summary><h3>EBS - Armazenamento da Instância</h3></summary>
  <ul>
    <li>Os volumes EBS são unidades de rede com desempenho bom, mas "limitado"</li>
    <li>Se você precisa de um disco de hardware com alto desempenho, use o Armazenamento da Instância EC2</li>
    <li>Melhor desempenho de I/O</li>
    <li>O Armazenamento da Instância EC2 perde seu armazenamento se for interrompido (efêmero)</li>
    <li>Bom para buffer/cache/dados temporários/contúdo temporário</li>
    <li>Risco de perda de dados em caso de falha de hardware</li>
    <li>Backups e replicação são de sua responsabilidade</li>
  </ul>
</details>

<details><summary><h3>EFS - Sistema de Arquivos Elástico</h3></summary>
  <ul>
    <li>NFS gerenciado (sistema de arquivos de rede) que pode ser montado em centenas de instâncias EC2</li>
    <li>O EFS funciona com instâncias EC2 Linux em várias zonas de disponibilidade</li>
    <li>Altamente disponível, escalável, custoso, pagamento por uso, sem planejamento de capacidade</li>
 
  <hr/>
  <p>
    Neste diagrama, existe um Sistema de Arquivos EFS com um grupo de segurança, e então temos instâncias EC2 em várias zonas de disponibilidade conectadas a ele.
    Portanto, temos instâncias EC2 em us-east-1a, instâncias EC2 em us-east-1b, bem como instâncias EC2 em us-east-1c. E todas estão conectadas ao mesmo sistema EFS:
  </p>
  <div align="center"> 
              <img src="https://thumbs2.imgbox.com/2e/2f/j6bLDISQ_t.png">  
            </div>
        <hr/>
   <li> Acesso Infrequente EFS (EFS-IA)
      <ul>
        <li>Classe de armazenamento otimizada para arquivos não acessados diariamente</li>
        <li>Custo mais baixo em comparação com o Padrão</li>
        <li>O EFS moverá automaticamente seus arquivos para o EFS-IA com base no último acesso</li>
        <li>Ative o EFS-IA com uma Política de Ciclo de Vida</li>
        <li>Exemplo: mova arquivos que não foram acessados por 60 dias para o EFS-IA</li>
        </ul>
          <div align="center"> 
                <img src="https://thumbs2.imgbox.com/e3/33/VrvdXrru_t.png">  
          </div>
        <hr/>
   </ul>
</details>

<details><summary><h3>EBS vs EFS</h3></summary>
   <p>
     Observando um EBS com uma instância EC2 em uma Zona de Disponibilidade 1 (AZ) e outra Zona de Disponibilidade 2. Em seguida, o volume EBS só pode ser anexado a uma instância em uma AZ específica. E os volumes EBS estão vinculados a Zonas de Disponibilidade específicas.
     Mas se quisermos mover o volume EBS de uma AZ para outra, podemos criar um snapshot. Isso criaria um snapshot do EBS e, em seguida, restauraríamos esse snapshot em uma nova zona de disponibilidade.
     E, efetivamente, teríamos movido o volume EBS. Mas isso é uma cópia, não é uma réplica em sincronia. Isso é uma cópia, e isso significaria que esse disco agora pode ser usado por outra instância EC2:
   </p>
  <div align="center"> 
      <img src="https://thumbs2.imgbox.com/1c/74/e3OiEdv8_t.png">  
  </div>
  <hr/>
  <p>
    EFS é um sistema de arquivos de rede. Isso significa que tudo o que está no drive EFS é compartilhado por tudo o que está montado nele. Então, o que isso significa? Digamos que tenhamos muitas instâncias na Zona de Disponibilidade um em um
    ou muitas instâncias também na Zona de Disponibilidade 2. Ao mesmo tempo, todas essas instâncias podem montar o mesmo drive EFS, usando um alvo de montagem, e todas verão os mesmos arquivos.
    Isso torna um sistema de arquivos compartilhado:
  </p>
  <div align="center"> 
      <img src="https://thumbs2.imgbox.com/36/ac/gg8CtxzO_t.png">
  </div>
  <hr/>
</details>

<details><summary><h3>FSx</h3></summary>
  <ul>
    <li>Lance sistemas de arquivos de alto desempenho de terceiros na AWS</li>
    <li>Serviço totalmente gerenciado</li>
    <li>Atualmente existem 3 tipos de FSx
        <ul>
          <li>FSx para Windows File Server
            <ul>
              <li>Um sistema de arquivos compartilhado nativo do Windows totalmente gerenciado, altamente confiável e escalável</li>
              <li>Construído no Windows File Server</li>
              <li>Suporta protocolo SMB e Windows NTFS</li>
              <li>Integrado ao Microsoft Active Directory</li>
              <li>Pode ser acessado pela AWS ou pela sua infraestrutura local</li>
            </ul>
            <div align="center"> 
              <img src="https://thumbs2.imgbox.com/ab/7c/USeaqi2h_t.png">
            </div>
            <hr/>
          </li>
          <li>FSx para Lustre
            <ul>
              <li>Armazenamento de arquivos totalmente gerenciado, de alto desempenho e escalável para <b>Computação de Alto Desempenho (HPC)</b></li>
              <li>O nome Lustre é derivado de "Linux" e "cluster"</li>
              <li>Aprendizado de Máquina, Análises, Processamento de Vídeo, Modelagem Financeira...</li>
              <li>Escalabilidade de até 100 GB/s, milhões de operações por segundo, latências sub-milissegundos</li>
            </ul>
            <div align="center"> 
                <img src="https://thumbs2.imgbox.com/3f/29/oDflKIeQ_t.png">
            </div>
          </li>
          <li>FSx para NetApp ONTAP
            <ul>
                <li>Um serviço em nuvem totalmente gerenciado que oferece armazenamento compartilhado altamente disponível e escalável com recursos avançados de gerenciamento de dados.</li>
                <li>Baseado no sistema operacional de armazenamento NetApp ONTAP, oferecendo recursos de nível empresarial para gerenciamento, eficiência e segurança de dados.</li>
                <li>Suporta os protocolos NFS (Network File System) e SMB (Server Message Block), sendo adequado para uma ampla variedade de aplicativos e cargas de trabalho.</li>
                <li>Oferece recursos avançados de gerenciamento de dados, como deduplicação, compressão de dados e backups baseados em snapshots, aprimorando a eficiência de armazenamento e a proteção de dados.</li>
                <li>Integra-se perfeitamente ao seu ambiente NetApp local existente, possibilitando cenários de nuvem híbrida.</li>
                <li>Permite fácil migração e replicação de dados entre sistemas NetApp locais e FSx para NetApp ONTAP na AWS.</li>
            </ul>
            <div align="center"> 
                <img src="https://github.com/gil-son/aws/assets/72712095/073c464d-5857-4e20-96db-d8fd66a26170">
            </div>
          </li>
        </ul>
    </li>
  </ul>
  <hr/>
</details>

<details><summary><h3>Escalabilidade e Disponibilidade</h3></summary>
  <details><summary><h4>Escalabilidade</h4></summary>
        <ul>
          <li>Escalabilidade significa que a aplicação/sistema pode lidar com cargas maiores ao se adaptar.</li>
          <li>Há dois tipos de escalabilidade:
            <ul>
              <li>Escalabilidade Vertical
                <ul>
                  <li>Escalabilidade Vertical significa aumentar o tamanho da instância.</li>
                  <li>Melhorar qualquer parte da instância.</li>
                  <li>Sua aplicação roda em um t2.micro, escalar verticalmente significa rodá-la em um t2.large, por exemplo.</li>
                  <div align="center">
                    <img src="https://thumbs2.imgbox.com/d4/1a/yPfIV4ZR_t.png">
                  </div>
                  <li>A escalabilidade vertical é muito comum para sistemas não distribuídos, como um banco de dados.</li>
                  <li>Geralmente, há um limite para o quanto você pode escalar verticalmente (limite de hardware).</li>
                </ul>
              </li>
              <li>Escalabilidade Horizontal (= elasticidade)
                  <ul>
                  <li>Escalabilidade Horizontal significa aumentar o número de instâncias/sistemas para sua aplicação.</li>
                  <li>A escalabilidade horizontal implica em sistemas distribuídos.</li>
                  <li>Isso é muito comum em aplicações web/aplicações modernas.</li>
                  <div align="center">
                    <img src="https://thumbs2.imgbox.com/1e/13/1NerXmnE_t.png">
                  </div>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
    </details>
    <details><summary><h4>Disponibilidade</h4></summary>
    <ul>
      <li>A Alta Disponibilidade geralmente está associada à escalabilidade horizontal.</li>
      <li>Alta disponibilidade significa executar sua aplicação/sistema em pelo menos 2 Zonas de Disponibilidade.</li>
      <li>O objetivo da alta disponibilidade é sobreviver à perda de um centro de dados (desastre).</li>
      <div align="center">
        <img src="https://thumbs2.imgbox.com/78/63/coxLKVbv_t.png">
      </div>
      <div align="center">
        <img src="https://thumbs2.imgbox.com/c6/b3/Sjg8TioT_t.png">
      </div>
    </ul>
  </details>
</details>

<details><summary><h3>Escalabilidade e Disponibilidade para EC2</h3></summary>
  <ul>
    <li>Escalonamento Vertical: Aumentar o tamanho da instância (= escalar para cima/baixo)
      <ul>
        <li>De: t2.nano - 0.5 de RAM, 1 vCPU</li>
        <li>Para: u-12tb.metal - 12.3TB de RAM, 448 vCPUs</li>
      </ul>
    </li>
    <li>Escalonamento Horizontal: Aumentar o número de instâncias (= escalar para fora/dentro)
      <ul>
        <li>Grupo de Auto Scaling</li>
        <li>Balanceador de Carga</li>
      </ul>
    </li>
    <li>Alta Disponibilidade: Executar instâncias para a mesma aplicação em várias Zonas de Disponibilidade:
      <ul>
        <li>Grupo de Auto Scaling em várias Zonas de Disponibilidade</li>
        <li>Balanceador de Carga em várias Zonas de Disponibilidade</li>
      </ul>
    </li>
  </ul>
</details>

  <p><b>Load Balancers:</b> EC2 offers load balancers, which distribute network traffic among multiple EC2 Instances in a region.</p>
  <p><b>Regions:</b> EC2 is available in several regions around the world. Each region is an independent geographic area, with multiple availability zones to increase resilience and availability.</p>
  <p><b>Availability zones:</b> Each EC2 region has multiple availability zones, which are physically separate data centers, but connected by a low-latency, high-bandwidth network.</p>
  <p><b>Elastic IP:</b> An Elastic IP is a static IP address that you can associate with an EC2 Instance. It allows you to keep the same IP address even if the instance is stopped or restarted.</p>
  <hr/>
</details>



<details><summary> <h3>Melhores Práticas</h3></summary>
<hr/>
<ul>
  <li><b>Opção de Compra:</b> Escolha o tipo de instância apropriado com base nas necessidades de recursos de computação e carga de trabalho esperada:
    <ul>
      <li>Instâncias On-Demand - carga de trabalho curta, precificação previsível, pagamento por segundo</li>
      <li>Reservadas (1 e 3 anos)
        <ul>
          <li>Instâncias Reservadas - cargas de trabalho longas</li>
          <li>Instâncias Reservadas Conversíveis - cargas de trabalho longas com instâncias flexíveis</li>
        </ul>
      </li>
      <li>Planos de Economia (1 e 3 anos) - compromisso com uma quantidade de uso, carga de trabalho longa</li>
      <li>Instâncias Spot - cargas de trabalho curtas, econômicas, podem perder instâncias (menos confiáveis)</li>
      <li>Hosts Dedicados - reserve um servidor físico inteiro, controle o posicionamento da instância</li>
      <li>Instâncias Dedicadas - nenhum outro cliente compartilhará seu hardware</li>
      <li>Reservas de Capacidade - reserve capacidade em uma zona de disponibilidade específica por qualquer duração</li>
    </ul>
      <hr/>
      <table>
        <tr>
          <th>Opção de Compra</th>
          <th>Descrição</th>
        </tr>
        <tr>
          <td>Instâncias On-Demand</td>
          <td>Carga de trabalho curta, precificação previsível, pagamento por segundo</td>
        </tr>
        <tr>
          <td>Instâncias Reservadas (1 e 3 anos)</td>
          <td>
            - Instâncias Reservadas: Cargas de trabalho longas com um compromisso de prazo fixo<br>
            - Instâncias Reservadas Conversíveis: Cargas de trabalho longas com instâncias flexíveis
          </td>
        </tr>
        <tr>
          <td>Planos de Economia (1 e 3 anos)</td>
          <td>Compromisso com uma quantidade de uso, adequado para cargas de trabalho longas</td>
        </tr>
        <tr>
          <td>Instâncias Spot</td>
          <td>Cargas de trabalho curtas, eficientes em custo, mas menos confiáveis</td>
        </tr>
        <tr>
          <td>Hosts Dedicados</td>
          <td>Reserve um servidor físico inteiro, controle o posicionamento da instância</td>
        </tr>
        <tr>
          <td>Instâncias Dedicadas</td>
          <td>Nenhum outro cliente compartilhará seu hardware</td>
        </tr>
        <tr>
          <td>Reservas de Capacidade</td>
          <td>Reserve capacidade em uma zona de disponibilidade específica por qualquer duração</td>
        </tr>
    </table>
  </li>
  <li>Configure grupos de segurança para restringir o acesso à instância</li>
  <li>Use chaves SSH para autenticar o acesso à instância</li>
  <li>Implemente backups regulares da instância para proteger dados críticos</li>
  <li>Monitore o uso da instância e defina alertas para anomalias ou problemas de desempenho</li>
  <li>Use o Elastic Load Balancing para distribuir a carga de trabalho entre várias instâncias e melhorar a disponibilidade</li>
  <li>Use o Auto Scaling para aumentar ou diminuir a capacidade da instância com base na demanda da carga de trabalho, permitindo que a infraestrutura se ajuste automaticamente à demanda do usuário</li>
  <li>Configure opções de segurança, como CloudTrail e CloudWatch, para monitorar e auditar o acesso à instância e proteger contra ameaças de segurança</li>
</ul>
<hr/>
</details>

<details><summary> <h3>Modelo de Responsabilidade para EC2</h3></summary>
<hr/>
<table>
  <tr>
    <th>AWS</th>
    <th>USUÁRIO</th>
  </tr>
  <tr>
    <td>
        <ul>
          <li>Infraestrutura (segurança global da rede)</li>
          <li>Isolamento no host físico</li>
          <li>Substituição de hardware com defeito</li>
          <li>Validação de conformidade</li>
        </ul>
    </td>
    <td>
       <ul>
          <li>Regra de Grupos de Segurança</li>
          <li>Patches e atualizações do sistema operacional</li>
          <li>Software e utilitários instalados na Instância EC2</li>
          <li>Funções IAM atribuídas à EC2 e gerenciamento de acesso de usuário IAM</li>
          <li>Segurança de dados em sua instância</li>
      </ul>
    </td>
  </tr>
</table>
<hr/>
</details>

<details><summary><h3>Modelo de Responsabilidade para Armazenamento do EC2</h3></summary>
<hr/>
<table>
  <tr>
    <th>AWS</th>
    <th>USUÁRIO</th>
  </tr>
  <tr>
    <td>
        <ul>
          <li>Infraestrutura</li>
          <li>Replicação de dados para volumes EBS e unidades EFS</li>
          <li>Substituição de hardware com defeito</li>
          <li>Garantir que seus funcionários não possam acessar seus dados</li>
        </ul>
    </td>
    <td>
       <ul>
          <li>Configurar procedimentos de backup/snapshot</li>
          <li>Configurar a criptografia de dados</li>
          <li>Responsabilidade por quaisquer dados nos drives</li>
          <li>Compreender o risco de usar o Armazenamento de Instância EC2</li>
      </ul>
    </td>
  </tr>
</table>
<hr/>
</details>

