# AWS

<div align="center">
  <img src="https://i.ibb.co/6PMkBpW/AWS-Services-Shelf.png" width="40%">
</div>



<hr/>

### English reading

<details>
  <summary>Welcome</summary>
  <br/>
  <div align="center">
    <img src="https://cdn-icons-png.flaticon.com/512/3855/3855345.png" width="20%">
  </div>
      
  <p>This documentation serves as a platform to enhance and disseminate knowledge about AWS. I have crafted it to be intuitive, incorporating diagrams, partitions, examples, illustrations, and more.</p>
  
  - If you <b>feel confident about your understanding of AWS</b> and its resources, you can navigate to the <b>summary</b> and explore new features. 
  - However, if you are a beginner, I recommend allowing me to guide you by starting with the <b>AWS analogy</b>:

  #### AWS analogy
  
  AWS (Amazon Web Services) is a cloud platform from Amazon that offers various services for businesses and developers. To better understand, imagine that AWS is like a large tool store, where you can rent everything you need to build your house (or in this case, your application in the cloud).

There you can find simple shelves like S3 (for storage) to more complex tools like EC2 (for creating virtual servers). And if you need something even more specific, just take a look at the store catalog (Amazon Marketplace), which has a little bit of everything.

Oh, and there's more! In AWS, you only pay for what you use. That is, if you need a drill for just one hour, rent it for an hour and pay only for that period. And if you need the drill for longer, just renew the rental. So, you don't have to waste money on tools that you won't use.

Additionally, AWS has a security team that keeps an eye on everything all the time. So, you can rest assured knowing that your tools (or your application) are secure in Amazon's cloud.

In summary, AWS is like "a cloud tool store", where you rent only what you need and have security guaranteed by Amazon's team. Now just choose the right tools to build your house (or your application) and get to work!

  <div align="center">
      <img src="https://cdn-icons-png.flaticon.com/512/7714/7714580.png" width="12%">
      <img src="https://cdn-icons-png.flaticon.com/512/3032/3032220.png" width="5%">
      <img src="https://cdn-icons-png.flaticon.com/512/7845/7845642.png" width="12%">
      <img src="https://cdn-icons-png.flaticon.com/512/3032/3032220.png" width="5%">
      <img src="https://cdn-icons-png.flaticon.com/512/2590/2590584.png" width="12%">
      <img src="https://cdn-icons-png.flaticon.com/512/3032/3032230.png" width="5%">
      <img src="https://cdn-icons-png.flaticon.com/512/1864/1864777.png" width="12%">
    </div> 
           
</details>
<details>
  <summary>Summary</summary>
   <br/>
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
     <td>Elastic Beanstalk is an AWS-managed service that simplifies the deployment and scalability of web applications quickly and easily.</td>
 </tr>    

<tr align="center">
     <td>FaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lambda.md">Lambda</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lambda.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/945f3fc449518a73b9f5f32868db466c-926961f91b072604c42b7f39ce2eaf1c.svg" /></a></td>
     <td>AWS Lambda is a serverless service that allows for code execution in response to events, without the need for server management.</td>
 </tr>
 
 <tr align="center">
     <td rowspan="2">IaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/EC2.md">EC2</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/EC2.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /></a></td>
     <td>Amazon EC2 is a cloud computing service that allows easy configuration and running of virtual servers in the Amazon cloud, scaling compute capacity vertically or horizontally based on your application needs, and paying only for the resources you use.</td>
 </tr>

  <tr align="center">
     <td rowspan="5" >Networking and Delivery</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/VPC.md">VPC</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/VPC.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/74f8d03e857091589308684a506ba915-4d9c246d4283a8c3150cf0aa442dec10.svg" /></a></td>
     <td>A VPC (Virtual Private Cloud) is a virtual network environment in the cloud that provides isolated, private space for resources. It offers control over network configuration, including IP address ranges, subnets, and security settings, facilitating secure and scalable deployment of applications and services.</td>
 </tr>

 <tr align="center">
     <td>Content Delivery</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AmazonCloudFront.md">CloudFront</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AmazonCloudFront.md"><img src="https://thumbs2.imgbox.com/23/62/A66Gl0Cp_t.png" width="55%"/></a></td>
     <td>AWS CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs globally with low latency and high transfer speeds. It integrates seamlessly with other AWS services to enhance performance and security.</td>
 </tr>

 <tr align="center">
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
 
 <tr align="center">
     <td>Migrations & Transfer</td>
     <td>Data Transfer</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSSnowFamily.md">AWS SnowFamily</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSSnowFamily.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/316ccf80948adeaa0b9fc5863fa2e5d0-041cc4f719216c8b7fab8dd1d41f41e0.svg" /></a></td>
     <td>The tools in the AWSSnowFamily theme facilitate offline data movement and processing, ensuring seamless delivery for massive datasets.</td>
 </tr>  

 <tr align="center">
     <td rowspan="2">Storage</td>
     <td>STaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSStorageGateway.md">AWS StorageGateway</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSStorageGateway.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/6e57963f170fcf163d7a0362ab3aa560-475c7af9547c560c673fa2266ae7f440.svg" /></a></td>
     <td>Proficient in implementing and managing Storage Gateway solutions to seamlessly integrate on-premises environments with cloud storage, optimizing data transfer and access. Skilled in configuring and troubleshooting Storage Gateway configurations for efficient and reliable data storage solutions.</td>
 </tr>

