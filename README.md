# AWS

<div align="center">
  <img src="https://i.ibb.co/6PMkBpW/AWS-Services-Shelf.png" width="40%">
</div>



<details><summary> <h3>Ler em Português - BR</h3></summary>
<hr/>

<details><summary><h4>Introdução</h4></summary>
<br>
A AWS (Amazon Web Services) é uma plataforma na nuvem da Amazon que oferece diversos serviços para empresas e desenvolvedores. Para entender melhor, imagine que a AWS é como uma grande loja de ferramentas, onde você pode alugar tudo o que precisa para construir sua casa (ou no caso, sua aplicação na nuvem).

Lá você encontra desde martelos simples, como o S3 (para armazenamento de arquivos), até ferramentas mais complexas, como o EC2 (para criação de servidores virtuais). E se precisar de algo ainda mais específico, é só dar uma olhadinha no catálogo da loja, que tem de tudo um pouco.

Ah, e tem mais! Na AWS, você só paga pelo que usar. Ou seja, se precisar de uma furadeira por apenas uma hora, é só alugar por uma hora e pagar só por esse período. E se precisar de uma furadeira por mais tempo, é só renovar o aluguel. Assim, você não precisa gastar dinheiro à toa com ferramentas que não vai usar.

Além disso, a AWS tem uma equipe de segurança que fica de olho em tudo o tempo todo. Então, você pode ficar tranquilo que suas ferramentas (ou sua aplicação) estão seguras na nuvem da Amazon.

Resumindo, a AWS é como "uma loja de ferramentas na nuvem", onde você aluga só o que precisa e tem a segurança garantida pela equipe da Amazon. Agora é só escolher as ferramentas certas para construir sua casa (ou sua aplicação) e colocar a mão na massa!

</details>

<details><summary><h4>Por onde começar?</h4></summary>
<br>

O AWS Identity and Access Management (IAM) é altamente recomendado para iniciantes, pois oferece uma maneira segura de começar a utilizar os serviços da AWS desde o início. Ele ajuda a evitar erros comuns que poderiam resultar em violações de segurança. Além disso, o IAM é um serviço gratuito da AWS e é conhecido por sua facilidade de uso.

Se desejar explorar mais sobre o IAM e outros recursos relacionados, você pode conferir a seção de Sumário. Para acessar diretamente, clique <a href="https://github.com/gil-son/aws/blob/main/portugues-br/IAM.md">aqui</a>.

<div align="center">
<img src="https://thumbs2.imgbox.com/0a/27/EsIpVA0r_t.png" width="60%"/>
</div>


Simultaneamente, é aconselhável familiarizar-se com os conceitos básicos de computação em nuvem. Isso inclui entender a razão por trás do surgimento da computação em nuvem, as mudanças na infraestrutura antes e depois de sua introdução, os diversos tipos de computação em nuvem, estratégias de consumo, escolha de regiões, entre outros. Para obter informações detalhadas sobre esses conceitos, <a href="https://github.com/gil-son/aws/blob/main/portugues-br/Basico.md">consulte</a> 

</details>



<details><summary><h4>Sumário</h4></summary>
<br>
<table>
 <tr align="center">
     <td>Categoria</td>
     <td>Modelo de Serviço</td>
     <td>Recurso</td>
     <td>img</td>
     <td>Info</td>
 </tr>
  
  <tr align="center">
     <td>Segurança, Indentidade e conformidade</td>
     <td>Integra com qualquer modelo de serviço</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/IAM.md">IAM</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/IAM.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/0ebc580ae6450fce8762fad1bff32e7b-0841c1f0e7c5788b88d07a7dbcaceb6e.svg" /></a></td>
     <td>O IAM da AWS é um serviço de gerenciamento de identidades e acessos que permite controlar o acesso aos recursos da AWS por usuários e aplicativos.</td>
 </tr>

