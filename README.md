# awscloud

A Python Package to List AWS Cloud Resources for Different AWS Services!

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install awscloud.

```bash
pip install awscloud
```

## Usage

```python

import boto3, awscloud
from datetime import datetime, timedelta

## Below Start & End Date is used for Metrics Such as EC2's CPU Percentage etc.
start_date = datetime.now() - timedelta(days = 7)
end_date = datetime.now()

## Returns List of Attributes and Methods of this Package / Module.
print( dir( awscloud.AWSCloud ) )

## Refer Configuration from https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html
aws_object = awscloud.AWSCloud( session = boto3.Session( profile_name = PROFILE_NAME, region_name = REGION_NAME ) )

## List AWS EC2 Instances.
print( aws_object.List_EC2_Instances() )

## List AWS EC2 Volumes.
print( aws_object.List_EC2_Volumes() )

## List AWS EC2 Snapshots.
print( aws_object.List_EC2_Snapshots() )

## List AWS EC2 Security Groups.
print( aws_object.List_EC2_Security_Groups() )

## List AWS EC2 Load Balancers.
print( aws_object.List_EC2_Load_Balancers() )

## List AWS EC2 Network Interfaces.
print( aws_object.List_EC2_Network_Interfaces() )

## List AWS EC2 Key Pairs.
print( aws_object.List_EC2_Key_Pairs() )

## List AWS Elastic Beanstalk Applications.
print( aws_object.List_Elastic_Beanstalk_Apps() )

## List AWS S3 Buckets.
print( aws_object.List_S3_Buckets() )

## List AWS Lambda Functions.
print( aws_object.List_Lambda_Functions() )

## List AWS RDS Databases.
print( aws_object.List_AWS_RDS() )

## List AWS EC2 CPU Utilization Metrics.
print( aws_object.Get_EC2_CPU_Metrics( start_date = start_date, end_date = end_date ) )

## List AWS Trusted Advisor for Cost Optimizing.
print( aws_object.List_Cost_Trust_Advisor() )

```


## Contributing
Pull Requests are Welcome. For Major Changes, Please Open an issue First to Discuss What You Would like to Change.

Please Make Sure to Update Tests as Appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)