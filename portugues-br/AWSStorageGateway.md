AWS Storage Gateway

<div align="center">
  <img src="https://cdn2.iconfinder.com/data/icons/amazon-aws-stencils/100/Storage__Content_Delivery_AWS_Storage_Gateway-512.png" width="30%">
</div>
<br/>

O AWS Storage Gateway atua como uma ponte vital, conectando a infraestrutura de dados local com soluções de armazenamento baseadas em nuvem, especialmente o Amazon S3. Ele integra perfeitamente ambientes locais com a Nuvem AWS, fornecendo um serviço de armazenamento híbrido.
<hr/>

### Casos de Uso

<b>Recuperação de Desastres:</b> O Storage Gateway facilita soluções eficientes de recuperação de desastres, permitindo a replicação e o backup de dados para a nuvem de forma transparente, garantindo a continuidade dos negócios em caso de emergências.

<b>Backup e Restauração:</b> Oferece um mecanismo confiável para fazer backup de dados críticos de sistemas locais para a nuvem, simplificando estratégias de proteção de dados e garantindo a integridade dos dados.

<b>Armazenamento em Camadas:</b> O Storage Gateway permite que organizações implementem arquiteturas de armazenamento em camadas, otimizando custos e desempenho ao mover dados de forma transparente entre o armazenamento local e as camadas de armazenamento baseadas em nuvem, com base em padrões de acesso e requisitos.
<hr/>
Tipos de Gateway de Armazenamento

<b>Gateway de Arquivo:</b> Permite que aplicativos locais acessem dados armazenados como objetos no Amazon S3 usando protocolos de arquivo padrão. Este gateway oferece uma maneira transparente e econômica de armazenar e recuperar dados na nuvem, mantendo a compatibilidade com aplicativos existentes.

<b>Gateway de Volume:</b> Apresenta armazenamento em nuvem como volumes de armazenamento de blocos iSCSI, permitindo que aplicativos locais acessem armazenamento em nuvem durável e escalável. Ele fornece acesso em nível de bloco e suporta vários casos de uso, como backup, recuperação de desastres e migração de dados.

<b>Gateway de Fita:</b> Integra aplicativos de backup locais com Amazon S3 e Glacier, permitindo que os usuários armazenem dados na nuvem usando fluxos de trabalho baseados em fita. O Gateway de Fita fornece armazenamento de arquivamento durável e econômico com capacidades de backup externo.
<hr/>

### Extra

#### Opções Nativas de Armazenamento da AWS

Então, se você quisesse resumir as opções de armazenamento na AWS, o armazenamento de blocos seria o EBS ou uma instância de armazenamento EC2.

O armazenamento de arquivos seria um sistema de arquivos de rede, então Amazon EFS e o armazenamento de objetos seriam Amazon S3 ou Glacier.
<br/>
<div align="center">
  <img src="https://thumbs2.imgbox.com/f7/45/7NyuhKAK_t.png">
</div>