<tr align="center">
     <td rowspan="3">Computação</td>
     <td>PaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/ElasticBeanstalk.md">ElasticBeanstalk</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/ElasticBeanstalk.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d43b67a293d39d11b046bd1813c804cb-4bc0ce71c93950e1ad695b25a4f1d4b5.svg" /></a></td>
     <td>O Elastic Beanstalk é um serviço gerenciado pela AWS que facilita o deploy e a escalabilidade de aplicações web de forma rápida e simples.</td>
 </tr> 
  
 <tr align="center">
     <td>IaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/EC2.md">EC2</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/EC2.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /></a></td>
     <td>O Amazon EC2 é um serviço de computação em nuvem que permite configurar e executar facilmente servidores virtuais na nuvem da Amazon, escalando verticalmente ou horizontalmente a capacidade de computação de acordo com as necessidades da sua aplicação, pagando apenas pelos recursos que você usa.</td>
 </tr>

 <tr align="center">
     <td>FaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Lambda.md">Lambda</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Lambda.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/945f3fc449518a73b9f5f32868db466c-926961f91b072604c42b7f39ce2eaf1c.svg" /></a></td>
     <td>AWS Lambda é um serviço serverless que permite a execução de código em resposta a eventos, sem a necessidade de gerenciamento de servidores.</td>
 </tr>

<tr align="center">
     <td rowspan="3">Rede e Entrega de Conteúdo</td>
     <td>Gerenciamento de API</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/APIGateway.md">API Gateway</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/APIGateway.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/fb0cde6228b21d89ec222b45efec54e7-0856e92285f4e7ed254b2588d1fe1829.svg" /></a></td>
     <td>O Amazon API Gateway é uma poderosa ferramenta da AWS que permite aos desenvolvedores criar, publicar, monitorar e gerenciar APIs de forma segura e escalável, facilitando a integração entre diferentes serviços e aplicações.</td>
 </tr>

 <tr align="center">
     <td>Gerenciamento de DNS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Route53.md">Route 53</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Route53.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/f5d2c00d40914bff4f82f29f9ef768bc-53a84099cf556710383a52b4612a8612.svg" /></a></td>
     <td>O Amazon Route 53 é o serviço de sistema de nomes de domínio (DNS) e entrega de conteúdo (CDN) da AWS, oferecendo registro de domínio, resolução de DNS e direcionamento de tráfego para otimizar a disponibilidade e desempenho de aplicações na internet.</td>
 </tr>

<tr align="center">
     <td rowspan="6">Integra com qualquer modelo de serviço</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/LoadBalancer.md">Load Balancer</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/LoadBalancer.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/7177e919b32ad97825f95e902595014b-1594766d92813b5baeb706c453f91de0.svg" /></a></td>
     <td>O balanceamento de carga otimiza a distribuição de recursos, garantindo um desempenho eficiente e confiável ao distribuir o tráfego de rede de entrada entre vários servidores ou recursos.</td>
 </tr>

<tr align="center">
     <td>Armazenar</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/S3.md">S3</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/S3.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/c0828e0381730befd1f7a025057c74fb-43acc0496e64afba82dbc9ab774dc622.svg" /></a></td>
     <td>O Amazon S3 é um serviço de armazenamento de objetos altamente escalável e durável da AWS, projetado para armazenar e recuperar quantidades massivas de dados de qualquer lugar na web.</td>
 </tr>
 
<tr align="center">
     <td rowspan="2">Banco de Dados</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/DynamoDB.md">DynamoDB</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/DynamoDB.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/6f419a45e63123b4c16bd679549610f6-87862c68693445999110bbd6a467ce88.svg" /></a></td>
     <td>DynamoDB é um serviço de banco de dados NoSQL, totalmente gerenciado, altamente escalável, flexível e com alta performance</td>
 </tr>
  
<tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/RDS.md">RDS</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/RDS.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/1d374ed2a6bcf601d7bfd4fc3dfd3b5d-c9f69416d978016b3191175f35e59226.svg" /></a></td>
     <td>O Amazon RDS é um serviço de banco de dados gerenciado na nuvem que facilita a configuração, operação e escalabilidade de bancos de dados relacionais, como MySQL, PostgreSQL, Oracle, SQL Server e outros.</td>
 </tr>
 
