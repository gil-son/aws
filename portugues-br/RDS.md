RDS
<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/thumbs/2x/aws-rds-logo.png" width="40%">
</div>
<br>
<br>
<p>
O Amazon Relational Database Service (RDS) é um serviço de banco de dados gerenciado e escalável que simplifica a configuração, operação e escalabilidade de bancos de dados relacionais na nuvem. O RDS é compatível com vários motores de banco de dados relacionais, incluindo MySQL, PostgreSQL, Oracle, SQL Server e MariaDB.
</p>
  
O RDS oferece recursos como backup e restauração, monitoramento, escalabilidade, segurança e gerenciamento de patches automáticos. O serviço é altamente disponível e tolerante a falhas, com suporte para failover automático e replicação síncrona e assíncrona para garantir a integridade dos dados.
<details><summary> <h3>Recursos</h3></summary>
<ul>
    <li><b>Escalabilidade:</b> O RDS permite aumentar ou diminuir a capacidade do banco de dados de forma rápida e fácil, sem interrupção do serviço.</li>
    <li><b>Disponibilidade:</b> O RDS é projetado para ser altamente disponível e tolerante a falhas, com suporte para failover automático e replicação síncrona e assíncrona.</li>
    <li><b>Backup e restauração:</b> O RDS oferece recursos de backup e restauração integrados, permitindo que você crie backups automáticos e sob demanda e restaure bancos de dados a partir desses backups.</li>
    <li><b>Monitoramento:</b> O RDS oferece recursos de monitoramento para ajudar a rastrear o desempenho do banco de dados e detectar problemas rapidamente.</li>
    <li><b>Gerenciamento de patches:</b> O RDS oferece gerenciamento de patches automáticos para manter o banco de dados atualizado e protegido contra vulnerabilidades de segurança conhecidas.</li>
    <li><b>Segurança:</b> O RDS oferece recursos de segurança avançados, incluindo criptografia de dados em repouso e em trânsito, controle de acesso baseado em função e compatibilidade com o Amazon VPC para proteger o banco de dados em uma rede virtual privada.</li>
</ul> 
</details>

<details><summary><h3>Termos e Conceitos</h3></summary>
  
<ul>
  <li><b>Banco de Dados Relacional:</b> Um banco de dados relacional é uma coleção de tabelas que se relacionam por meio de chaves primárias e chaves estrangeiras.</li>
  <li><b>Instância do Banco de Dados:</b> Uma instância do banco de dados é uma cópia do banco de dados em execução em um servidor dedicado na nuvem. Você pode configurar o tamanho da instância do banco de dados e a quantidade de armazenamento associado a ela.</li>
  <li><b>Snapshot:</b> Um snapshot é uma cópia dos dados do banco de dados em um determinado ponto no tempo. Você pode criar snapshots manualmente ou programá-los para serem criados automaticamente.</li>
  <li><b>Multi-AZ:</b> A opção Multi-AZ cria uma réplica síncrona do banco de dados em uma zona de disponibilidade secundária, aumentando a disponibilidade e a durabilidade do banco de dados.</li>
  <li><b>Leitura Réplica:</b> Uma leitura réplica é uma cópia do banco de dados que pode ser usada para leitura de dados, aumentando a escalabilidade e a performance da consulta.</li>
  <li><b>Endpoint:</b> Um endpoint é um ponto de entrada para acessar um banco de dados RDS. Os endpoints são usados para se conectar a instâncias do banco de dados do RDS.</li>
  <li><b>Parâmetros do Sistema:</b> Os parâmetros do sistema controlam o comportamento de instâncias do banco de dados RDS. Eles podem ser modificados para ajustar o desempenho e a configuração do banco de dados.</li>
  <li><b>Opções de Recuperação de Desastres:</b> O RDS oferece várias opções de recuperação de desastres, incluindo backups automáticos, snapshots manuais e replicação multi-AZ.</li>
  <li><b>Aurora:</b> O Amazon Aurora é um serviço de banco de dados relacional compatível com o MySQL e PostgreSQL, que oferece escalabilidade, durabilidade e desempenho superiores em relação a outros bancos de dados RDS.</li>
</ul>
</details>

<details><summary><h3>Boas Práticas</h3></summary>
 
<ul>
  <li>Definir corretamente as chaves primárias das tabelas para garantir a escalabilidade e a performance da consulta</li>
  <li>Usar o provisionamento de capacidade adequado para evitar o aumento de custos e a diminuição da performance da consulta</li>
  <li>Usar as opções de criptografia do Amazon RDS para proteger dados confidenciais em trânsito e em repouso</li>
  <li>Fazer backups regulares dos dados do banco de dados e testar regularmente a recuperação de desastres</li>
  <li>Usar grupos de segurança do Amazon RDS para controlar o acesso ao banco de dados</li>
  <li>Monitorar o desempenho e o uso do Amazon RDS com o Amazon CloudWatch e definir alertas para anomalias ou problemas de segurança</li>
  <li>Usar múltiplas zonas de disponibilidade para aumentar a disponibilidade e a durabilidade do banco de dados</li>
  <li>Usar o Amazon RDS Performance Insights para obter uma visão detalhada do desempenho do banco de dados e identificar gargalos</li>
