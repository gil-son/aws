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
  