<tr align="center">
     <td rowspan="2">Gerenciamento e Governança</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/CloudWatch.md">CloudWatch</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/CloudWatch.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/8f57ebd825a828e205b2dde223ba17e4-6af63a22dc297f8041286760ee8cd2c9.svg" /></a></td>
     <td>O CloudWatch é um serviço de monitoramento e observabilidade da AWS que permite coletar, armazenar, visualizar e alertar sobre dados de logs e métricas em tempo real para recursos em nuvem.</td>
 </tr>
  
 <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AutoScaling.md">AutoScaling</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AutoScaling.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/8c4ff0bc6eb31f0dcf6f6765b4259429-8b46577d889db4c0abac90ec6961f188.svg" /></a></td>
     <td>O Auto Scaling da AWS é um serviço que ajusta automaticamente a capacidade de recursos computacionais para atender à demanda em tempo real, garantindo eficiência e alta disponibilidade.</td>
 </tr> 
  
</table>
</details>
</details>

<details><summary> <h3>Read in English - US</h3></summary>
<hr/>

<details><summary><h4>Introduction</h4></summary>
<br>

AWS (Amazon Web Services) is a cloud platform from Amazon that offers various services for businesses and developers. To better understand, imagine that AWS is like a large tool store, where you can rent everything you need to build your house (or in this case, your application in the cloud).

There you can find simple hammers like S3 (for file storage) to more complex tools like EC2 (for creating virtual servers). And if you need something even more specific, just take a look at the store catalog, which has a little bit of everything.

Oh, and there's more! In AWS, you only pay for what you use. That is, if you need a drill for just one hour, just rent it for an hour and pay only for that period. And if you need a drill for longer, just renew the rental. So, you don't have to waste money on tools that you won't use.

In addition, AWS has a security team that keeps an eye on everything all the time. So, you can rest assured that your tools (or your application) are secure in Amazon's cloud.

In summary, AWS is like "a cloud tool store", where you rent only what you need and have security guaranteed by Amazon's team. Now just choose the right tools to build your house (or your application) and get to work!

</details>

<details><summary><h4>Where to start?</h4></summary>
<br>

The AWS Identity and Access Management (IAM) is highly recommended for beginners as it provides a secure way to start using AWS services from the outset. It helps prevent common errors that could lead to security breaches. Additionally, IAM is a free AWS service known for its user-friendly interface.

If you wish to explore more about IAM and other related features, you can check the Summary section. To access it directly, <a href="https://github.com/gil-son/aws/blob/main/english-us/IAM.md"> click here</a>.

<div align="center">
<img src="https://thumbs2.imgbox.com/0a/27/EsIpVA0r_t.png" width="60%"/>
</div>

Simultaneously, it is advisable to familiarize yourself with the fundamental concepts of cloud computing. This includes understanding the reasons behind the emergence of cloud computing, the changes in infrastructure before and after its introduction, various types of cloud computing, consumption strategies, region selection, among other aspects. For detailed information on these concepts, <a href="https://github.com/gil-son/aws/blob/main/english-us/Basic.md"> refer to this link.</a>

</details>

<details><summary><h4>Summary</h4></summary>
<br>
 <table>
 <tr align="center">
     <td>Category</td>
     <td>Service Model</td>
     <td>Resource</td>
     <td>img</td>
     <td>Info</td>
 </tr>
  <tr align="center">
     <td>Security, Identity and Compliance</td>
     <td>Integrate with any service model</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/IAM.md">IAM</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/IAM.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/0ebc580ae6450fce8762fad1bff32e7b-0841c1f0e7c5788b88d07a7dbcaceb6e.svg" /></a></td>
     <td>AWS IAM is an identity and access management service that enables control of access to AWS resources by users and applications.</td>
 </tr>