<tr align="center">
     <td>Analycts</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSGlue.md"></a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSGlue.md"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTFVmyCvjYqwBE1Od0HzgD-Us60WPPpWHfAU8SVxm-HaQ&s" width="60%" /></a></td>
     <td>Fully managed ETL service. Simplifies data preparation, integration, and transformation. Enables seamless data loading for analytics in AWS ecosystem.</td>
 </tr>

<tr align="center">
     <td rowspan="8">Machine Learning</td>
     <td>Data Security</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Macie.md">Macie</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Macie.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/433463d9b34c9b0b655eb325d5f0ebce-bb33021b98aec6dc842de83ef649969e.svg" /></a></td>
     <td>Amazon Macie is a fully managed data security service that uses machine learning to automatically discover, classify, and protect sensitive data in AWS, ensuring compliance and enhancing data security.</td>
</tr>
<tr align="center">
     <td rowspan="7">Comunication</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Transcribe.md">Transcribe</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Transcribe.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/762bf9a0fc087fbb4ba021a3cee6edaf-2578b25de7cbb06633f39903ccc90d08.svg" /></a></td>
     <td>AWS Transcribe is an automatic speech recognition (ASR) service that converts spoken language into text, enabling transcription of audio and video files for various applications. It supports real-time and batch processing with features like speaker identification and custom vocabulary.</td>
</tr>
 <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Polly.md">Polly</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Polly.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/8ca4245f09e5a6ecf058c15cca9ac9b6-4a6ec5b037b363b8f33064d09d4f40ab.svg" /></a></td>
     <td>Amazon Polly is a text-to-speech service that uses advanced deep learning technologies to convert written text into natural-sounding speech, supporting multiple languages and voices for various use cases like application accessibility and media content.</td>
 </tr>
  <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Comprehend.md">Comprehend</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Comprehend.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/482863db6bbcbe5d42b2c38fc881497d-595c830f25109d745525de43d97fe7a9.svg" /></a></td>
     <td>Amazon Comprehend is a natural language processing (NLP) service that uses machine learning to extract insights from text, such as entity recognition, sentiment analysis, and topic classification. It helps analyze large volumes of textual data to improve decision-making and operational efficiency.</td>
 </tr>
  <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Kendra.md">Kendra</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Kendra.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/a9ab7ffabee2fd02cfeb90fa2c01a7fd-721a0b96fe52c46786b1ff711999c730.svg" /></a></td>
     <td>Amazon Kendra is an AWS service that offers intelligent search capabilities for enterprise data. It uses machine learning to deliver highly accurate and relevant search results across various data sources and formats.</td>
 </tr>
 <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Textract.md">Textract</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Textract.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/0121e707af85a4b5d571de33104d5ac1-b655f8b189e18898d77c2e95627a589b.svg" /></a></td>
     <td>AWS Textract is a machine learning service that automatically extracts text and data from documents, going beyond OCR by capturing structured data like tables and forms. It helps organizations streamline document processing, reduce manual data entry, and improve accuracy in extracting valuable information from complex documents.</td>
 </tr>
 </tr>
 <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Translate.md">Translate</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Translate.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/fc46e26a907870744758b76166150f62-76c22bfd03882310f44da5a6a9590864.svg" /></a></td>
     <td>A fully managed neural machine translation service that provides fast, high-quality, and affordable language translation for a wide variety of content types. Ideal for applications requiring real-time or batch translation, supporting multiple languages and enabling localization of content.</td>
 </tr>
<tr align="center">
    <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lex.md">Lex</a></td>
    <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lex.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/16660b27a03cc547adc54a269bc4a69e-7d762d8739de54214018a7d757540c79.svg" /></a></td>
    <td>AWS Lex is a service for building conversational interfaces using voice and text, powered by the same technology as Amazon Alexa, enabling developers to create chatbots and virtual assistants.</td>
