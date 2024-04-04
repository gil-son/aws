AWS Storage Gateway 

<div align="center">
  <img src="https://cdn2.iconfinder.com/data/icons/amazon-aws-stencils/100/Storage__Content_Delivery_AWS_Storage_Gateway-512.png" width="30%">
</div>
<br/>

AWS Storage Gateway acts as a vital bridge, connecting on-premise data infrastructure with cloud-based storage solutions, particularly Amazon S3. It seamlessly integrates on-premises environments with the AWS Cloud, providing a hybrid storage service.

<hr/>

### Use Cases

<b>Disaster Recovery:</b> Storage Gateway facilitates efficient disaster recovery solutions by enabling seamless data replication and backup to the cloud, ensuring business continuity in case of emergencies.

<b>Backup & Restore:</b> It offers a reliable mechanism for backing up critical data from on-premises systems to the cloud, simplifying data protection strategies and ensuring data integrity.

<b>Tiered Storage:</b> Storage Gateway enables organizations to implement tiered storage architectures, optimizing cost and performance by seamlessly moving data between on-premises storage and cloud-based storage tiers based on access patterns and requirements.

<hr/>

### Types of Storage Gateway

<b>File Gateway:</b> Allows on-premises applications to access data stored as objects in Amazon S3 using standard file protocols. This gateway offers a seamless and cost-effective way to store and retrieve data in the cloud while maintaining compatibility with existing applications.

<b>Volume Gateway:</b> Presents cloud storage as iSCSI block storage volumes, enabling on-premises applications to access durable and scalable cloud storage. It provides block-level access and supports various use cases such as backup, disaster recovery, and data migration.

<b>Tape Gateway:</b> Integrates on-premises backup applications with Amazon S3 and Glacier, allowing users to store data in the cloud using familiar tape-based workflows. Tape Gateway provides durable, cost-effective archival storage with offsite backup capabilities.


<hr/>

### Extra

#### AWS Storage Cloud Native Options

So if you wanted summarize the storage options on AWS, the block storage would be EBS or an EC2 instance store. 

The file store would be a network file system so Amazon EFS and object storage would be Amazon S3 or Glacier.

<br/>

<div align="center">
  <img src="https://thumbs2.imgbox.com/f7/45/7NyuhKAK_t.png">
</div>