<tr align="center">
     <td rowspan="3">Compute</td>
     <td>PaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/ElasticBeanstalk.md">ElasticBeanstalk</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/ElasticBeanstalk.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d43b67a293d39d11b046bd1813c804cb-4bc0ce71c93950e1ad695b25a4f1d4b5.svg" /></a></td>
     <td>Elastic Beanstalk is an AWS-managed service that simplifies the deployment and scalability of web applications quickly and easily..</td>
 </tr>    
   
 <tr align="center">
     <td>IaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/EC2.md">EC2</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/EC2.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /></a></td>
     <td>Amazon EC2 is a cloud computing service that allows easy configuration and running of virtual servers in the Amazon cloud, scaling compute capacity vertically or horizontally based on your application needs, and paying only for the resources you use.</td>
 </tr>

 <tr align="center">
     <td>FaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lambda.md">Lambda</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lambda.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/945f3fc449518a73b9f5f32868db466c-926961f91b072604c42b7f39ce2eaf1c.svg" /></a></td>
     <td>AWS Lambda is a serverless service that allows for code execution in response to events, without the need for server management.</td>
 </tr>

 <tr align="center">
     <td rowspan="3" >Networking and Delivery</td>
     <td>API Management</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/APIGateway.md">API Gateway</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/APIGateway.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/fb0cde6228b21d89ec222b45efec54e7-0856e92285f4e7ed254b2588d1fe1829.svg" /></a></td>
     <td>Amazon API Gateway is a powerful AWS tool that enables developers to securely and scalably create, publish, monitor, and manage APIs, facilitating integration between different services and applications.</td>
 </tr>

 <tr align="center">
     <td>DNS Management</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Route53.md">Route 53</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Route53.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/f5d2c00d40914bff4f82f29f9ef768bc-53a84099cf556710383a52b4612a8612.svg" /></a></td>
     <td>The Amazon Route 53 is AWS's domain name system (DNS) and content delivery network (CDN) service, providing domain registration, DNS resolution, and traffic routing to optimize availability and performance for applications on the internet.
</td>
 </tr>
 
 <tr align="center">
     <td rowspan="6">Integrate with any service model</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/LoadBalancer.md">Load Balancer</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/LoadBalancer.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/7177e919b32ad97825f95e902595014b-1594766d92813b5baeb706c453f91de0.svg" /></a></td>
     <td>Load balancing optimizes resource distribution, ensuring efficient and reliable performance by distributing incoming network traffic across multiple servers or resources.</td>
 </tr>
<tr align="center">
     <td>Storage</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/S3.md">S3</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/S3.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/c0828e0381730befd1f7a025057c74fb-43acc0496e64afba82dbc9ab774dc622.svg" /></a></td>
     <td>Amazon S3 is a highly scalable and durable object storage service from AWS, designed to store and retrieve massive amounts of data from anywhere on the web.</td>
 </tr>

<tr align="center">
     <td rowspan="2">Database</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/DynamoDB.md">DynamoDB</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/DynamoDB.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/6f419a45e63123b4c16bd679549610f6-87862c68693445999110bbd6a467ce88.svg" /></a></td>
     <td>DynamoDB is a fully managed, highly scalable, flexible, and high-performance NoSQL database service.</td>
 </tr>
 
<tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/RDS.md">RDS</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/RDS.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/1d374ed2a6bcf601d7bfd4fc3dfd3b5d-c9f69416d978016b3191175f35e59226.svg" /></a></td>
     <td>Amazon RDS is a managed cloud database service that makes it easy to set up, operate, and scale relational databases such as MySQL, PostgreSQL, Oracle, SQL Server, and others.</td>
 </tr>
 
 <tr align="center">
     <td rowspan="2">Management and Governance</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/CloudWatch.md">CloudWatch</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/CloudWatch.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/8f57ebd825a828e205b2dde223ba17e4-6af63a22dc297f8041286760ee8cd2c9.svg" /></a></td>
     <td>CloudWatch is an AWS monitoring and observability service that allows you to collect, store, visualize, and alert on real-time log and metric data for cloud resources.</td>
 </tr>
   
 <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AutoScaling.md">AutoScaling</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AutoScaling.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/8c4ff0bc6eb31f0dcf6f6765b4259429-8b46577d889db4c0abac90ec6961f188.svg" /></a></td>
     <td>AWS Auto Scaling is a service that automatically adjusts the capacity of computational resources to meet real-time demand, ensuring efficiency and high availability.</td>
 </tr>    
   
   
</table>
</details>
</details>