</tr>
</table>


<div>
  <h2>NEW SUMMARY - COMING SOON</h2>
  
  - <img src="https://thumbs2.imgbox.com/95/7a/hpxsWpqt_t.png" alt="Compute" width="40" height="40"> Compute (3/11)
      <hr>
      <table/>
         <tr align="center">
             <td>Resource</td>
             <td>img</td>
             <td>Info</td>
        </tr>
        <tr align="center">
             <td><a href="https://github.com/gil-son/aws/blob/main/english-us/EC2.md">EC2</a></td>
             <td><a href="https://github.com/gil-son/aws/blob/main/english-us/EC2.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /></a></td>
             <td>Amazon EC2 is a cloud computing service that allows easy configuration and running of virtual servers in the Amazon cloud, scaling compute capacity vertically or horizontally based on your application needs, and paying only for the resources you use.</td>
        </tr>
        <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lambda.md">Lambda</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lambda.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/945f3fc449518a73b9f5f32868db466c-926961f91b072604c42b7f39ce2eaf1c.svg" /></a></td>
         <td>AWS Lambda is a serverless service that allows for code execution in response to events, without the need for server management.</td>
       </tr>
        <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/ElasticBeanstalk.md">ElasticBeanstalk</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/ElasticBeanstalk.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d43b67a293d39d11b046bd1813c804cb-4bc0ce71c93950e1ad695b25a4f1d4b5.svg" /></a></td>
         <td>Elastic Beanstalk is an AWS-managed service that simplifies the deployment and scalability of web applications quickly and easily.</td>
       </tr>
     </table>
  
  - <img src="https://thumbs2.imgbox.com/47/60/PNaM3eXz_t.png" alt="Storage" width="40" height="40"> Storage (3/7)
    <hr>
    <table>
       <tr align="center">
           <td>Resource</td>
           <td>img</td>
           <td>Info</td>
      </tr> 
      <tr align="center">
       <td><a href="https://github.com/gil-son/aws/blob/main/english-us/S3.md">S3</a></td>
       <td><a href="https://github.com/gil-son/aws/blob/main/english-us/S3.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/c0828e0381730befd1f7a025057c74fb-43acc0496e64afba82dbc9ab774dc622.svg" /></a></td>
       <td>Amazon S3 is a highly scalable and durable object storage service from AWS, designed to store and retrieve massive amounts of data from anywhere on the web.</td>
     </tr>
      <tr align="center">
       <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSSnowFamily.md">AWS SnowFamily</a></td>
       <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSSnowFamily.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/316ccf80948adeaa0b9fc5863fa2e5d0-041cc4f719216c8b7fab8dd1d41f41e0.svg" /></a>      </td>
       <td>The tools in the AWSSnowFamily theme facilitate offline data movement and processing, ensuring seamless delivery for massive datasets.</td>
     </tr>
     <tr align="center">
        <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSStorageGateway.md">AWS StorageGateway</a></td>
        <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSStorageGateway.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/6e57963f170fcf163d7a0362ab3aa560-475c7af9547c560c673fa2266ae7f440.svg" /></a></td>
         <td>Proficient in implementing and managing Storage Gateway solutions to seamlessly integrate on-premises environments with cloud storage, optimizing data transfer and access. Skilled in configuring and troubleshooting Storage Gateway configurations for efficient and reliable data storage solutions.</td>
     </tr>
      <table/>
  - <img src="https://thumbs2.imgbox.com/1b/15/XwlZ3v2v_t.png" alt="Networking & Content Delivery" width="40" height="40"> Networking & Content Delivery (4/10)
    <hr>
      <table>
         <tr align="center">
             <td>Resource</td>
             <td>img</td>
             <td>Info</td>
        <tr align="center">
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/VPC.md">VPC</a></td>
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/VPC.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/74f8d03e857091589308684a506ba915-4d9c246d4283a8c3150cf0aa442dec10.svg" /></a></td>
           <td>A VPC (Virtual Private Cloud) is a virtual network environment in the cloud that provides isolated, private space for resources. It offers control over network configuration, including IP address ranges, subnets, and security settings, facilitating secure and scalable deployment of applications and services.</td>
       </tr>
       <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AmazonCloudFront.md">CloudFront</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AmazonCloudFront.md"><img src="https://thumbs2.imgbox.com/23/62/A66Gl0Cp_t.png" width="55%"/></a></td>
         <td>AWS CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs globally with low latency and high transfer speeds. It integrates seamlessly with other AWS services to enhance performance and security.</td>
       </tr>
        <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Route53.md">Route 53</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Route53.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/f5d2c00d40914bff4f82f29f9ef768bc-53a84099cf556710383a52b4612a8612.svg" /></a></td>
         <td>The Amazon Route 53 is AWS's domain name system (DNS) and content delivery network (CDN) service, providing domain registration, DNS resolution, and traffic routing to optimize availability and performance for applications on the internet.
        </td>
       </tr>
      <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/LoadBalancer.md">Load Balancer</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/LoadBalancer.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/7177e919b32ad97825f95e902595014b-1594766d92813b5baeb706c453f91de0.svg" /></a>  </td>
         <td>Load balancing optimizes resource distribution, ensuring efficient and reliable performance by distributing incoming network traffic across multiple servers or resources.</td>
       </tr>
    <table/>
  - <img src="https://thumbs2.imgbox.com/01/20/rXpLIkB8_t.png" alt="Database" width="40" height="40"> Database (2/9)
     <hr>
      <table>
        <tr align="center">
            <td>Resource</td>
            <td>img</td>
            <td>Info</td>
        </tr>
        <tr align="center">
       <td><a href="https://github.com/gil-son/aws/blob/main/english-us/DynamoDB.md">DynamoDB</a></td>
       <td><a href="https://github.com/gil-son/aws/blob/main/english-us/DynamoDB.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/6f419a45e63123b4c16bd679549610f6-87862c68693445999110bbd6a467ce88.svg" /></a></td>
       <td>DynamoDB is a fully managed, highly scalable, flexible, and high-performance NoSQL database service.</td>
      </tr>
      <tr align="center">
       <td><a href="https://github.com/gil-son/aws/blob/main/english-us/RDS.md">RDS</a></td>
       <td><a href="https://github.com/gil-son/aws/blob/main/english-us/RDS.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/1d374ed2a6bcf601d7bfd4fc3dfd3b5d-c9f69416d978016b3191175f35e59226.svg" /></a></td>
       <td>Amazon RDS is a managed cloud database service that makes it easy to set up, operate, and scale relational databases such as MySQL, PostgreSQL, Oracle, SQL Server, and others.</td>
     </tr>
    </table>
  - <img src="https://thumbs2.imgbox.com/43/82/jLNe9Jbm_t.png" alt="Security, Identity, & Compliance" width="40" height="40"> Security, Identity, & Compliance (2/23)
     <hr>
      <table>
        <tr align="center">
            <td>Resource</td>
            <td>img</td>
            <td>Info</td>
        </tr>
        <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/IAM.md">IAM</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/IAM.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/0ebc580ae6450fce8762fad1bff32e7b-0841c1f0e7c5788b88d07a7dbcaceb6e.svg" /></a></td>
         <td>AWS IAM is an identity and access management service that enables control of access to AWS resources by users and applications.</td>
        </tr>
        <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Macie.md">Macie</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Macie.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/433463d9b34c9b0b655eb325d5f0ebce-bb33021b98aec6dc842de83ef649969e.svg" /></a></td>
         <td>Amazon Macie is a fully managed data security service that uses machine learning to automatically discover, classify, and protect sensitive data in AWS, ensuring compliance and enhancing data security.</td>
        </tr>
      </table>
  - <img src="https://thumbs2.imgbox.com/c9/28/i8xe96iT_t.png" alt="Analytics" width="40" height="40"> Analytics (1/19)
     <hr>
      <table>
        <tr align="center">
            <td>Resource</td>
            <td>img</td>
            <td>Info</td>
        </tr>
        <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSGlue.md">AWS Glue</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/AWSGlue.md"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTFVmyCvjYqwBE1Od0HzgD-Us60WPPpWHfAU8SVxm-HaQ&s" width="25%" /></a></td>
         <td>Fully managed ETL service. Simplifies data preparation, integration, and transformation. Enables seamless data loading for analytics in AWS ecosystem.</td>
       </tr>
    </table>
  - <img src="https://thumbs2.imgbox.com/16/5c/Irs3F10Z_t.png" alt="Machine Learning" width="40" height="40"> Machine Learning (7/29)
     <hr>
      <table>
        <tr align="center">
            <td>Resource</td>
            <td>img</td>
            <td>Info</td>
        </tr>
       <tr align="center">
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Transcribe.md">Transcribe</a></td>
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Transcribe.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/762bf9a0fc087fbb4ba021a3cee6edaf-2578b25de7cbb06633f39903ccc90d08.svg" /></a></td>
           <td>AWS Transcribe is an automatic speech recognition (ASR) service that converts spoken language into text, enabling transcription of audio and video files for various applications. It supports real-time and batch processing with features like speaker identification and custom vocabulary.</td>
        </tr>
        <tr align="center">
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Polly.md">Polly</a></td>
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Polly.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/8ca4245f09e5a6ecf058c15cca9ac9b6-4a6ec5b037b363b8f33064d09d4f40ab.svg" /></a></td>
           <td>Amazon Polly is a text-to-speech service that uses advanced deep learning technologies to convert written text into natural-sounding speech, supporting multiple languages and voices for various use cases like application accessibility and media content.</td>
       </tr>
       <tr align="center">
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Comprehend.md">Comprehend</a></td>
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Comprehend.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/482863db6bbcbe5d42b2c38fc881497d-595c830f25109d745525de43d97fe7a9.svg" /></a></td>
           <td>Amazon Comprehend is a natural language processing (NLP) service that uses machine learning to extract insights from text, such as entity recognition, sentiment analysis, and topic classification. It helps analyze large volumes of textual data to improve decision-making and operational efficiency.</td>
       </tr>
       <tr align="center">
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Kendra.md">Kendra</a></td>
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Kendra.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/a9ab7ffabee2fd02cfeb90fa2c01a7fd-721a0b96fe52c46786b1ff711999c730.svg" /></a></td>
           <td>Amazon Kendra is an AWS service that offers intelligent search capabilities for enterprise data. It uses machine learning to deliver highly accurate and relevant search results across various data sources and formats.</td>
       </tr> 
      <tr align="center">
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Textract.md">Textract</a></td>
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Textract.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/0121e707af85a4b5d571de33104d5ac1-b655f8b189e18898d77c2e95627a589b.svg" /></a></td>
           <td>AWS Textract is a machine learning service that automatically extracts text and data from documents, going beyond OCR by capturing structured data like tables and forms. It helps organizations streamline document processing, reduce manual data entry, and improve accuracy in extracting valuable information from complex documents.</td>
     </tr>
      <tr align="center">
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Translate.md">Translate</a></td>
           <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Translate.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/fc46e26a907870744758b76166150f62-76c22bfd03882310f44da5a6a9590864.svg" /></a></td>
           <td>A fully managed neural machine translation service that provides fast, high-quality, and affordable language translation for a wide variety of content types. Ideal for applications requiring real-time or batch translation, supporting multiple languages and enabling localization of content.</td>
       </tr>
       <tr align="center">
        <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lex.md">Lex</a></td>
        <td><a href="https://github.com/gil-son/aws/blob/main/english-us/Lex.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/16660b27a03cc547adc54a269bc4a69e-7d762d8739de54214018a7d757540c79.svg" /></a></td>
        <td>AWS Lex is a service for building conversational interfaces using voice and text, powered by the same technology as Amazon Alexa, enabling developers to create chatbots and virtual assistants.</td>
      </tr>
    </table>
  - <img src="https://thumbs2.imgbox.com/56/87/tWtOvjHB_t.png" alt="Management & Governance" width="40" height="40"> Management & Governance (1/27)
     <hr>
      <table>
        <tr align="center">
            <td>Resource</td>
            <td>img</td>
            <td>Info</td>
        </tr>
        <tr align="center">
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/CloudWatch.md">CloudWatch</a></td>
         <td><a href="https://github.com/gil-son/aws/blob/main/english-us/CloudWatch.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/8f57ebd825a828e205b2dde223ba17e4-6af63a22dc297f8041286760ee8cd2c9.svg" /></a></td>
         <td>CloudWatch is an AWS monitoring and observability service that allows you to collect, store, visualize, and alert on real-time log and metric data for cloud resources.</td>
       </tr>
    </table>
  - <img src="https://thumbs2.imgbox.com/47/b6/NVGD2zwy_t.png" alt="Developer Tools" width="40" height="40"> Developer Tools (0/14)
  - <img src="https://thumbs2.imgbox.com/d8/3c/eEzI8xpZ_t.png" alt="Application Integration" width="40" height="40"> Application Integration (1/9)
    <hr>
    <table>
       <tr align="center">
           <td>Resource</td>
           <td>img</td>
           <td>Info</td>
      </tr> 
    <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/APIGateway.md">API Gateway</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/english-us/APIGateway.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/fb0cde6228b21d89ec222b45efec54e7-0856e92285f4e7ed254b2588d1fe1829.svg" /></a></td>
     <td>Amazon API Gateway is a powerful AWS tool that enables developers to securely and scalably create, publish, monitor, and manage APIs, facilitating integration between different services and applications.</td>
     </tr>
    </table>
  - <img src="https://thumbs2.imgbox.com/27/97/8m67EJTG_t.png" alt="Front-end Web & Mobile" width="40" height="40"> Front-end Web & Mobile (0/4)
  - <img src="https://thumbs2.imgbox.com/1b/7a/pE5Ap4nv_t.png" alt="Containers" width="40" height="40"> Containers (0/4)
  - <img src="https://thumbs2.imgbox.com/af/16/N9EvPFcD_t.png" alt="Migration & Transfer" width="40" height="40"> Migration & Transfer (0/8)
  - <img src="https://thumbs2.imgbox.com/c8/d6/lIXRbROX_t.png" alt="Media Services" width="40" height="40"> Media Services (0/12)
  - <img src="https://thumbs2.imgbox.com/01/f6/mhwKvqjN_t.png" alt="Internet of Things" width="40" height="40"> Internet of Things (0/9)
  - <img src="https://thumbs2.imgbox.com/7e/24/aEOHuYEa_t.png" alt="End User Computing" width="40" height="40"> End User Computing (0/4)
  - <img src="https://thumbs2.imgbox.com/e9/3a/DnMVdCdL_t.png" alt="Business Applications" width="40" height="40"> Business Applications (0/12)
  - <img src="https://thumbs2.imgbox.com/ce/99/HIiBQBDO_t.png" alt="Game Development" width="40" height="40"> Game Development (0/1)
  - <img src="https://thumbs2.imgbox.com/4d/21/BYfIWXid_t.png" alt="Blockchain" width="40" height="40"> Blockchain (0/1)
  - <img src="https://thumbs2.imgbox.com/00/5d/0dmC6jMp_t.png" alt="Cloud Financial Management" width="40" height="40"> Cloud Financial Management (0/3)
  - <img src="https://thumbs2.imgbox.com/54/c6/XyPgFynS_t.png" alt="Customer Enablement" width="40" height="40"> Customer Enablement (0/5)
  - <img src="https://thumbs2.imgbox.com/fa/08/5hLOyOHh_t.png" alt="Satellite" width="40" height="40"> Satellite (0/1)
  - <img src="https://thumbs2.imgbox.com/03/c7/4wEaTpkr_t.png" alt="Quantum Technologies" width="40" height="40"> Quantum Technologies (0/1)