</ul> 

Essas boas práticas ajudarão a garantir que o seu banco de dados Amazon RDS esteja otimizado para a escalabilidade, a disponibilidade e a segurança, garantindo que seus aplicativos possam executar de forma eficaz e eficiente. 
</details>

<details><summary><h3>Vantagens de usar RDS em comparação com implantar um banco de dados no EC2</h3></summary>
<ul>
  <li> RDS é um serviço gerenciado:
    <ul>
      <li>Provisionamento automatizado, atualizações de patch de sistema operacional</li>
      <li>Backups contínuos e restauração para um timestamp específico (Ponto no Tempo para Restauração)!</li>
      <li>Painéis de monitoramento</li>
      <li>Replicas de leitura para melhorar o desempenho de leitura</li>
      <li>Janelas de manutenção para atualizações</li>
      <li>Capacidade de dimensionamento (vertical e horizontal)</li>
      <li>Armazenamento suportado pelo EBS</li>
    </ul>
  </li>
  <li>MAS você não pode fazer SSH em suas instâncias</li>
</ul>

#### Arquitetura de Solução RDS

<div align="center">
  <img src="https://thumbs2.imgbox.com/ac/c1/huoLe6f2_t.png">
</div>
</details>

<details><summary><h3>Implantações RDS: Réplicas de Leitura, Multi-AZ</h3></summary>

  Para começar, existe uma aplicação, que lê de um banco de dados RDS principal. Mas digamos que essa aplicação precise escalar as cargas de trabalho de leitura, temos cada vez mais aplicações que precisam ler cada vez mais dados do RDS. A maneira de fazer isso é criando uma Réplica de Leitura. Isso significa que haverá cópias, algumas réplicas do seu banco de dados RDS que serão criadas. E isso permitirá que suas aplicações leiam também dessa Réplica de Leitura. E, portanto, você está distribuindo as leituras para muitos bancos de dados RDS diferentes. Você pode criar até 15 Réplicas de Leitura. Como você pode ver, neste exemplo:

<div align="center">
  <img src="https://thumbs2.imgbox.com/9c/37/EmrqVv9D_t.png">
</div>

É possível ver as Réplicas de Leitura apontando para o banco de dados RDS principal, e as aplicações podem ler de todas elas. Agora, quando se trata de escrever dados, a escrita é feita apenas no banco de dados principal, então a aplicação ainda precisa escrever apenas no único banco de dados RDS central.

<hr/>

Agora temos o Multi-AZ. E isso é útil quando você precisa ter failover em caso de uma falha na Zona de Disponibilidade (AZ). Então, caso a zona de disponibilidade falhe, e isso lhe dá alta disponibilidade. Neste exemplo, as aplicações leem e escrevem do mesmo banco de dados RDS principal. Mas vamos configurar uma replicação cross-AZ, em outra zona de disponibilidade diferente. E este será um banco de dados de failover, e é por isso que é chamado de Multi-AZ porque está em uma AZ diferente. Agora, caso o banco de dados RDS principal falhe, por qualquer motivo, porque talvez haja um problema com ele, ou talvez porque a AZ esteja tendo problemas, então o RDS acionará um failover. E então sua aplicação mudará para o banco de dados de desenvolvedor em uma AZ diferente. Neste caso, os dados são apenas lidos e gravados no banco de dados principal. O banco de dados de failover é passivo, não é acessível até que haja um problema com o banco de dados principal. E você só pode ter uma outra zona de AZ como uma zona de failover:

<div align="center">
  <img src="https://thumbs2.imgbox.com/1b/0a/fEbRtyaX_t.png">
</div>

<hr/>

O último tipo de implantação que você pode fazer é chamado de Multi-Região. Então, isso é para réplicas de leitura, mas desta vez, em vez de estarem na mesma região, elas estão em diferentes regiões. Para dar um exemplo, temos eu-west um para o banco de dados RDS, e vamos criar uma réplica de leitura em us-east-2. E assim, as aplicações em us-east dois podem ler localmente desta réplica de leitura. Mas sempre que esta aplicação precisa escrever dados, as gravações precisam acontecer através da região. E então precisamos escrever os dados para us-west-1. O mesmo se você também tivesse outra região em ap-southeast-2, então na Austrália, você teria os mesmos conceitos. Então, por que você gostaria de ter um tipo de implantação multi-região? Bem, em primeiro lugar, porque você quer configurar uma estratégia de recuperação de desastres, em caso de problema na região. Então, se eu-west-1 estiver tendo um problema regional, então você tem um backup em es-east-2, e é por isso que é uma estratégia de recuperação de desastres. E também, como você pode ver, nossas aplicações que estão em diferentes regiões têm melhor desempenho, porque elas lêem de um banco de dados local, então têm menos latência. Mas finalmente, quando você faz isso, você precisa entender que, como está replicando dados entre regiões, então haverá um custo de replicação associado às transferências de dados entre regiões:

<div align="center">
  <img src="https://thumbs2.imgbox.com/1b/37/jjw8aAks_t.png">
</div>

</details>
  
