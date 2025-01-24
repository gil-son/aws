<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:299/1*6vvtwkEFppDrUiTC9ELP2g.png" width="25%">
</div>
<br/>

AWS Glue é um serviço totalmente gerenciado de extração, transformação e carga (Extract, Transform and Load - ETL) fornecido pela Amazon Web Services. Ele simplifica o processo de preparação e carregamento de dados para análises automatizando tarefas como descoberta de dados, catalogação de metadados e geração de código ETL.

AWS Glue é um serviço de integração de dados sem servidor que facilita a descoberta, preparação, movimentação e integração de dados de várias fontes para análises, aprendizado de máquina (ML) e desenvolvimento de aplicativos.


<details><summary><h3>Componentes</h3></summary>

#### Integração de Dados

Escolha seu motor de integração de dados preferido no AWS Glue para suportar seus usuários e cargas de trabalho. Componentes como o Catálogo de Dados, Motor ETL, Jobs ETL e Crawlers facilitam a integração de dados de várias fontes, permitindo que os usuários extraiam, transformem e carreguem dados para análise.

<div align="center">
  <img src="https://d1.awsstatic.com/reInvent/reinvent-2022/glue/Product-Page-Diagram_AWS-Glue_for-Ray%402x.f34b47cf0280c7d843ea457b704ea512bebd91d5.png">
</div>

#### ETL Orientado por Eventos
Os acionadores permitem fluxos de trabalho ETL orientados por eventos, permitindo que os usuários agendem ou acionem jobs ETL com base em eventos como chegada ou alterações de dados. Isso garante que o processamento de dados ocorra em resposta a eventos específicos, permitindo análises em tempo real ou quase em tempo real.
AWS Glue pode executar seus jobs de extração, transformação e carga (ETL) conforme novos dados chegam. Por exemplo, você pode configurar o AWS Glue para iniciar seus jobs ETL assim que novos dados se tornarem disponíveis no Amazon Simple Storage Service (S3).

<div align="center">
  <img src="https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Event-Driven-ETL-Pipelines%20(4).3f3f393bfdb3deefdf183c1cfd39741f99eed6c6.png">
</div>

#### Catálogo de Dados AWS Glue

Você pode usar o Catálogo de Dados para descobrir e pesquisar rapidamente vários conjuntos de dados da AWS sem mover os dados. Uma vez catalogados, os dados estão imediatamente disponíveis para pesquisa e consulta usando o Amazon Athena, Amazon EMR e o Amazon Redshift Spectrum.
O Catálogo de Dados Glue serve como um repositório de metadados centralizado para armazenar informações sobre fontes de dados, esquemas e tabelas. Facilita a descoberta, pesquisa e compreensão de dados, aumentando a eficiência da gestão e análise de dados.

<div align="center">
  <img src="https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Unified-View%20(3).cbbd4734e6a79cc3d2569064d0010605a0a307ae.png">
</div>

#### Job ETL sem código

O AWS Glue Studio facilita a criação, execução e monitoramento visual de jobs ETL do AWS Glue. Você pode criar jobs ETL que movem e transformam dados usando um editor de arrastar e soltar, e o AWS Glue gera automaticamente o código.

<div align="center">
  <img src="https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Elixir%20(2).522ef785088de982530b9fdde4c8be146562fa0f.png">
</div>

#### Gerenciamento e monitoramento da qualidade dos dados

O AWS Glue Data Quality automatiza a criação, gerenciamento e monitoramento de regras de qualidade de dados para garantir dados de alta qualidade em seus data lakes e pipelines.

<div align="center">
  <img src="https://d1.awsstatic.com/reInvent/reinvent-2022/glue/Product-Page-Diagram_AWS-Glue_Data-Quality%402x.121ffd889bd81b67268beed4f6f1424454ebae4d.png">
</div>

#### Preparação de dados

Com o AWS Glue DataBrew, você pode explorar e experimentar dados diretamente do seu data lake, data warehouses e bancos de dados, incluindo Amazon S3, Amazon Redshift, AWS Lake Formation, Amazon Aurora e Amazon Relational Database Service (RDS). Você pode escolher entre mais de 250 transformações pré-criadas no DataBrew para automatizar tarefas de preparação de dados, como filtragem de anomalias, padronização de formatos e correção de valores inválidos.

