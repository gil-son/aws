Auto Scaling
<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1200/1*Xd6ZqCDKUo5Cb79c2jdUxg.png" width="50%">
</div>

Amazon Auto Scaling is a versatile service that provides automatic capacity adjustments not only for Amazon EC2 instances but also for other AWS resources. By dynamically scaling resources based on predefined metrics such as CPU utilization or network traffic, Auto Scaling enables you to optimize performance and cost efficiency. Moreover, it seamlessly integrates with various AWS services, allowing dynamic scaling across a wide range of resources.

<details><summary><h3>Features</h3></summary>
<ul>
  <li><b>Dynamic scaling:</b> Auto Scaling automatically adjusts the number of EC2 instances, Docker services running on ECS, Kubernetes clusters on EKS, read/write capacity on DynamoDB, Aurora database instances, and other resources in response to changes in demand, ensuring your applications have the right amount of resources at all times.</li>
  <li><b>Scaling policies:</b> You can define scaling policies that determine when and how to scale EC2 instances, Docker services, read/write capacity on DynamoDB, and others based on metrics such as CPU utilization, network traffic, or custom metrics.</li>
  <li><b>Integration with AWS services:</b> Auto Scaling can be integrated with other AWS services like Amazon CloudWatch, Elastic Load Balancing, AWS Identity and Access Management (IAM) for more efficient and dynamic scaling across a variety of resources.</li>
  <li><b>Instance health monitoring:</b> Auto Scaling continuously monitors the health of EC2 instances, containers, databases, etc., and replaces unhealthy instances to maintain desired capacity and availability.</li>
  <li><b>Scheduled scaling:</b> You can set up scheduled scaling actions to automatically adjust the capacity of your instances, containers, databases, etc., based on predictable patterns, such as increasing during peak hours and decreasing during periods of lower demand.</li>
  <li><b>Integration with AWS Elastic Beanstalk:</b> Auto Scaling can be used with AWS Elastic Beanstalk to automatically scale your web applications based on traffic patterns.</li>
</ul>
</details>

