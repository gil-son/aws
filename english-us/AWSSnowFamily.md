AWS Snow Family

<div align="center">
  <img src="https://thumbs2.imgbox.com/5c/94/COU1p1I7_t.png">
</div>
<br/>

The AWS Snow Family is a set of physical devices designed to securely and efficiently transfer data between on-premises environments and the AWS Cloud. These devices help organizations with large data volumes to overcome challenges related to data transfer, migration, and edge computing. It's helps when you need to run operations in austere, non-data center environments, and in locations where there's a lack of consistent network connectivity:

- Highly-secure, portable devices to collect and process data at the edge, and <b>migrate data into and out AWS</b>. Exist 2 use cases, Data migration and Edge computing.

- Data migration:
  - Snowcone
  - SnowBall Edge
  - Snowmobile   


- Edge computing:
  - Snowcone
  - Snowball Edge

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
you have limited connectivity, limited bandwidth, transferring data over the network may cost you some money. It's not free to use a network. It could be that also the bandwidth is shared. For example, if you download a video from AWS, and you download 10 terabytes of data, maybe you're going to block your entire office, because you're maximizing the bandwithin your office. And then maybe the connection is not stable enough. So, you have to retry, and so on.



AWS Snowcone
<div align="center">
  <img src="https://mms.businesswire.com/media/20200617005657/en/799138/4/4440824_AWS_Snowcone_E_Ink_Label.jpg" width="25%">
</div>
<br/>


AWS Snowball
<div align="center">
  <img src="https://www.ktexperts.com/wp-content/uploads/2019/11/Snowball-closed-600w.png" width="25%">
</div>
<br/>


AWS Snowmobile
<div align="center">
  <img src="https://d1.awsstatic.com/products/Snow/Snowmobile_11082016_09_SO1_534x300.2a5a5677ec9c098f2c4fa915a620e5fd2baed5a4.2a5a5677ec9c098f2c4fa915a620e5fd2baed5a4.png" width="50%">
</div>
<br/>
