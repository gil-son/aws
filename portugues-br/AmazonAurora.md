Aurora

<div align="center">
  <img src="https://bluesentry.cloud/wp-content/uploads/2021/02/amazon_aurora.png" width="40%">
</div>
<br>
<br>
<p>
Amazon Aurora é um serviço de banco de dados relacional compatível com MySQL e PostgreSQL fornecido pela AWS. Ele oferece escalabilidade, durabilidade e desempenho superiores em comparação com outros bancos de dados RDS.
</p>

A arquitetura do Aurora foi projetada para fornecer alto desempenho e disponibilidade para cargas de trabalho de banco de dados. Ele usa um sistema de armazenamento distribuído e tolerante a falhas replicado em várias Zonas de Disponibilidade (AZs) para aumentar a confiabilidade.
<details><summary><h3>Recursos</h3></summary>
<ul>
    <li><b>Escalabilidade:</b> O Aurora fornece escalabilidade contínua e automática para lidar com cargas de trabalho em crescimento sem tempo de inatividade.</li>
    <li><b>Alta Disponibilidade:</b> O Aurora é projetado para alta disponibilidade com failover automático e backups contínuos para garantir a durabilidade dos dados.</li>
    <li><b>Desempenho:</b> O Aurora oferece alto desempenho com um sistema de armazenamento especialmente projetado e arquitetura distribuída otimizada para cargas de trabalho de banco de dados.</li>
    <li><b>Compatibilidade:</b> O Aurora é compatível com MySQL e PostgreSQL, permitindo a migração fácil de aplicativos e ferramentas existentes.</li>
    <li><b>Backups e Restauração:</b> O Aurora oferece backups contínuos e recuperação até um determinado momento, permitindo restaurar o banco de dados para qualquer segundo dentro do período de retenção.</li>
    <li><b>Segurança:</b> O Aurora fornece recursos avançados de segurança, incluindo criptografia em repouso e em trânsito, autenticação de banco de dados IAM e suporte a VPC.</li>
    <li><b>Comparação:</b> O Aurora é "otimizado pela AWS" e afirma uma melhoria de desempenho de 5x em relação ao MySQL no RDS, mais de 3x o desempenho do Postgres no RDS</li>
    <li><b>Custo:</b> Não está incluído no nível gratuito</li>
</ul> 
</details>
<details><summary><h3>Termos e Conceitos</h3></summary>
<ul>
  <li><b>Cluster:</b> Um cluster Aurora consiste em uma instância primária e até 15 réplicas de leitura. A instância primária lida com operações de gravação, enquanto as réplicas de leitura podem ser usadas para escalonamento de leitura e failover.</li>
  <li><b>Instância:</b> Uma instância Aurora é um único ponto de extremidade em um cluster Aurora. Pode ser uma instância primária ou uma réplica de leitura.</li>
  <li><b>Armazenamento:</b> O Aurora usa um sistema de armazenamento distribuído que se dimensiona automaticamente para até 128 terabytes por instância de banco de dados. Ele fornece desempenho e durabilidade consistentes e altos.</li>
  <li><b>Ponto de Extremidade:</b> Um ponto de extremidade é um endereço de rede que os clientes usam para se conectar a uma instância de banco de dados Aurora.</li>
  <li><b>Failover Automático:</b> O Aurora detecta e substitui automaticamente uma instância primária em caso de falha, minimizando o tempo de inatividade.</li>
  <li><b>Performance Insights:</b> O Performance Insights do Aurora ajuda a monitorar o desempenho do banco de dados e analisar problemas de desempenho em tempo real.</li>
</ul>
</details>
<details><summary><h3>Melhores Práticas</h3></summary>
<ul>
  <li>Projetar tabelas e índices para aproveitar a arquitetura distribuída do Aurora para um desempenho ideal.</li>
  <li>Monitorar regularmente o desempenho do banco de dados usando o Performance Insights do Aurora e configurar alertas para anomalias de desempenho.</li>
  <li>Usar autenticação de banco de dados IAM para gerenciar com segurança o acesso ao banco de dados e eliminar a necessidade de senhas de banco de dados.</li>
  <li>Ativar a criptografia em repouso e em trânsito para proteger dados confidenciais armazenados em bancos de dados Aurora.</li>
  <li>Testar regularmente backups e restaurações até um determinado momento para garantir a recuperabilidade dos dados em caso de falha.</li>
  <li>Implementar implantações multi-AZ para aumentar a disponibilidade e a tolerância a falhas.</li>
  <li>Escalar operações de leitura usando réplicas de leitura do Aurora para descarregar o tráfego de leitura da instância primária.</li>
</ul> 
Essas melhores práticas ajudarão a otimizar o desempenho, a disponibilidade e a segurança do seu banco de dados Aurora, garantindo uma operação confiável para seus aplicativos.
</details>

<details><summary> <h3>Vantagem de usar Aurora versus implantar BD no EC2</h3></summary>
<ul>
  <li> Aurora é um serviço gerenciado:
    <ul>
      <li>Provisionamento automatizado, aplicação de patches do SO</li>
      <li>Backups contínuos e recuperação até um determinado momento</li>
      <li>Painéis de monitoramento e Performance Insights</li>
      <li>Réplicas de leitura para melhorar o desempenho de leitura</li>
      <li>Janelas de manutenção para atualizações</li>
      <li>Capacidade de dimensionamento (vertical e horizontal)</li>
      <li>Armazenamento com dimensionamento e durabilidade automáticos</li>
    </ul>
  </li>
  <li>Mas você não pode fazer SSH em suas instâncias</li>
</ul>

#### Arquitetura de Solução Aurora 

<div align="center">
  <img src="https://thumbs2.imgbox.com/6a/f6/RxlEsCvg_t.png">
</div>

</details>

<details><summary> <h3>Amazon Aurora Serverless</h3></summary>

Amazon Aurora Serverless é uma configuração nativa

 da nuvem e sob demanda do Amazon Aurora que ajusta automaticamente a capacidade do banco de dados para atender às necessidades do aplicativo. Ele oferece escalabilidade perfeita e eficiência de custos ao dimensionar automaticamente para cima ou para baixo com base no uso real. Com o Aurora Serverless, os usuários não precisam mais gerenciar instâncias de banco de dados, sendo ideal para aplicativos com cargas de trabalho imprevisíveis ou variáveis.

<ul>
    <li>Instanciação automática de banco de dados e dimensionamento automático com base no uso real</li>
    <li>O PostgreSQL e o MySQL são ambos suportados como BDs Aurora Serverless</li>
    <li>Não há necessidade de planejamento de capacidade</li>
    <li>Mínima sobrecarga de gerenciamento</li>
    <li>Pagamento por segundo, pode ser mais econômico</li>
</ul>

#### Casos de Uso

O Aurora Serverless é bom para cargas de trabalho infrequentes, intermitentes ou imprevisíveis.

Bem, do ponto de vista do cliente, é super fácil. Ele se conecta a uma frota de proxies gerenciada pelo Aurora. E o Aurora, nos bastidores, vai instanciar instâncias de banco de dados quando precisar escalar para cima ou para baixo. E esses bancos de dados do Aurora vão compartilhar o mesmo volume de armazenamento, não importa o que aconteça. Então, do ponto de vista, se você ver o Aurora sem sobrecarga de gerenciamento e assim por diante, pense no Aurora Serverless.

<div align="center" width="40%">
  <img src="https://thumbs2.imgbox.com/cd/63/C1daqgj1_t.png">
</div>

</details>

</details>