<details><summary><h3>Terms and Concepts</h3></summary>
  <details><summary><h4>Scalability</h4></summary>
        <ul>
          <li>Scalability means that application / system can handle greater loads by adapting.</li>
          <li>There are two kinds of scalability:
            <ul>
              <li>Vertical Scalability
                <ul>
                  <li>Vertical Scalability means increase the size of the instance</li>
                  <li>Improve any part of the instance</li>
                  <li>Your application runs on a t2.micro, Scaling that application vertically means running it on a t2.large</li>
                  <div align="center">
                    <img src="https://thumbs2.imgbox.com/d4/1a/yPfIV4ZR_t.png">
                  </div>
                  <li>Vertical scalability is very common for non distributed systems, such as a database.</li>
                  <li>Theres usually a limit to how much you can vertically scale (hardware limit)</li>
                </ul>
              </li>
              <li>Horizontal Scalability (= elasticity)
                  <ul>
                  <li>Horizontal Scalability means increase the number of the instance / system for your application</li>
                  <li>Horizontal scaling implies distributed systems</li>
                  <li>This is very common for web applications / modern applications</li>
                  <div align="center">
                    <img src="https://thumbs2.imgbox.com/1e/13/1NerXmnE_t.png">
                  </div>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
  </details> 
  <details><summary><h4>Availability</h4></summary>
      <ul>
          <li>High Availability usually goes hand in hand with horizontal scaling</li>
          <li>High availability means running your application / system in at least 2 Availability Zones</li>
          <li>The goal of high availability is to survive a data center loss (disaster)</li>
            <div align="center">
                  <img src="https://thumbs2.imgbox.com/78/63/coxLKVbv_t.png">
            </div>
            <div align="center">
                  <img src="https://thumbs2.imgbox.com/c6/b3/Sjg8TioT_t.png">
            </div>
      </ul>
 </details> 
   <details><summary><h4>Scalability vs Elasticity (vs Agility)</h4></summary>
      <ul>
          <li><b>Scalability:</b> ability to accomodate a larger load by making the hardware stronger (scale up), or by adding nodes (scale out)</li>
          <li><b>Elasticity:</b>once a system is scalable, elasticity means that there will be some "auto-scaling" so that the system can scale based on the load. This is "cloud-friendly", pay-per-use, match demand, optimize costs</li>
          <li><b>Agility:</b>(not related to scalability - distractor) new IT resources are only a click away, wich means that you reduce the time to make those resources available to your developers from weeks to just minutes.</li>
      </ul>
      <hr/>
 </details> 
 <details><summary><h4>Auto Scaling Groups - Scaling Strategies</h4></summary>
      <ul>
          <li><b>Manual Scaling:</b> update the size of an ASG manually</b></li>
          <li><b>Dynamic Scaling:</b> respond to changing demand
              <ul>
                <li><b>Simple / Step Scaling</b>
                    <ul>
                      <li>When a Cloud Watch alarm is triggered (example CPU > 70%), then add 2 units</li>
                      <li>When a Cloud Watch alarm is triggered (example CPU < 30%), then remove</li>
                        <div align="center">
                          <img src="https://100daysofdevops.com/wp-content/uploads/2019/11/auto-scaling.png" width="50%">
                        </div>
                        (Adjusts the number of running instances based on application demand)
                    </ul>
                </li>
                 <li><b>Target Tracking Scaling</b>
                    <ul>
                      <li>Example: I want the avarege ASG CPU to stay around 40%</li>
                    </ul>
                </li>
                <li><b>Scheduled Scaling</b>
                    <ul>
                      <li>Antecipate a scaling based on known usage patterns</li>
                      <li>Example: increase the min capacity to 10 at 5pm on Wednesday</li>
                    </ul>
                    <div align="center">
                      <img src="https://docs.amazonaws.cn/en_us/autoscaling/ec2/userguide/images/capacity-example-with-as-diagram.png" width="50%">
                    </div>
                    (Auto Scaling helps ensure your application has the necessary capacity to handle both current and future demand)
                </li>
              </ul>
          </li>
          <li><b>Predictive Scaling</b>
              <ul>
                <li>Use Machine Learning to predict future traffic ahead of time</li>
                <li>Automatically provisions the right number of resources in advance</li>    
             </ul>
          </li>  
      </ul>
 </details>
</details>

<details><summary><h3>Best Practices</h3></summary>
<ul>
  <li><b>Define appropriate scaling policies:</b> Analyze your application's performance metrics and expected demand to define scaling policies that ensure optimal resource allocation, whether for EC2 instances, Docker services, database instances, etc.</li>
  <li><b>Use dynamic scaling:</b> Enable dynamic scaling based on real-time metrics to automatically adjust the number of instances, containers, read/write capacity on DynamoDB, etc., in response to changes in demand, ensuring optimal performance and cost efficiency.</li>
  <li><b>Monitor and optimize:</b> Regularly monitor and analyze your application's performance, and adjust scaling policies as needed to optimize resource allocation and maintain optimal performance across various AWS resources.</li>
  <li><b>Enable detailed monitoring:</b> Activate detailed monitoring for your Auto Scaling groups to collect more granular metrics and make more informed scaling decisions, regardless of the resource used.</li>
  <li><b>Use scheduled scaling:</b> Take advantage of scheduled scaling actions to automatically adjust the capacity of your instances, containers, databases, etc., based on predictable patterns, such as increasing during peak hours and decreasing during periods of lower demand.</li>
  <li><b>Integrate with other AWS services:</b> Leverage integration with other AWS services such as Amazon CloudWatch, Elastic Load Balancing, AWS Identity and Access Management (IAM) for more efficient and dynamic scaling across a variety of resources.</li>
  <li><b>Optimize the cooldown period:</b> Configure an appropriate cooldown period to prevent Auto Scaling from starting or terminating additional instances immediately after a scaling activity, allowing time for new instances to stabilize, whether for EC2 instances, Docker services, database instances, etc.</li>
</ul>
</details>
