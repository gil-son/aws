EC2 Auto Scaling

<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1200/1*Xd6ZqCDKUo5Cb79c2jdUxg.png" width="50%">
</div>

Amazon EC2 Auto Scaling is a service that allows you to automatically adjust the number of Amazon EC2 instances running in response to changes in application demand. With Amazon EC2 Auto Scaling, you can ensure that your application has the necessary capacity to handle both current and future demand. It can automatically adjust the number of EC2 instances to handle traffic spikes and reduce the number of instances when demand decreases.
<details><summary><h3>Resources</h3></summary>
<ul>
  <li><b>Elasticity:</b> EC2 Auto Scaling automatically adjusts the number of running instances based on application demand.</li>
<div align="center">
<img src="https://100daysofdevops.com/wp-content/uploads/2019/11/auto-scaling.png" width="50%">
</div>
  <li><b>Scalability:</b> EC2 Auto Scaling helps ensure your application has the necessary capacity to handle both current and future demand.</li>
<div align="center">
<img src="https://docs.amazonaws.cn/en_us/autoscaling/ec2/userguide/images/capacity-example-with-as-diagram.png" width="50%">
</div>
  <li><b>Load balancing:</b> EC2 Auto Scaling works in conjunction with Elastic Load Balancing (ELB) to distribute traffic across EC2 instances.</li>
<div align="center">
<img src="https://media.amazonwebservices.com/blog/2014/elb_auto_scale_instances_2.png" width="50%">
</div>
  <li><b>High availability:</b> EC2 Auto Scaling helps ensure your application is always available, even during traffic spikes.</li>
  <li><b>Integration with other AWS services:</b> EC2 Auto Scaling can easily be integrated with other AWS services, such as Amazon CloudWatch and Amazon SNS.</li>
</ul>
</details>
<details><summary><h3>Terms and Concepts</h3></summary>
<ul>
  <li><b>Auto Scaling groups:</b> An Auto Scaling group is a set of EC2 instances created from a single configuration. The Auto Scaling group is automatically scaled to meet application demand.</li>
  <li><b>Scaling policy:</b> The scaling policy is a set of rules that EC2 Auto Scaling follows to adjust the number of running instances.</li>
  <li><b>Scaling metrics:</b> The scaling metrics are the metrics used by EC2 Auto Scaling to determine when to adjust the number of running instances. Some common metrics include CPU utilization, memory utilization, and number of network connections.</li>
  <li><b>Automatic launch:</b> Automatic launch is the process of automatically creating new EC2 instances in response to application demand.</li>
  <li><b>Automatic termination:</b> Automatic termination is the process of automatically shutting down EC2 instances when they are no longer needed.</li>
</ul>
</details>
<details><summary><h3>Best Practices</h3></summary>

Some best practices for using Amazon EC2 Auto Scaling include:
<ul>
  <li>Defining appropriate scaling policies and alarms to ensure that EC2 instances are added or removed automatically based on application demand.</li>
  <li>Configuring load balancing to distribute traffic across running EC2 instances, ensuring high availability and horizontal scalability.</li>
  <li>Monitoring EC2 instance usage and setting alerts for anomalies or security issues.</li>
  <li>Using configuration options to ensure that EC2 instances have the necessary capacity and resources to handle application demand.</li>
  <li>Automating the deployment of applications on EC2 instances to reduce downtime and ensure consistency across different instances.</li>
</ul>

It is important to remember that Amazon EC2 Auto Scaling is a powerful tool for ensuring application scalability and availability, but its configuration should be careful and well-planned. Additionally, it is important to constantly monitor application performance and adjust scaling policies according to changes in demand and usage.
