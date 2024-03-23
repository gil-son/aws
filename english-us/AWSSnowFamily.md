AWS Snow Family

<div align="center">
  <img src="https://thumbs2.imgbox.com/5c/94/COU1p1I7_t.png">
</div>
<br/>

The AWS Snow Family is a set of physical devices designed to securely and efficiently transfer data between on-premises environments and the AWS Cloud. These devices help organizations with large data volumes to overcome challenges related to data transfer, migration, and edge computing. It's helps when you need to run operations in austere, non-data center environments, and in locations where there's a lack of consistent network connectivity:

- Highly-secure, portable devices to collect and process data at the edge, and <b>migrate data into and out AWS</b>. Exist 2 use cases, Data migration and Edge computing.

  - Edge computing:
    - Snowcone
    - Snowball Edge
    
  - Data migration:
    - Snowcone
    - SnowBall Edge
    - Snowmobile   
 
    <table>
      <tr>
        <th></th>
        <th>Snowcone & Snowcone SSD</th>
        <th>Snowball Edge Storage Optimized</th>
        <th>Snowmobile</th>
      </tr>  
      <tr>
        <td>Storage Capacity</td>
        <td>8 TB HDD 14TB SSD</td>
        <td>80 TB usable</td>
        <td><100 PB</td>
      </tr>
      <tr>
        <td>Migration Size</td>
        <td>Up to 24 TB, online and offline</td>
        <td>Up to PBs, offline</td>
        <td>Up to EB, offline</td>
      </tr>
      <tr>
        <td>DataSync agent</td>
        <td>Pre-installed</td>
        <td></td>
        <td></td>
      </tr>
  </table>

<hr/>

### Why Data Migrations with AWS Snow Family?

Well, if we look at the times it takes to transfer a lot of data over the network, it can take a lot of time. So for example, if we want to transfer 100 terabytes over a one gigabits per seconds network line, it will take us 12 days to achieve it, okay?

And so obviously if we do a petabyte, it will take forever and so on. 

<div align="center">
<table>
  <tr>
    <th rowspan=2></th>
    <th colspan=3>Time to Transfer</th>
  </tr>
  <tr>
    <th>100 Mbps</th>
    <th>1 Gbps</th>
    <th>10 Gbps</th>
  </tr>
  <tr>
    <th>
      10 TB
    </th>
    <td>
      12 days
    </td>
    <td>
      30 hours
    </td>
    <td>
      3 hours
    </td>
  </tr>
  <tr>
    <th>
      100 TB
    </th>
    <td>
      124 days
    </td>
    <td>
      12 days
    </td>
    <td>
      30 hours
    </td>
  </tr>
  <tr>
    <th>
      1 PB
    </th>
    <td>
      3 year
    </td>
    <td>
      124 days
    </td>
    <td>
      12 days
    </td>
  </tr>
</table>
</div>

So, as we can see, sometimes we just want the data to get to AWS fast, and the challenges is that sometimes on top of having a small network transfer, 
you have limited connectivity, limited bandwidth, transferring data over the network may cost you some money. It's not free to use a network. It could be that also the bandwidth is shared. For example, if you download a video from AWS, and you download 10 terabytes of data, maybe you're going to block your entire office, because you're maximizing the bandwithin your office. And then maybe the connection is not stable enough. So, you have to retry, and so on. So, all of these reasons make a case for Snow Family.

<b>AWS Snow Family: offiline devices to perform data migrations</b>If it takes more than a week to transfer over the network, use Snowball devices!

- Direct updaload to S3:
  - If wanted to directly updload a file into Amazon S3, we have the client sends the data into Amazon S3.
  <div align="center">
    <img src="https://thumbs2.imgbox.com/e7/e7/Ih9IrkFy_t.png" width="50%">
  </div>

- With Snow Family:
  - With Snow Family device, the clients request a Snow device. We receive it via post, okay? AWS will deliver the devices to us. We load the data directly onto the divices locally, and then we <b>ship</b> back the device to AWS, into an AWS facility. Then they will take the device and they will plug it into their own infraestructure. And then the data will be imported or exported based on what you want to do to an Amazon S3 bucket and you're good to go.
   <div align="center">
    <img src="https://thumbs2.imgbox.com/9d/dd/WHpoBWQI_t.png">
  </div>
 
    So really it is a way to transfer data to AWS, but through the physical route, not the network route

