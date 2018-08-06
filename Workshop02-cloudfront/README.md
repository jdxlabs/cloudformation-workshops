# cloudformation-workshops

Workshops about Cloud Formation on AWS

## Workshop02 : CloudFront


### Basic example with CloudFront, S3 and Route53

#### Commands
```
export AWS_PROFILE=<aws-profile>
aws cloudformation create-stack --stack-name <stack-name> --template-body file://./basic-cf.yml --parameters file://./params.json
watch -n1 'aws cloudformation describe-stacks --stack-name <stack-name> | grep StackStatus'
aws cloudformation delete-stack --stack-name <stack-name>
```


### Usecase : WebPageTest (webpagetest.org) deployed with CloudFront

#### Commands
```
TODO
```
