DynamoDB

<div align="center">
  <img src="https://static-00.iconduck.com/assets.00/aws-dynamodb-icon-227x256-8rljy0a9.png" width="25%">
</div>
<br/>

O Amazon DynamoDB é um serviço de banco de dados NoSQL totalmente gerenciado que oferece desempenho rápido e previsível com escalabilidade contínua. Ele é projetado para lidar com cargas de trabalho de alto tráfego e pode escalar para cima ou para baixo sem qualquer tempo de inatividade.

As melhores práticas para usar o DynamoDB se concentram em modelagem eficiente de dados, otimização de desempenho, gerenciamento de custos, segurança e disponibilidade.

<details><summary><h3>Componentes</h3></summary>

#### Modelagem Eficiente de Dados

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/3124/3124850.png" width="25%">
</div>

A modelagem eficiente de dados no DynamoDB envolve projetar suas tabelas para suportar os padrões de consulta de sua aplicação. Considerações importantes incluem escolher a chave primária correta, usar índices secundários para flexibilidade adicional de consulta e desnormalizar dados para minimizar operações de leitura.

#### Otimização de Desempenho

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/9732/9732828.png" width="25%">
</div>

A otimização de desempenho concentra-se em usar as chaves de partição corretas para garantir uma distribuição de dados uniforme e minimizar as partições quentes. Também é importante usar os modos de capacidade de leitura e gravação apropriados, aproveitar o DynamoDB Streams para atualizações em tempo real e habilitar o Auto Scaling para ajustar a capacidade conforme necessário. Milhões de solicitações por segundo, trilhões de linhas, 100s de TB de armazenamento. Rápido e consistente em desempenho

#### Gerenciamento de Custos

<div align="center">
  <img src="http://cdn-icons-png.flaticon.com/512/6745/6745218.png" width="25%">
</div>

O gerenciamento de custos no DynamoDB envolve selecionar o modelo de preços correto (sob demanda ou provisionado), monitorar o uso com o AWS Cost Explorer, usar o DynamoDB Accelerator (DAX) para cargas de trabalho intensivas de leitura e aplicar TTL (Time to Live) para excluir automaticamente itens expirados e reduzir os custos de armazenamento.

#### Segurança

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/4744/4744315.png" width="25%">
</div>

As melhores práticas de segurança incluem o uso do AWS Identity and Access Management (IAM) para controlar o acesso aos recursos do DynamoDB, habilitar a criptografia em repouso e em trânsito, implementar controle de acesso fino com políticas do IAM e auditar regularmente sua configuração de segurança com o AWS Security Hub.

#### Disponibilidade

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/9614/9614483.png" width="25%">
</div>

Garantir alta disponibilidade envolve projetar suas tabelas com chaves de partição tolerantes a falhas, habilitar tabelas globais para replicação entre regiões, usar os recursos de backup e restauração do DynamoDB para proteção de dados e monitorar suas tabelas com o Amazon CloudWatch para detectar e responder rapidamente a problemas. Totalmente Gerenciado Altamente disponível com replicação em 3 AZ

</details>

<details><summary><h3>O que o DynamoDB oferece?</h3></summary>

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/15438/15438480.png" width="25%">
</div>

O DynamoDB oferece uma experiência de banco de dados totalmente gerenciada e serverless com segurança integrada, backup, restauração e armazenamento em cache na memória para aplicativos em escala da internet. Ele suporta modelos de dados chave-valor e de documento e fornece capacidades flexíveis de consulta com índices secundários.

</details>

<details><summary><h3>Quais problemas o DynamoDB resolve?</h3></summary>

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/4133/4133589.png" width="25%">
</div>  
  
O DynamoDB aborda vários desafios na gestão de bancos de dados escaláveis e de alto desempenho, incluindo:

- Gerenciamento de alto volume e baixa latência para aplicativos.
- Escalabilidade contínua com tráfego sem tempo de inatividade.
- Simplificação da

 gestão operacional com um serviço totalmente gerenciado.
- Fornecimento de recursos de segurança robustos para proteger dados sensíveis.
- Oferecimento de recuperação robusta de desastres com backup e restauração integrados.

</details>

<details><summary><h3>Quais são os benefícios de usar o DynamoDB?</h3></summary>

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/3588/3588592.png" width="25%">
</div>  

Alguns dos principais benefícios de usar o DynamoDB incluem:

- Escalabilidade: Escalabilidade fácil para lidar com grandes volumes de dados e altas taxas de solicitação.
- Desempenho: Fornece tempos de resposta consistentes de milissegundos de um único dígito.
- Eficiência de Custos: Oferece modelos de preços flexíveis para gerenciar custos de forma eficaz.
- Totalmente Gerenciado: Elimina a necessidade de tarefas de gerenciamento de banco de dados.
- Segurança: Oferece recursos de segurança robustos, incluindo criptografia e controle de acesso fino.

</details>

<details><summary><h3>Como o DynamoDB é usado no desenvolvimento de aplicativos?</h3></summary>

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/1705/1705312.png" width="25%">
</div>  

No desenvolvimento de aplicativos, o DynamoDB é usado para armazenar e recuperar dados com alta disponibilidade e durabilidade. Ele suporta aplicativos em tempo real com o DynamoDB Streams e pode ser integrado a outros serviços da AWS, como o Lambda para computação serverless, o S3 para armazenamento de dados e o CloudWatch para monitoramento.

</details>

<details><summary><h3>Quais são os casos de uso típicos para o DynamoDB?</h3></summary>

<div align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/2833/2833807.png" width="25%">
</div>  
  
Os casos de uso comuns para o DynamoDB incluem:

- Plataformas de comércio eletrônico: Gerenciamento de catálogos de produtos, perfis de usuários e carrinhos de compras.
- Aplicações de jogos: Manipulação de dados de jogadores, classificações e estado do jogo.
- Aplicações IoT: Armazenamento e consulta de dados de séries temporais de dispositivos conectados.
- Plataformas de mídia social: Gerenciamento de interações de usuários, feeds de conteúdo e metadados.
- Serviços financeiros: Processamento de transações e manutenção de informações de conta.
- Análises em tempo real: Armazenamento e análise de fluxos de dados de alta velocidade.

</details>


</details>
<details><summary><h3>Video</h3></summary>
  <div align="center">
    <a href="https://www.youtube.com/watch?v=NCOySd9B6bI" target="_blank">
        <img width="640" height="360" src="https://i.ytimg.com/vi/NCOySd9B6bI/hq720.jpg" alt="Watch Video" />
    </a>
  </div>
</details>