<hr/>

#### Edge Computing (for data transfer)

<details>
   <summary>Snow Ball Edge</summary>
   <div align="center">
    <img src="https://www.ktexperts.com/wp-content/uploads/2019/11/Snowball-closed-600w.png" width="25%">
  </div>
  Snowball Edge is a huge box as you can see and it is going to be used to:
    <ul>
      <li>Physical data transport solution, move TBs or PBs in or out of AWS.</li>
      <li>Alternative to moving data over the network (and paying network fees)</li>
      <li>Pay for data transfer job</li>
      <li>Provide block storage and Amazon S3-compatible object storage</li>
      <li><b>Snowball Edge Storage Optimed:</b> 80TB of HDD capacity for block volume and S3 compatible object storage</li>
      <li><b>Snowball Edge Compute Optimed:</b> 42TB of HDD or 28TB NVMe capacity for block volume and S3 compatible object storage</li>
      <li>Use cases: large data cloud migrations, DC decommission, disaster recovery</li>
    </ul>
  
</details>


<hr/>

#### Data Migrations

<details>
  <summary>AWS Snowcone</summary>
  <div align="center">
    <img src="https://mms.businesswire.com/media/20200617005657/en/799138/4/4440824_AWS_Snowcone_E_Ink_Label.jpg" width="25%">
  </div>
  
 
  AWS Snowcone and Snowcone SSD:
  <ul>
    <li>Small, portable computing, anywhere, rugged & secure, withstands harsh enviroments</li>
    <li>Device used for edge computing, storage, and data transfer</li>
    <li>Snowcone - 8 TB of HDD Storage</li>
    <li>Snowcone SSD - 14 TB of SSD Storage</li>
  </ul>

   You will use the Snowcone where the Snowball does not fit, for example, in a space-constrained enviroment, and you must provide your own batteries and cables. Now to send back the data to AWS, you have two options, So either you send the data back offiline by shipping it, or you can connect this device after it has captured some data into a data center, for example, whatever that has an internet connection, and then use the AWS DataSync service to send the data back to AWS.
</details>

<details>
  <summary>AWS Snowball</summary>  

  <div align="center">
    <img src="https://www.ktexperts.com/wp-content/uploads/2019/11/Snowball-closed-600w.png" width="25%">
  </div>

  AWS Snowball is a robust data transport solution for securely transferring large volumes of data to and from the AWS Cloud. With built-in security features and flexible deployment options, Snowball ensures reliable data transfer even in challenging environments. Ideal for organizations requiring efficient, high-speed data migrations and backups:

- Large-scale data transport solution for securely transferring large amounts of data to and from the AWS Cloud.
- Designed to handle petabytes of data.
- Physical device with built-in security features for data protection during transit.
- Available in multiple configurations with varying storage capacities.
- Suitable for use cases where transferring data over the internet is impractical or inefficient.
- Can be used in remote or edge locations with limited network connectivity.
- Provides options for offline data transfer by shipping the device or online data transfer via a secure network connection.
- Offers integration with AWS services like AWS DataSync for seamless data transfer to AWS storage services.
- Ideal for scenarios requiring high-speed, secure, and reliable data transfer, such as large-scale migrations, data backups, or disaster recovery operations.
</details>

<details>
  <summary>AWS Snowmobile</summary>
  
  <div align="center">
    <img src="https://d1.awsstatic.com/products/Snow/Snowmobile_11082016_09_SO1_534x300.2a5a5677ec9c098f2c4fa915a620e5fd2baed5a4.2a5a5677ec9c098f2c4fa915a620e5fd2baed5a4.png" width="50%">
  </div>
  
  The Snowmobile is an actual truck. So, when they announced it, they actually took a truck on stage to show, that it was an actual truck that is going to transfer data. And so, with Snowmobile, you can transfer exabytes of data:
  
  <ul>
    <li>Transfer exabytes of data (1EB = 1,000 PB = 1,000,000 TBs)</li>
    <li>Each Snowmobile will have 100 Petabytes of capacity (Then you need 10 Snowmobiles to reach 1 exabytes, use multiple in parallel)</li>
    <li>High security, temperature controlled, GPS, 24/7 video surveillance</li>
    <li>Better than Snowball if you transfer more than 10 PB</li>
  </ul>
