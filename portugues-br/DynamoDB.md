DynamoDB

<div align="center">
  <img src="https://www.datarain.com.br/wp-content/uploads/2020/08/DybamoDB-logo.png" width="35%">
</div>
O Amazon DynamoDB é um banco de dados NoSQL totalmente gerenciado e escalável, que fornece armazenamento e recuperação de dados de alto desempenho e baixa latência. O DynamoDB foi projetado para ser uma solução de banco de dados altamente disponível e tolerante a falhas, capaz de lidar com grandes volumes de dados e tráfego de leitura/gravação.

<details><summary> <h3>Recursos</h3></summary>
<ul>
    <li><b>Escalabilidade:</b> O DynamoDB pode escalar horizontalmente de forma automática e rápida, sem interrupção de serviço, para suportar grandes volumes de dados e tráfego.</li>
    <li><b>Desempenho:</b> O DynamoDB oferece um desempenho de leitura e gravação de dados muito alto, com latências de milissegundos.</li>
    <li><b>Disponibilidade:</b> O DynamoDB é projetado para ser altamente disponível, com replicação de dados síncrona e assíncrona para garantir a tolerância a falhas.</li>
    <li><b>Gerenciamento de acesso:</b> O DynamoDB oferece recursos de controle de acesso granular, permitindo que você defina permissões de acesso a tabelas e itens de tabela com base em papéis do IAM, políticas de acesso e chaves de acesso.</li>
    <li><b>Backup e restauração:</b> O DynamoDB oferece recursos de backup e restauração integrados, permitindo que você crie backups automáticos e sob demanda de tabelas e restaure tabelas a partir desses backups.</li>
</ul> 
</details>


<details><summary> <h3>Termos e conceitos</h3></summary>
<ul>
<li><b>Tabelas:</b> O DynamoDB é um banco de dados NoSQL, e todas as informações são armazenadas em tabelas. Cada tabela contém várias linhas (itens) e cada linha pode ter um número variável de colunas (atributos).</li>
<li><b>Partições:</b> O DynamoDB é projetado para ser altamente escalável, e os dados são distribuídos em partições para garantir alta disponibilidade e desempenho. Cada partição é um conjunto de itens que compartilham a mesma chave de partição.</li>
<li><b>Chave primária:</b> Cada item em uma tabela do DynamoDB deve ter uma chave primária exclusiva que identifica o item. Existem dois tipos de chave primária no DynamoDB: chave de partição e chave de partição e de ordenação.</li>
<li><b>Chave de Ordenação:</b> A chave de ordenação é um atributo adicional que pode ser usado para ordenar itens dentro de uma partição.</li>
<li><b>Índices:</b> O DynamoDB oferece suporte a dois tipos de índices: índices de chave e índices globais. Os índices de chave são criados com base em um ou mais atributos da tabela, enquanto os índices globais permitem consultas em qualquer atributo da tabela.</li>
<li><b>Consistência:</b> O DynamoDB oferece suporte a duas opções de consistência para leituras: consistência forte e consistência eventual.</li>
<li><b>Capacidade:</b> O DynamoDB é escalável horizontalmente e permite que você ajuste a capacidade de leitura/gravação para atender às necessidades de desempenho da sua aplicação. A capacidade de leitura/gravação é medida em unidades de leitura/gravação, e você pode provisionar a quantidade de unidades necessárias para atender aos requisitos de tráfego da sua aplicação.</li>
<li><b>Streams:</b> O DynamoDB Streams é um recurso que permite capturar mudanças em tabelas do DynamoDB em tempo real e processá-las usando serviços da AWS, como o AWS Lambda.</li>
<li><b>Consulta e Filtragem:</b> O DynamoDB permite usar expressões de consulta e filtragem em uma tabela.</li>
<li><b>Transações:</b> O DynamoDB suporta transações atômicas que permitem agrupar várias operações em uma única transação.</li>
</ul>
</details>

<details><summary> <h3>Boas Práticas</h3></summary>
<ul>
  <li>Definir corretamente as chaves primárias das tabelas para garantir a escalabilidade e a performance da consulta</li>
  <li>Usar o provisionamento de capacidade adequado para evitar o aumento de custos e a diminuição da performance da consulta</li>
  <li>Usar as opções de criptografia do DynamoDB para proteger dados confidenciais</li>
  <li>Usar transações para manter a consistência dos dados em operações complexas que envolvem várias tabelas ou itens</li>
  <li>Configurar políticas de controle de acesso apropriadas para limitar o acesso às tabelas</li>
  <li>Usar o Amazon CloudWatch para monitorar o desempenho e a utilização do DynamoDB e definir alertas para anomalias ou problemas de segurança</li>
</ul>
</details>
