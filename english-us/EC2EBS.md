# Amazon Elastic Block Store (EBS)


<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0f/AWS_Simple_Icons_Storage_Amazon_EBS.svg/1200px-AWS_Simple_Icons_Storage_Amazon_EBS.svg.png" width="50%">
</div>

First of all, It is important you have knowlegde about <a href="https://github.com/gil-son/aws/blob/main/english-us/EC2.md">EC2</a>.

- An Amazon Elastic Block Store (EBS) volume is a network drive you can attach to your instance while it runs.
- It allows your instances to persist data even after their termination.
- EBS can only be mounted to one instance at a time (at the CCP level).
- EBS is bound to a specific availability zone.
- It's like a "USB stick" that takes information from one computer and passes it to another computer.
    


<details><summary><h3>Features</h3></summary>
<ul>
  <li><b>Scalability:</b> EBS volumes can be easily scaled up or down based on your storage requirements.</li>
  <li><b>Snapshots:</b> EBS allows you to create point-in-time snapshots of your volumes, providing a backup and recovery mechanism.</li>
  <li><b>High Performance:</b> EBS volumes offer high-performance storage with different volume types optimized for various use cases.</li>
  <li><b>Encryption:</b> EBS volumes can be encrypted for enhanced data security.</li>
  <li><b>Integration with EC2:</b> EBS volumes seamlessly integrate with Amazon EC2 instances, providing persistent block storage.</li>
</ul>
</details>

<details><summary><h3>Terms and Concepts</h3></summary>
<ul>
  <li><b>EBS Volumes:</b> EBS volumes are block-level storage devices that can be attached to EC2 instances.
      <li> It's a network drive (i.e not a physical drive)
        <ul>
          <li>It uses the network to communicate the instances, which means there might be a bit of latency</li>
          <li>It can be detached from an EC2 instance and attached to another one quickly</li>
        </ul>
     </li>
    <li> Its locked to an Avalability Zone (AZ)
        <ul>
          <li>An EBS Volume in us-east-Ia cannot bet attched to us-east-Ib</li>
          <li>To move a volume across, you first need to snapshot it</li>
        </ul>
    </li>
    <li>Have a privioned capacity (size in GBs, and IOPS)
      <ul>
          <li>You get billed for all the provisioned capacity</li>
          <li>You can increase the capacity of the drive over time</li>
      </ul>
   </li>
</li>
<li><b>EBS Volume - Example:</b> If exist a us-east-1 with one EC2 instance, it is possible to attach one EBS Volume to the EC2 instance

<div align="center">
  <img src="https://thumbs2.imgbox.com/82/bf/uWxwk84p_t.png">
</div>

If a new instance is alocated, the EBS Volume can not be attached to two instances

<div align="center">
  <img src="https://thumbs2.imgbox.com/5b/17/vMHtPcJ1_t.png">
</div>

then, this other EC2 instance needs to have its own EBS Volume attached to it as well as is very possible two EBS Volumes attached to one instance

<div align="center">
  <img src="https://thumbs2.imgbox.com/f2/62/do8a2PME_t.png">
</div>

Now EBS Volume are liked to an avalability zone, in this case us-east-1a. So if you want to have other EBS Volumes in an other AZ, then you would
need to create this separately in the other avaliability zone, in this case us-east-1b. So jut same way that's your EC2 instances are bound to an AZ,
so are the EBS Volumes

<div align="center">
  <img src="https://thumbs2.imgbox.com/92/5b/3rMQjWcM_t.png">
</div>

Finally, its possibile to create EBS Volumes and leave them unattached they don't need to be necessarily attached to an EC2 instance, they can be attached on demand
and that makes it very, very powerful

<div align="center">
  <img src="https://thumbs2.imgbox.com/59/32/RuvDvoKI_t.png">
</div>

 <li><b>Delete on Termination attribute:</b> Finally, when a EBS is create through EC2 instances
      <ul> Look
          <li>there is this thing called a Deletes on Termination attribute
            <div align="center">
              <img src="https://thumbs2.imgbox.com/4f/e1/jcdePj9F_t.png">
            </div>
          </li>
          <li>As well as exist a column in instance - storage to check about if you terminate the EC2, in consequence the EBS will be termitade too or not
            <div align="center">
              <img src="https://images2.imgbox.com/61/84/ch7cWPAA_o.png">
            </div>
          </li>
        </ul>
</li>
  
<li><b>Snapshot:</b> A snapshot is a point-in-time copy of an EBS volume, which can be used for backup and recovery.
    <ul>
          <li>Make a backup (snapshot) of your EBS volume at a point in time</li>
          <li>Not necessary to detach volume to do snapshot, but recommended</li>
          <li>Can copy snapshot across AZ or Region, is a way to transfer some of the data in different region on AWS</li>
          <hr/>
          So us-east-1a has an EC2 and an attached EBS volume
           <div align="center">
              <img src="https://thumbs2.imgbox.com/a8/20/eanO2Ogn_t.png">
           </div>
          That EBS volume would be snapshot it. For consequence the EBS Snapshots exist in your region
           <div align="center">
              <img src="https://thumbs2.imgbox.com/1b/7f/rfK9FFKN_t.png">
            </div>
          And that snapshot can be used to restore a new EBS volume in another availability zone
          <div align="center">
              <img src="https://thumbs2.imgbox.com/af/c8/UMTAkjwK_t.png">
          </div>
          And then now that is done. Is possible to attach the new EBS volume to an EC2 is us-east-1b and effectively transferred an EBS volume through a snapshot across AZ
          <div align="center">
              <img src="https://thumbs2.imgbox.com/c1/41/z4bXfnrm_t.png">
          </div>
      </ul>
<li><b>Snapshots Features:</b>
          <ul>
            <li><b>EBS Snapshot Archive</b>
              <ul>
                <li>Move a Snapshot to an "archive tier" that is 75% cheaper</li>
                <li>Takes within 24 or 72 hours for restoring the archive</li>
                <div align="center">
                  <img src="https://thumbs2.imgbox.com/09/2f/sCjyRxEh_t.png">
                </div>
              </ul>
            </li>
            <li><b>Recycle Bin for EBS Snapshots</b>
              <ul>
                <li>Setup rules to retain deleted snapshots so you can recover them after an accidental deletion</li>
                <li>Specify retention (from 1 day to 1 year)</li>
                <li></li>
                   <div align="center">
                    <img src="https://thumbs2.imgbox.com/02/10/OFCpvOaf_t.png">
                  </div> 
              </ul> 
            </li>
          </ul>
</li>
</li>
<li><b>Volume Types:</b> EBS provides different volume types, including General Purpose, Provisioned IOPS, and Magnetic, each optimized for specific use cases.</li>
</ul>
</details>

<details><summary><h3>Best Practices</h3></summary>
Some best practices for using Amazon EBS include:
<ul>
  <li>Choosing the appropriate volume type based on your application's I/O requirements.</li>
  <li>Regularly creating snapshots for backup and recovery purposes.</li>
  <li>Monitoring volume performance and adjusting as needed.</li>
  <li>Encrypting sensitive data by enabling EBS volume encryption.</li>
  <li>Considering RAID configurations for improved performance and fault tolerance.</li>
</ul>
</details>

It's crucial to understand the features, terms, and best practices associated with Amazon EBS to effectively utilize its capabilities for your applications.
