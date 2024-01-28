 Load Balancer for AWS Lambda

  <div align="center">
    <img src="https://coralogix.com/wp-content/uploads/2019/02/Load-balancer-icon.png" width="50%">
  </div>
  
 A load balancer is a server or a critical component that plays a pivotal role in distributing incoming internet traffic to multiple servers (such as EC2 instances) downstream. This process optimizes resource utilization, enhances system performance, and ensures high availability by preventing any single server from being overwhelmed. Load balancers act as intermediaries, efficiently managing the distribution of requests, thereby improving the overall reliability and responsiveness of the system.

<div align="center">
    <img src="https://thumbs2.imgbox.com/44/00/9bCV1Xo4_t.png">
</div>

  
Load balancing is a versatile concept and can be applied to various types of resources beyond just EC2 instances. Load balancers are commonly used in different scenarios to distribute traffic across a range of resources to improve performance, reliability, and availability. Here are some examples of resources that can be combined with load balancing:

<ul>
    <li><strong>Web Servers:</strong> Load balancers can distribute incoming web traffic across multiple web servers to ensure efficient utilization of resources and improve the response time for users.</li>
    <li><strong>Application Servers:</strong> If your application is distributed across multiple servers, a load balancer can evenly distribute user requests among them to prevent any single server from becoming a bottleneck.</li>
    <li><strong>Database Servers:</strong> In some cases, load balancing can be applied to database servers to distribute database queries and transactions, helping to scale database operations and prevent overload on a single database server.</li>
    <li><strong>Microservices:</strong> In a microservices architecture, where an application is composed of small, independent services, load balancing can be used to distribute traffic across the various microservices.</li>
    <li><strong>Cloud Services:</strong> Beyond EC2 instances, load balancers can be used to distribute traffic across different types of cloud services, such as containers (e.g., Kubernetes clusters), serverless functions, or other virtual machines.</li>
    <li><strong>Hybrid Environments:</strong> Load balancing can be implemented in hybrid environments that span both on-premises data centers and cloud infrastructure, ensuring a balanced distribution of traffic across diverse resources.</li>
    <li><strong>Global Server Load Balancing (GSLB):</strong> Load balancing can also be employed on a global scale, distributing traffic across servers located in different geographic regions to optimize performance and provide fault tolerance.</li>