</div>
</details>

<hr/>

### Ler em Português

<details>
  <summary>Bem vindo(a)</summary>
  <br/>

  <div align="center">
    <img src="https://cdn-icons-png.flaticon.com/512/3855/3855345.png" width="20%">
  </div>
  
  <p>Esta documentação serve como uma plataforma para aprimorar e disseminar conhecimento sobre a AWS. Eu a elaborei de forma intuitiva, incorporando diagramas, partições, exemplos, ilustrações e muito mais.</p>

- Se você <b>se sente confiante sobre o seu entendimento da AWS</b> e seus recursos, pode acessar o <b>sumário</b> e explorar novas funcionalidades.
- No entanto, se você é um iniciante, recomendo que me permita guiá-lo começando com uma <b>Analogia à AWS</b>:

#### Analogia à AWS

A AWS (Amazon Web Services) é uma plataforma de nuvem da Amazon que oferece vários serviços para empresas e desenvolvedores. Para entender melhor, imagine que a AWS é como uma grande loja de ferramentas, onde você pode alugar tudo o que precisa para construir sua casa (ou, neste caso, sua aplicação na nuvem).

Lá você pode encontrar prateleiras simples como o S3 (para armazenamento) até ferramentas mais complexas como o EC2 (para criar servidores virtuais). E se você precisar de algo ainda mais específico, basta dar uma olhada no catálogo da loja (Amazon Marketplace), que tem um pouco de tudo.

