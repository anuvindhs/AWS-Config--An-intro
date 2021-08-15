# AWS-Config-An-intro
AWS Config is a fully managed service that provides you with an AWS resource inventory, configuration history, and configuration change notifications to enable security and governance. With AWS Config you can discover existing AWS resources, export a complete inventory of your AWS resources with all configuration details, and determine how a resource was configured at any point in time. These capabilities enable compliance auditing, security analysis, resource change tracking, and troubleshooting.



## What is AWS Config?
AWS config takes care of tracking of all resources which are created, deleted, or managed with a great accuracy and less effort.
AWS config does detailed inventory of AWS resources configuration while continuously audit changes.This helps in evaluate configuration and compliance with preferred configurations using AWS Config Rules.
Also you can use Amazon SNS for notification when a change occurs 
 
In other words  

 A fully managed services for 
-  AWS resources inventory
-  To capture resources changes 
-  Store Configuration for individual resources
-  Snapshot of current resource configuration
-  SNS when a change occurs
- Cloud trail integration - Who made the change and When
- Compliance check - possible custom rules
- Security Analysis
- Information regarding relationship of resources
![config-AWS](https://d1.awsstatic.com/Products/product-name/diagrams/product-page-diagram-Config_how-it-works.bd28728a9066c55d7ee69c0a655109001462e25b.png)

------------
Lets talk a bit about **Configuration History** ! 

###Configuration items (CI)
 CI helps to understand changes of aws resources in  certain set of time.
####Components of a Configuration Item
![CI-AWS config](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4d81n9zw0s01m0r65vta.gif)

A json file that consist of-

*Metadata - Information about configuration item
it contains Version ID , the time when the configuration ID captured,Status of configuration, State ID*

*Attributes- information about resource ID, Key-Value tags for this resource,resource type, ARN- Amazon resource Name, AZ of resource, time stamp of resource creation*

*Relationships- Relationship between rsources associated with the account*

*Current Configaration - Information for call to discribe or list API resource 
example –* 
```bash
aws configservice get-resource-config-history –resource-type AWS::EC2::Subnet –resource-id subnet-xxxxxxxx
```

------------
###Resources 

[Demo of AWS Config](https://www.coursera.org/lecture/aws-fundamentals-addressing-security-risk/demo-of-aws-config-SnvLQ "Demo of AWS Config") - by [Rudy Chetty ](https://www.linkedin.com/in/rudashanchetty/ "Rudy Chetty ")

[Enforce Compliance with AWS Config](https://www.youtube.com/watch?v=X_fznJtSyV8&ab_channel=AmazonWebServices "Enforce Compliance with AWS Config") - by [AWS](https://www.youtube.com/channel/UCd6MoB9NC6uYN2grvUNT-Zg "AWS")

[Evaluate Third-Party Resources with AWS Config](https://www.youtube.com/watch?v=XwPVKsvrFXc&ab_channel=AmazonWebServices "Evaluate Third-Party Resources with AWS Config") -by [AWS](https://www.youtube.com/channel/UCd6MoB9NC6uYN2grvUNT-Zg "AWS") 

[AWS Config Videos Collection]( https://awsvideocatalog.com/management_&_governance/config "AWS Config videocatalog") by [awsvideocatalog.com](https://awsvideocatalog.com/ "awsvideocatalog.com")
 ------------
###Hands on Labs

 [AWS Config Workshop](https://mng.workshop.aws/config.html  "AWS Config Workshop") 

[AWS Config Workshop - Risk and Complaince ](https://risk-compliance.workshop.aws/en/3-detective-controls-config/1-config-setup.html  "AWS Config Workshop - Risk and Complaince ")

[Config Engine for IAC (infrastructure as code) Development Kit code ](https://github.com/awslabs/aws-config-engine-for-compliance-as-Rule  "Config Engine for IAC (infrastructure as code) Development Kit code ")

[AWS Config Rule Development Kit ](https://github.com/awslabs/aws-config-rdk  "AWS Config Rule Development Kit ")

[AWS Config Rules Repository](https://github.com/awslabs/aws-config-rules  "AWS Config Rules Repository")