</ul>



  <details>
    <summary>
      <h3>Features</h3>
    </summary>
    <ul>
      <li><b>Distribution of Traffic:</b> Load balancing evenly distributes incoming requests among multiple instances, preventing overloading of any single function.</li>
      <li><b>Enhanced Scalability:</b> Load balancing facilitates horizontal scaling, allowing your serverless architecture to handle increased workloads seamlessly.</li>
      <li><b>High Availability:</b> By distributing functions across multiple availability zones, load balancing ensures continuous operation even in the face of failures.</li>
      <li><b>Cost Optimization:</b> Efficient load balancing can help optimize costs by ensuring resources are utilized effectively.</li>
      <li><b>Single Point:</b> Expose a single point of access (DNS) to your application</li>
      <li><b>Handle Failures:</b> Seamlessly handle failures of downstream instances</li>
      <li><b>Health Checks:</b>Do regular health checks to your instances</li>
      <li><b>Security:</b>Provide SSL termination (HTTPS) for your websites</li>
     <li><b>Across Zones:</b>High availability across zones</li>
    </ul>
  </details>

   <details><summary><h3>Components and Configuration</h3></summary>
      <details><summary><h4>Why use an Elastic Load Balancer?</h4></summary>
       <ul>
          <li>An ELB (Elastic Load Balancer) is a managed load balancer:
              <ul>
                <li>AWS guarantees that it will be working</li>
                <li>AWS takes care of upgrades, mainenance, high availability</li>
                <li>AWS provides only a few configurations knobs</li>
              </ul>
          </li>
          <li>It costs less to setup your own load balancer but it will be a lot more effort on your end (maintence, integrations)</li>
          <li>4 kinds of load balancers offered by AWS:
              <ul>
                <li>Application Load Balancer (HTTP / STTPS only) - Layer 7</li>
                <li>Network Load Balancer (ultra-high performance, allows for TCP) - Layer 4</li>
                <li>Gateway Load Balancer - Layer 3</li>
                <li>Classic Load Balancer (retired in 2023) - Layer 4 & 7</li>
              </ul>
          </li>
       </ul>
      </details>
      <details><summary><h4>Types of Load Balancers</h4></summary>
        <ul>
           <li>Application Load Balancer:
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/40/ab/a5iXGjyz_t.png" width="25%">
               </div>
               <ul>
                 <li>HTTP / HTTPS / gRPC protocols (Layer 7)</li>
                 <li>HTTP Routing features</li>
                 <li>AWS provides only a few con</li>
               </ul>
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/24/70/ait8gdLE_t.png">
               </div>
              <p>Choose an Application Load Balancer when you need a flexible feature set for your applications with HTTP and HTTPS traffic. Operating at the request level, Application Load Balancers provide advanced routing and visibility features targeted at application architectures, including microservices and containers.</p>
              <div align="center">
                 <img src="https://a.b.cdn.console.awsstatic.com/a/v1/5OBQRLTIGHMRUVN5XLKT5XU3JE4K6GTDZFDK5IPNT3GWUZTYJBOQ/2024-01-23T02-33-43_a88821a4018ec38/Static/591e55b0c20360da58ee3eee136b1fc6.svg" width="50%">
               </div>
              <hr/>
           </li>
           <li>Network Load Balancer:
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/12/75/GWDh0X03_t.png" width="25%">
               </div>
               <ul>
                 <li>TCP / UDP protocols (Layer 4)</li>
                 <li>High Performance, millions of request per seconds</li>
                 <li>Static IP through Elastic IP</li>
               </ul>
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/41/7e/6muve8z5_t.png">
               </div>
               <p>Choose a Network Load Balancer when you need ultra-high performance, TLS offloading at scale, centralized certificate deployment, support for UDP, and static IP addresses for your applications. Operating at the connection level, Network Load Balancers are capable of handling millions of requests per second securely while maintaining ultra-low latencies.
               </p>
               <div align="center">
                 <img src="https://a.b.cdn.console.awsstatic.com/a/v1/5OBQRLTIGHMRUVN5XLKT5XU3JE4K6GTDZFDK5IPNT3GWUZTYJBOQ/2024-01-23T02-33-43_a88821a4018ec38/Static/707c56b1d8a250c545ca7e2af0e770d7.svg" width="50%">
               </div>
               <hr/>
           </li>
            <li>Gateway Load Balancer:
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/b9/aa/ESBhKVPV_t.png" width="25%">
               </div>
               <ul>
                 <li>GENEVE Protocol on IP Packets (Layer 3)</li>
                 <li>Route Traffic to Firewalls that you manage on EC2 Instances</li>
                 <li>Intrusion detection</li>
               </ul>
               <div align="center">
                 <img src="https://thumbs2.imgbox.com/12/05/GFeWXg40_t.png">
               </div>
              <p>Choose a Gateway Load Balancer when you need to deploy and manage a fleet of third-party virtual appliances that support GENEVE. These appliances enable you to improve security, compliance, and policy controls.</p>
              <div align="center">
                 <img src="https://a.b.cdn.console.awsstatic.com/a/v1/5OBQRLTIGHMRUVN5XLKT5XU3JE4K6GTDZFDK5IPNT3GWUZTYJBOQ/2024-01-23T02-33-43_a88821a4018ec38/Static/2b583e8904605b0212959d386600bc20.svg" width="50%">
               </div>
           </li>
        </ul>
       </details>
  </details>

  <details>
    <summary>
      <h3>Terms and Concepts</h3>
    </summary>
    <ul>
      <li><b>Functions:</b> An AWS Lambda function is a unit of code that is executed in response to events.</li>
      <li><b>Events:</b> An event is an action that occurs in an AWS service, such as file upload in S3 or an API request from Amazon API Gateway, that can trigger the execution of a Lambda function.</li>
      <li><b>Runtime:</b> The runtime is the environment in which the code of the Lambda function is executed.</li>
      <li><b>Layers:</b> Layers allow you to include libraries, frameworks, and other dependency files in your Lambda function, while keeping the separation of your business logic code.</li>
      <li><b>Execution policy:</b> The execution policy controls the permissions that a Lambda function has to access other AWS resources.</li>
      <li><b>Alias:</b> An alias is a pointer to a specific version of a Lambda function.</li>
    </ul>
  </details>

  <details>
    <summary>
      <h3>Best Practices</h3>
    </summary>
    <ul>
      <li>Design Lambda functions to be small and perform specific tasks.</li>
      <li>Limit the execution time of functions to avoid unnecessary execution or failure due to time limits.</li>
      <li>Use environment variables to store sensitive information, such as API keys and passwords.</li>
      <li>Manage and monitor the logging of functions for troubleshooting and debugging.</li>
      <li>Use versioning and access control options to track and manage changes to Lambda functions.</li>
      <li>Configure access control policies to limit access to Lambda functions and the resources they use.</li>
      <li>Use monitoring resources, such as CloudWatch Metrics and CloudWatch Logs, to monitor and analyze the performance and efficiency of Lambda functions.</li>
      <li>Test and validate Lambda functions before deploying them to production.</li>
    </ul>
  </details>