Ah, e tem mais! Na AWS, você só paga pelo que usa. Ou seja, se você precisar de uma furadeira por apenas uma hora, alugue-a por uma hora e pague apenas por esse período. E se você precisar da furadeira por mais tempo, é só renovar o aluguel. Assim, você não precisa desperdiçar dinheiro com ferramentas que não vai usar.

Além disso, a AWS conta com uma equipe de segurança que fica de olho em tudo o tempo todo. Então, você pode ficar tranquilo sabendo que suas ferramentas (ou sua aplicação) estão seguras na nuvem da Amazon.

Resumindo, a AWS é como "uma loja de ferramentas na nuvem", onde você aluga apenas o que precisa e tem a segurança garantida pela equipe da Amazon. Agora é só escolher as ferramentas certas para construir sua casa (ou sua aplicação) e colocar as mãos à obra!

<div align="center">
    <img src="https://cdn-icons-png.flaticon.com/512/7714/7714580.png" width="12%">
    <img src="https://cdn-icons-png.flaticon.com/512/3032/3032220.png" width="5%">
    <img src="https://cdn-icons-png.flaticon.com/512/7845/7845642.png" width="12%">
    <img src="https://cdn-icons-png.flaticon.com/512/3032/3032220.png" width="5%">
    <img src="https://cdn-icons-png.flaticon.com/512/2590/2590584.png" width="12%">
    <img src="https://cdn-icons-png.flaticon.com/512/3032/3032230.png" width="5%">
    <img src="https://cdn-icons-png.flaticon.com/512/1864/1864777.png" width="12%">
