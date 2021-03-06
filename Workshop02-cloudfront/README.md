# cloudformation-workshops
Workshops about Cloud Formation on AWS

## Workshop02 : Basic example with CloudFront, S3 and Route53

### Commands
```
export AWS_PROFILE=<aws-profile>
aws cloudformation validate-template --template-body file://./basic-cf.yml
aws cloudformation create-stack --stack-name <env>-ws02 --template-body file://./basic-cf.yml --parameters file://./params.json
watch -n1 'aws cloudformation describe-stacks --stack-name <env>-ws02 | grep StackStatus'
aws s3 cp files/basic-cf-index.html s3://<repo-name>/index.html

# Update(s)
aws cloudformation update-stack --stack-name <env>-ws02 --template-body file://./basic-cf.yml --parameters file://./params.json

# Delete
aws cloudformation delete-stack --stack-name <env>-ws02
```
