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
        <li><b>Regras de firewall:</b> grupo de segurança.</li>
        <li><b>Script de inicialização (configurado no primeiro lançamento):</b> Dados do Usuário EC2.</li>
    </ul> 
</li>
<li><b>Imagens de AMI:</b> As imagens de AMI (Amazon Machine Image) são imagens pré-configuradas que você pode usar para iniciar instâncias EC2. Elas contêm o sistema operacional, o software necessário e as configurações da aplicação.</li>
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
<li><b>Load Balancers:</b> O EC2 oferece balanceadores de carga, que distribuem o tráfego de rede entre várias instâncias EC2 em uma região.</li>
</ul>
</details>

<details><summary> <h3>Boas práticas</h3></summary>
<ul>
  <li>Escolher o tipo de instância apropriado com base nas necessidades de recursos de computação e na carga de trabalho prevista</li>
  <li>Configurar grupos de segurança para restringir o acesso à instância</li>
  <li>Usar chaves SSH para autenticar o acesso à instância</li>
  <li>Implementar backups regulares da instância para proteger dados críticos</li>
  <li>Monitorar o uso da instância e definir alertas para anomalias ou problemas de desempenho</li>
  <li>Usar o Elastic Load Balancing para distribuir a carga de trabalho entre várias instâncias e melhorar a disponibilidade</li>
  <li>Usar o Auto Scaling para aumentar ou diminuir a capacidade de instância com base na demanda de carga de trabalho, permitindo que a infraestrutura se ajuste automaticamente à demanda dos usuários</li>
  <li>Configurar as opções de segurança, como o CloudTrail e o CloudWatch, para monitorar e auditar o acesso à instância e proteger contra ameaças de segurança</li>
</ul>
</details>