</div>


</details>
<details>
  <summary>Sumário</summary>

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
     <td>FaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Lambda.md">Lambda</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Lambda.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/945f3fc449518a73b9f5f32868db466c-926961f91b072604c42b7f39ce2eaf1c.svg" /></a></td>
     <td>AWS Lambda é um serviço serverless que permite a execução de código em resposta a eventos, sem a necessidade de gerenciamento de servidores.</td>
 </tr>
  
 <tr align="center">
     <td rowspan="2">IaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/EC2.md">EC2</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/EC2.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /></a></td>
     <td>O Amazon EC2 é um serviço de computação em nuvem que permite configurar e executar facilmente servidores virtuais na nuvem da Amazon, escalando verticalmente ou horizontalmente a capacidade de computação de acordo com as necessidades da sua aplicação, pagando apenas pelos recursos que você usa.</td>
 </tr>

  <tr align="center">
     <td rowspan="5" >Rede e Entrega de Conteúdo</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/VPC.md">VPC</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/VPC.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/74f8d03e857091589308684a506ba915-4d9c246d4283a8c3150cf0aa442dec10.svg" /></a></td>
     <td>Um VPC (Virtual Private Cloud) é um ambiente de rede virtual na nuvem que fornece espaço isolado e privado para recursos. Ele oferece controle sobre a configuração da rede, incluindo intervalos de endereços IP, sub-redes e configurações de segurança, facilitando a implantação segura e escalável de aplicativos e serviços.</td>
 </tr>

 <tr align="center">
    <td>Entrega de Conteúdo</td>
    <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AmazonCloudFront.md">CloudFront</a></td>
    <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AmazonCloudFront.md"><img src="https://thumbs2.imgbox.com/23/62/A66Gl0Cp_t.png" width="55%"/></a></td>
    <td>O AWS CloudFront é um serviço de rede de entrega de conteúdo (CDN) rápido que entrega dados, vídeos, aplicações e APIs globalmente com baixa latência e altas velocidades de transferência. Ele se integra perfeitamente com outros serviços da AWS para melhorar o desempenho e a segurança.</td>
