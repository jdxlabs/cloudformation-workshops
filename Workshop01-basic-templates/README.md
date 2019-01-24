# cloudformation-workshops
Workshops about Cloud Formation on AWS

## Workshop01 : Basic templates : S3, EC2 Linux/Windows and DynamoDB

First you should install the aws-cli and be connect to an AWS account, like [described here](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html).

### Commands (for instance for the S3 bucket)
```
export AWS_PROFILE=<aws-profile>
aws cloudformation validate-template --template-body file://./basic-s3.yml
aws cloudformation create-stack --stack-name <env>-ws01 --template-body file://./basic-s3.yml
watch -n1 'aws cloudformation describe-stacks --stack-name <env>-ws01 | grep StackStatus'

# Update(s)
aws cloudformation update-stack --stack-name <env>-ws01 --template-body file://./basic-s3.yml

# Delete
aws cloudformation delete-stack --stack-name <env>-ws01
```
