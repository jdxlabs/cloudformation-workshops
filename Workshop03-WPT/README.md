# cloudformation-workshops
Workshops about Cloud Formation on AWS

## Workshop03 : WebPageTest (webpagetest.org) deployed on AWS with EC2 and Load balancer

### Commandss
```
export AWS_PRsOFILE=<aws-profile>
aws cloudformation validate-template --template-body file://./wpt.yml
aws cloudformation create-stack --stack-name <stack-name> --template-body file://./wpt.yml --parameters file://./params.json
watch -n1 'aws cloudformation describe-stacks --stack-name <stack-name> | grep StackStatus'

# Update(s)
aws cloudformation update-stack --stack-name <stack-name> --template-body file://./wpt.yml --parameters file://./params.json

# Delete
aws cloudformation delete-stack --stack-name <stack-name>
```