</tr>

<tr align="center">
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
  
  <tr align="center">
     <td>Migração e transferência</td>
     <td>Transferência de Dados</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AWSSnowFamily.md">AWS SnowFamily</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AWSSnowFamily.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/316ccf80948adeaa0b9fc5863fa2e5d0-041cc4f719216c8b7fab8dd1d41f41e0.svg" /></a></td>
     <td>As ferramentas temáticas da AWSSnowFamily facilitam o movimento e processamento de dados offline, garantindo entrega perfeita para gigantescos conjuntos de dados.</td>
 </tr>

 <tr align="center">
     <td rowspan="2">Armazenamento</td>
     <td>STaaS</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AWSStorageGateway.md">AWS StorageGateway</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AWSStorageGateway.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/6e57963f170fcf163d7a0362ab3aa560-475c7af9547c560c673fa2266ae7f440.svg" /></a></td>
     <td>Proficiente na implementação e gestão de soluções do Gateway de Armazenamento para integrar de forma transparente ambientes locais com armazenamento em nuvem, otimizando a transferência e o acesso de dados. Habilidoso em configurar e solucionar problemas nas configurações do Gateway de Armazenamento para soluções eficientes e confiáveis de armazenamento de dados.</td>

<tr align="center">
     <td>Análise de dados</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AWSGlue.md">AWS Glue</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/AWSGlue.md"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTFVmyCvjYqwBE1Od0HzgD-Us60WPPpWHfAU8SVxm-HaQ&s" width="60%" /></a></td>
     <td>Serviço totalmente gerenciado de ETL. Simplifica a preparação, integração e transformação de dados. Permite o carregamento contínuo de dados para análises no ecossistema da AWS.</td>
 </tr>

