<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:2570/1*YcNHxdrbPlV-lWjN_0Ek3g.png" width="50%">
</div>
<br/>

<h2>How to Organize Resources?</h2>
<p>
  <ul>
    <li>
      <b>Office:</b>
      <img src="https://i.ytimg.com/vi/_x9gZt2Lw9Y/maxresdefault.jpg" />
    </li>
    <li>
      <b>Cloud:</b>
      <img src="https://docs.aws.amazon.com/pt_br/AmazonRDS/latest/UserGuide/images/con-VPC-sec-grp.png" />
    </li>
  </ul>
</p>

<p>Amazon Virtual Private Cloud (Amazon VPC) is a network service that allows you to create an isolated virtual network in the Amazon cloud. With Amazon VPC, you can create a custom network with subnets, routing, route tables, internet gateways, and other features, providing full control over your cloud network infrastructure.</p>

<details><summary> <h3>Resources</h3></summary>
<ul>
  <li>
    <b>Private Subnet:</b>
    <p>Imagine there's an EC2 instance that accesses a database and returns some information to another EC2 instance. It doesn't make sense to expose it to the internet, so it's placed in a private subnet.</p>
  </li>
  <li>
    <b>Public Subnet:</b>
    <p>The public subnet instance is connected to the internet and can receive both incoming and outgoing data. It's typically a web server instance that can receive or make requests, often through a Gateway.</p>
    <img src="https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nti327hmr7a642l03njz.png" />
  </li>
  <li><b>Connectivity and Security:</b>
    <ul>
      <li>
        <p>VPC allows you to establish Virtual Private Network (VPN) connections to connect to a private subnet within your cloud infrastructure:</p>
        <img src="https://uploads-ssl.webflow.com/611b82111c177de53409c4b5/624465dfe2552c5f29e83625_iE6_z3bFB8uMSnfUz8R2uHqvlYh0E7_mAi7odxPszG5GeA4OXTwp6s8GYKf1N8AFS6OcYCDrHBpouNps1VohYqXTvlV_ZmLCG0xKogzjPjRTT8txNbOqv9oh64W-rqJJ2WqrQgG_.png" />
      </li>
      <li>
        <p>If you need additional security and faster resource interaction without going through the internet, you can use AWS Direct Connect, which provides dedicated, isolated connections:</p>
        <img src="https://www.w3schools.com/aws/images/directconnect.png" />
      </li>
    </ul>
  </li>
  <li><b>Access Control Lists:</b><p>At the subnet level, to ensure secure data traffic within a VPC, it's beneficial to use a configuration called Network ACLs (Access Control List). Network ACL is a subnet-level access control list that acts as a firewall within the VPC (Virtual Private Cloud):</p>
    <img src="https://docs.aws.amazon.com/images/vpc/latest/userguide/images/security-diagram_updated.png" />
    <p>
      Network ACLs are stateless, meaning they don't store state information. They have rules for both inbound and outbound data. For example, if a data packet enters a database and is allowed based on the configured rules, it doesn't necessarily mean that the outbound traffic will also be allowed; that too will be checked against the defined rules (and can be configured).
    </p>
  </li>
  <li><b>Security Groups:</b><p>At the EC2 instance level, using resources like security groups, the behavior becomes stateful, meaning that if traffic can enter, it can also leave. Entry is only blocked if it doesn't pass the rules. This is the default configuration but can be adjusted:</p>
    <img src="https://uploads-ssl.webflow.com/611b82111c177de53409c4b5/624465dfa8356e5ee15fe3ce_A0pF_xA7TfbCk8yMYt3AmKtVWL7f0_3yZvrYulgIxW_Gt4H6Q-vfqeqCnjrM03SktstA1IUZS-GmsM3xbumitDsTXSM-FI87Lb00dedOS_C1pTi7ZXd9q0kF4h8a4h4ytP94j4eN.png" />
  </li>
  <li><b>Customization:</b> You can customize your VPC by defining subnets, route tables, internet gateways, and other network resources according to your needs.</li>
  <li><b>Elasticity:</b> Amazon VPC is highly scalable, allowing you to add network resources as your infrastructure grows.</li>
</ul>
</details>
<details><summary> <h3>Terms and Concepts</h3></summary>
<ul>
  <li><b>Subnets:</b> Subnets in Amazon VPC are logical divisions of your virtual network where you can run resources and apply security settings.</li>
  <li><b>Route Tables:</b> VPC route tables determine how network traffic is routed between subnets, gateways, and other network resources.</li>
  <li><b>Internet Gateway:</b> An Internet Gateway allows resources in your subnets to access the internet in a controlled manner.</li>
  <li><b>Security Groups:</b> Security groups are sets of firewall rules that control inbound and outbound network traffic for resources in the VPC.</li>
  <li><b>Network ACLs:</b> Network Access Control Lists are subnet-level security rules that control network traffic between subnets.</li>
  <li><b>VPN (Virtual Private Network):</b> A VPN allows you to establish a secure connection between your local network and your cloud VPC, extending your network infrastructure.</li>
</ul>
</details>
<details><summary> <h3>Best Practices</h3></summary>
<ul>
  <li>Carefully plan the structure of your VPC, including defining subnets and route tables to meet your application's needs.</li>
  <li>Use security groups to control inbound and outbound network traffic for resources in your VPC.</li>
  <li>Implement Network Access Control Lists (Network ACLs) to add additional layers of subnet-level security.</li>
  <li>Use Internet Gateways only when necessary and apply access control policies to ensure security.</li>
  <li>Set up secure VPN connections to connect your local network to your VPC, extending your network infrastructure securely.</li>
  <li>Monitor network traffic and configure alerts to detect suspicious activities or performance issues.</li>
  <li>Maintain clear documentation of your VPC configuration and network resources to facilitate management and issue resolution.</li>
</ul>
</details>
