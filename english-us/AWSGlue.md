AWS Glue

<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:299/1*6vvtwkEFppDrUiTC9ELP2g.png" width="25%">
</div>
<br/>

AWS Glue is a fully managed extract, transform, and load (ETL) service provided by Amazon Web Services. It simplifies the process of preparing and loading data for analytics by automating tasks such as discovering data, cataloging metadata, and generating ETL code.

AWS Glue is a serverless data integration service that makes it easier to discover, prepare, move, and integrate data from multiple sources for analytics, machine learning (ML), and application development.


<details><summary><h3>Components</h3></summary>

#### Data Integration

Choose your preferred data integration engine in AWS Glue to support your users and workloads. Components such as the Data Catalog, ETL Engine, ETL Jobs, and Crawlers facilitate the integration of data from various sources, enabling users to extract, transform, and load data for analysis.

<div align="center">
  <img src="https://d1.awsstatic.com/reInvent/reinvent-2022/glue/Product-Page-Diagram_AWS-Glue_for-Ray%402x.f34b47cf0280c7d843ea457b704ea512bebd91d5.png">
</div>

#### Event-driven ETL
Triggers enable event-driven ETL workflows by allowing users to schedule or trigger ETL jobs based on events such as data arrival or changes. This ensures that data processing occurs in response to specific events, enabling real-time or near-real-time analytics.
AWS Glue can run your extract, transform, and load (ETL) jobs as new data arrives. For example, you can configure AWS Glue to initiate your ETL jobs to run as soon as new data becomes available in Amazon Simple Storage Service (S3).

<div align="center">
  <img src="https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Event-Driven-ETL-Pipelines%20(4).3f3f393bfdb3deefdf183c1cfd39741f99eed6c6.png">
</div>

#### AWS Glue Data Catalog

You can use the Data Catalog to quickly discover and search multiple AWS datasets without moving the data. Once the data is cataloged, it is immediately available for search and query using Amazon Athena, Amazon EMR, and Amazon Redshift Spectrum.
The Glue Data Catalog serves as a centralized metadata repository for storing information about data sources, schemas, and tables. It facilitates data discovery, search, and understanding, enhancing the efficiency of data management and analytics.

<div align="center">
  <img src="https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Unified-View%20(3).cbbd4734e6a79cc3d2569064d0010605a0a307ae.png">
</div>

#### No-code ETL Job

AWS Glue Studio makes it easier to visually create, run, and monitor AWS Glue ETL jobs. You can build ETL jobs that move and transform data using a drag-and-drop editor, and AWS Glue automatically generates the code.

<div align="center">
  <img src="https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Elixir%20(2).522ef785088de982530b9fdde4c8be146562fa0f.png">
</div>

#### Manage and monitor data quality

AWS Glue Data Quality automates data quality rule creation, management, and monitoring to help ensure high quality data across your data lakes and pipelines.

<div align="center">
  <img src="https://d1.awsstatic.com/reInvent/reinvent-2022/glue/Product-Page-Diagram_AWS-Glue_Data-Quality%402x.121ffd889bd81b67268beed4f6f1424454ebae4d.png">
</div>

#### Data preparation

With AWS Glue DataBrew, you can explore and experiment with data directly from your data lake, data warehouses, and databases, including Amazon S3, Amazon Redshift, AWS Lake Formation, Amazon Aurora, and Amazon Relational Database Service (RDS). You can choose from over 250 prebuilt transformations in DataBrew to automate data preparation tasks such as filtering anomalies, standardizing formats, and correcting invalid values.

<div align="center">
  <img src="https://d1.awsstatic.com/products/aws-glue/product-page-diagram_AWS-Glue_Self-Service-Visual-Data%20(2).0e1a87155040f71dcc92464a283f1adddd39cf85.png">
</div>

</details>


<details><summary> <h3>What does AWS Glue do?</h3></summary>
AWS Glue automates the ETL process, enabling users to easily prepare and load data for analytics. It discovers and catalogs metadata about various data sources, including databases, tables, and schemas. With AWS Glue, users can create and run ETL jobs without the need to provision or manage infrastructure.
</details>

<details><summary> <h3>What problems does AWS Glue solve?</h3></summary>
  
AWS Glue addresses several challenges in the data preparation and ETL process, including:

- Manual effort: Traditional ETL processes require significant manual effort for data discovery, schema mapping, and ETL job creation.
- Scalability: Managing and scaling ETL infrastructure to handle large volumes of data can be complex and time-consuming.
- Data integration: Integrating data from disparate sources with varying formats and structures can be challenging without a centralized solution.

</details>


<details><summary><h3>What are the benefits of AWS Glue?</h3></summary>

Some key benefits of AWS Glue include:

- Automation: AWS Glue automates many tasks involved in the ETL process, reducing the need for manual intervention.
- Scalability: As a fully managed service, AWS Glue can automatically scale resources to handle varying workloads and data volumes.
- Cost-effectiveness: Users pay only for the resources consumed by their ETL jobs, eliminating the need for upfront investment in infrastructure.
- Data cataloging: AWS Glue provides a centralized metadata repository (Glue Data Catalog) that makes it easy to discover, search, and understand data assets.
    
</details>


<details><summary><h3>What is the data integration engine supported by AWS Glue?</h3></summary>
AWS Glue supports Apache Spark and Apache PySpark as its data integration engines. These engines provide distributed processing capabilities for executing ETL jobs at scale.
</details>


<details><summary> <h3>How is AWS Glue used to architect a cloud solution?</h3></summary>
In a cloud solution architecture, AWS Glue can be used to orchestrate and automate the data preparation and ETL process. It integrates with other AWS services such as Amazon S3, Amazon Redshift, and Amazon RDS to extract data from various sources, transform it as needed, and load it into target destinations for analysis.
</details>

<details><summary><h3>What are typical use cases for AWS Glue?</h3></summary>
Common use cases for AWS Glue include:

- Data warehousing: Preparing and loading data into data warehouses for analytics and reporting.
- Data lakes: Ingesting, transforming, and cataloging data for storage in data lakes.
- Real-time analytics: Processing and analyzing streaming data in real-time to derive insights.
- Data migration: Moving data between different storage systems or databases.  
</details>


<details><summary><h3>Video</h3></summary>
  <div align="center">
    <a href="https://www.youtube.com/watch?v=dQnRP6X8QAU" target="_blank">
        <img width="640" height="360" src="https://i.ytimg.com/vi_webp/dQnRP6X8QAU/maxresdefault.webp" alt="Watch Video" />
    </a>
  </div>
</details>