<tr align="center">
     <td rowspan="8">Aprendizado de Máquina</td>
     <td>Segurança dos dados</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Macie.md">Macie</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Macie.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/433463d9b34c9b0b655eb325d5f0ebce-bb33021b98aec6dc842de83ef649969e.svg" /></a></td>
     <td>Amazon Macie é um serviço de segurança de dados totalmente gerenciado que usa aprendizado de máquina para descobrir, classificar e proteger automaticamente dados sensíveis na AWS, garantindo conformidade e aprimorando a segurança dos dados.</td>
 </tr>
<tr align="center">
     <td rowspan="7">Comunicação</td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Transcribe.md">Transcribe</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Transcribe.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/762bf9a0fc087fbb4ba021a3cee6edaf-2578b25de7cbb06633f39903ccc90d08.svg" /></a></td>
     <td>AWS Transcribe é um serviço de reconhecimento automático de fala (ASR) que converte a linguagem falada em texto, permitindo a transcrição de arquivos de áudio e vídeo para diversas aplicações. Suporta processamento em tempo real e em lote, com recursos como identificação de locutores e vocabulário personalizado.</td>
 </tr>
 <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Polly.md">Polly</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Polly.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/8ca4245f09e5a6ecf058c15cca9ac9b6-4a6ec5b037b363b8f33064d09d4f40ab.svg" /></a></td>
     <td>Amazon Polly é um serviço de conversão de texto em fala que utiliza tecnologias avançadas de aprendizado profundo para transformar texto escrito em fala natural, suportando múltiplos idiomas e vozes para diversos casos de uso, como acessibilidade de aplicações e conteúdo de mídia.</td>
 </tr>
 <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Comprehend.md">Comprehend</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Comprehend.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/482863db6bbcbe5d42b2c38fc881497d-595c830f25109d745525de43d97fe7a9.svg" /></a></td>
     <td>Amazon Comprehend é um serviço de processamento de linguagem natural (NLP) que usa aprendizado de máquina para extrair insights de textos, como identificação de entidades, análise de sentimento e classificação de tópicos. Ele auxilia na análise de grandes volumes de dados textuais para melhorar a tomada de decisões e a eficiência operacional.</td>
 </tr>
 <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Kendra.md">Kendra</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Kendra.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/a9ab7ffabee2fd02cfeb90fa2c01a7fd-721a0b96fe52c46786b1ff711999c730.svg" /></a></td>
     <td>Amazon Kendra é um serviço da AWS que oferece capacidades de busca inteligente para dados empresariais. Ele utiliza aprendizado de máquina para fornecer resultados de busca altamente precisos e relevantes em várias fontes e formatos de dados.</td>
 </tr>
  <tr align="center">
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Textract.md">Textract</a></td>
     <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Textract.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/0121e707af85a4b5d571de33104d5ac1-b655f8b189e18898d77c2e95627a589b.svg" /></a></td>
     <td>AWS Textract é um serviço de aprendizado de máquina que extrai automaticamente texto e dados de documentos, indo além do OCR ao capturar dados estruturados como tabelas e formulários. Ele ajuda as organizações a otimizar o processamento de documentos, reduzir a entrada manual de dados e melhorar a precisão na extração de informações valiosas de documentos complexos.</td>
 </tr>
 <tr align="center">
    <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Translate.md">Translate</a></td>
    <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Translate.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/fc46e26a907870744758b76166150f62-76c22bfd03882310f44da5a6a9590864.svg" /></a></td>
    <td>Um serviço de tradução automática neural totalmente gerenciado que oferece tradução de idiomas rápida, de alta qualidade e acessível para uma ampla variedade de tipos de conteúdo. Ideal para aplicações que requerem tradução em tempo real ou em lote, suportando múltiplos idiomas e permitindo a localização de conteúdo.</td>
</tr>
<tr align="center">
    <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Lex.md">Lex</a></td>
    <td><a href="https://github.com/gil-son/aws/blob/main/portugues-br/Lex.md"><img src="https://d2q66yyjeovezo.cloudfront.net/icon/16660b27a03cc547adc54a269bc4a69e-7d762d8739de54214018a7d757540c79.svg" /></a></td>
    <td>AWS Lex é um serviço para criar interfaces de conversação usando voz e texto, alimentado pela mesma tecnologia do Amazon Alexa, permitindo que desenvolvedores criem chatbots e assistentes virtuais.</td>
</tr>
</table>

</details>

<div align="center">
  <img src="https://svgshare.com/i/13cG.svg" width="25%">
</div>

