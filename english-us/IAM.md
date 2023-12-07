IAM
<div align="center">
  <img src="https://branditechture.agency/brand-logos/wp-content/uploads/wpdm-cache/AWS-IAM-900x0.png" width="50%">
</div>

AWS <b>Identity and Access Management (IAM)</b> is one of the main resources because it allows for secure management of access to AWS services and other resources by creating user groups, users, and permissions.
<div align="center">
  <img src="https://user-images.githubusercontent.com/72712095/227651287-bb0f47cf-106b-4b27-be56-f954afef6bbb.png">
</div>
<details><summary> <h3>Resources</h3></summary>
<ul>
    <li><b>Shared access to AWS accounts:</b> Provides access permissions to other users</li>
    <li><b>Granular permissions:</b> Users can have different levels of access according to their roles in an AWS account</li>
    <li><b>MFA:</b> Multi-factor authentication</li>
    <li><b>Integration with AWS services:</b> Establishes levels of access permissions to AWS services</li>
    <li><b>Free:</b> IAM has no costs or usage limits</li>
</ul> 
</details>
<details><summary> <h3>Terms and concepts</h3></summary>
<ul>
<li><b>Identity:</b> Provides access to an AWS account</li>
<li><b>IAM Users:</b> Represents a person or service that uses AWS services</li>
<li><b>IAM Groups:</b> Collection of IAM users</li>
<li><b>IAM Roles:</b> Set of permissions that determine the level of access of an identity to AWS services
<div align="center">
<img src="https://cloudiofy.com/wp-content/uploads/2022/08/iam-entities.png" width="70%">
</div>  
</li>
<li><b>IAM Policies:</b> Define access permissions to AWS services (an object), when associated with a group and/or user, define their permissions. IAM Roles (role/function) have policies within them. Ways to use the policy:
<ul>
<li><b>Inline policy:</b> Permissions attached directly to an identity (not reusable)
<div align="center">
<img src="https://docs.aws.amazon.com/pt_br/IAM/latest/UserGuide/images/policies-inline-policies.diagram.png" width="70%">
</div>
</li>
<li><b>Managed policy:</b> Set of permissions available to multiple identities</li>
<div align="center">
<img src="https://docs.aws.amazon.com/pt_br/IAM/latest/UserGuide/images/policies-aws-managed-policies.diagram.png" width="70%">
</div>
</ul>   
</li>
<li><b>IAM Permissions:</b> Lowest level of the hierarchy, determines whether an identity can or cannot take an action on an AWS resource (Allow/Deny)</li>
<li><b>IAM Security Tools:</b>
<ul>
  <li>IAM Credentials Report (account-level)
      <ul>
        <li>a report that list all your account's users and the status of their various credential</li>
      </ul>
  </li> 
  <li>IAM Access Advisor (user-level)
      <ul>
        <li>Access advisor shows the service permissions granted to a user and when those services were last accessed.</li>
        <li>You can use this information to revise your policies.</li>
      </ul>
  </li> 
</ul>

</li>
 
</ul>
</details>
<details><summary> <h3>Best Practices</h3></summary>
 <p>
    AWS has a list of best practices to help developers and IT professionals manage access to AWS resources.  
 </p>
<ul>
    <li><b>Root account:</b> Do not use it for daily development tasks. It is more geared towards managing:
    <ul>
      <li>Account Dashboard</li>
      <li>Defining who the administrators are</li>
      <li>AWS plans and/or services</li>
    </ul>
    </li>
    <li><b>Users:</b> Create individual users and, if necessary, define a group for these users</li>
    <li><b>Least privilege:</b> Provide only the level of access needed</li>
    <li><b>Permissions:</b> Use user groups with permissions</li>
    <li><b>Auditing:</b> Activate AWS CloudTrail</li>
    <li><b>Passwords:</b> Always use strong passwords</li>
    <li><b>MFA:</b> Activate it for privileged users</li>
</ul> 
</details>