<div align="center">
  <img src="https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Self-Service-Visual-Data%20(2).0e1a87155040f71dcc92464a283f1adddd39cf85.png">
</div>

</details>


<details><summary> <h3>O que o AWS Glue faz?</h3></summary>
O AWS Glue automatiza o processo de ETL, permitindo que os usuários preparem e carreguem facilmente dados para análises. Ele descobre e cataloga metadados sobre várias fontes de dados, incluindo bancos de dados, tabelas e esquemas. Com o AWS Glue, os usuários podem criar e executar jobs ETL sem a necessidade de provisionar ou gerenciar infraestrutura.
</details>

<details><summary> <h3>Quais problemas o AWS Glue resolve?</h3></summary>
  
O AWS Glue aborda vários desafios no processo de preparação e ETL de dados, incluindo:

- Esforço manual: Processos tradicionais de ETL exigem um esforço manual significativo para descoberta de dados, mapeamento de esquema e criação de jobs ETL.
- Escalabilidade: Gerenciar e dimensionar infraestrutura ETL para lidar com grandes volumes de dados pode ser complexo e demorado.
- Integração de dados: Integrar dados de fontes díspares com formatos e estruturas variadas pode ser desafiador sem uma solução centralizada.

</details>


<details><summary><h3>Quais são os benefícios do AWS Glue?</h3></summary>

Alguns benefícios chave do AWS Glue incluem:

- Automação: O AWS Glue automatiza muitas tarefas envolvidas no processo de ETL, reduzindo a necessidade de intervenção manual.
- Escalabilidade: Como um serviço totalmente gerenciado, o AWS Glue pode dimensionar automaticamente recursos para lidar com cargas de trabalho e volumes de dados variáveis.
- Economia de custos: Os usuários pagam apenas pelos recursos consumidos por seus jobs ETL, eliminando a necessidade de investimento inicial em infraestrutura.
- Catalogação de dados: O AWS Glue fornece um repositório de metadados centralizado (Catálogo de Dados Glue) que facilita a descoberta, pesquisa e compreensão de ativos de dados.
    
</details>


<details><summary><h3>Qual é o motor de integração de dados suportado pelo AWS Glue?</h3></summary>
O AWS Glue suporta o Apache Spark e o Apache PySpark como seus motores de integração de dados. Esses motores fornecem capacidades de processamento distribuído para executar jobs ETL em escala.
</details>


<details><summary> <h3>Como o AWS Glue é usado para arquitetar uma solução na nuvem?</h3></summary>
Em uma arquitetura de solução na nuvem, o AWS Glue pode ser usado para orquestrar e automatizar o processo de preparação e ETL de dados. Ele se integra a outros serviços da AWS, como Amazon S3, Amazon Redshift e Amazon RDS para extrair dados de várias fontes, transformá-los conforme necessário e carregá-los em destinos de destino para análise.
</details>

<details><summary><h3>Quais são os casos de uso típicos para o AWS Glue?</h3></summary>
Casos de uso comuns para o AWS Glue incluem:

- Armazenamento de dados: Preparação e carregamento de dados em data warehouses para análises e relatórios.
- Data lakes: Ingestão, transformação e catalogação de dados para armazenamento em data lakes.
- Análises em tempo real: Processamento e análise de dados em streaming em tempo real para obter insights.
- Migração de dados: Movimentação de dados entre diferentes sistemas de armazenamento ou bancos de dados.  
</details>

<details><summary><h3>Videos</h3></summary>
  <div align="center">
    <a href="https://www.youtube.com/watch?v=HlVOQ5eMUf8" target="_blank">
        <img width="640" height="360" src="https://i.ytimg.com/vi/HlVOQ5eMUf8/maxresdefault.jpg" alt="Watch Video" />
    </a>
  </div>
  <hr/>
    <div align="center">
    <a href="https://www.youtube.com/watch?v=eDzUaGyVoyI" target="_blank">
        <img width="640" height="360" src="https://i.ytimg.com/vi_webp/eDzUaGyVoyI/maxresdefault.webp" alt="Watch Video" />
    </a>
  </div>
</details>