</details>

<hr/>

### Usage Process

Ok, so how do we use a Snow Family device?

Well, you request the device from the console for delivery. Then you install the Snowball client, or use AWS Apps Hub that well see in this lecture on your servers. Then you connect the Snowball to the servers and start copying the files in the client. Then you ship back the device when we're ready. It will go straight to the right AWS facility thanks to an E-Ink marker. And the data will be loaded onto an S3 bucket. And then the Snowball will be completely wiped according to the highest security measures. Stages:

<ol>
  <li>Request Snowball devices from the AWS console for delivery</li>
  <li>Install the Snowball client / AWS OpsHub on your serves</li>
  <li>Connect the snowball to your servers and copy files using the client</li>
  <li>Ship back the device when you're done (goes to the right AWS facility)</li>
  <li>Data will be loaded into an S3 bucket</li>
  <li>Snowball is completely wiped</li>
</ol>

So, that's for the data migration. And that was originally one and only use case for Snowball devices. But the second use case now for the Snow Family is called edge computing.

### What is Edge Computing?

Edge computing is when you process data while it's being created at an location. But the second use case now for the Snow Family is called edge computing. By the way, an edge location is anything that really doesn't have internet or that is far away from a cloud. So, for example, if you have a truck on the road, or if you have a ship on the sea, or a mining station inderground, all these things can be called edge locations, because they can produce data, but the may not necessarily have internet connectivity. 

<div align="center">
  <img src="https://thumbs2.imgbox.com/ab/cc/hRJPCEUF_t.png" width="50%">
</div>

So, either limited connectivity or no internet access,or no access to computing power. And so, you may still want to run computation, data processing at these locations. And for this, we need edge computing.
And so, to do edge computing, we can order a Snowball Edge device or a Snowcone, and we have it embedded into these edge locations, and start doing edge computing. 

So, the use cases of edge computing are to pre-process data, perform Machine Learning at the edge without it needing to go back to the cloud, transcode major streams in advance, and eventually, if needed, transfer the data back into AWS. You can then ship back the device for your Snowcone or Snowball Edge. Essentially, you start processing the data very close to where it's being created, and then you ship it back to AWS.

### Snow Family - Edge Computing

<ul>
  <li>Snowcone & Snowcone SSD (smaller) 
    <ul>
      <li>2 CPUs, 4 GB of memory, wired or wireless access</li>
      <li>USB-C power using a cord or the optional battery</li>
    </ul>
  </li>
  <li> Snowball Edge - Compute
    <ul>
      <li>104 vCPU, 416 GiB of RAM</li>
      <li>Optinal GPU (useful for video processing or Machine Learning)</li>
      <li>28 TB NVMe or 42TB HDD usable storage</li>
      <li>Storage Clustering available (up to 16 nodes)</li>
    </ul>
  </li>
  <li> Snowball Edge - Storage Optimized
    <ul>
      <li>Up to 40 vCPUs, 80 GiB of RAM, 80 TB storage</li>
    </ul>
  </li>
  <li>All: Can run EC2 Instances & AWS Lambda functions (using AWS IoT Greengrass)</li>
  <li>Long-term deployment options: 1 and 3 years discounted princing</li>
</ul>

### AWS OpsHub

Finally, for the Snow Family, there is OpsHub:

<ul>
  <li>Historically, to use Snow Family devices, you needed a CLI (Command Line Interface tool)</li>
  <li>Today, you can use AWS OpsHub (a software you install on you computer) to manage your Snow Family Device
    <ul>
      <li>Unlocking and configuring single or clustered devices</li>
      <li>Transferring files</li>
      <li>Launching and managing instances running on Snow Family Devices</li>
      <li>Monitor device metrics (storage capacity, active instances on your device)</li>
      <li>Launch compatible AWS services on your devices (ex: Amazon EC2 instances, AWS DataSync, Netork File System (NFS))</li>
    </ul>
  </li>
</ul>
<br/>
<div align="center">
  <img src="https://media.amazonwebservices.com/blog/2020/oh_dash_1.png">
</div>





