# cloudformation-workshops
Workshops about Cloud Formation on AWS

## Workshop04 : Simple VPC

### Commandss
```
export AWS_PRsOFILE=<aws-profile>
aws cloudformation validate-template --template-body file://./vpc.yml
aws cloudformation create-stack --stack-name sbx-<me>-ws04 --template-body file://./vpc.yml --parameters file://./params.json
watch -n1 'aws cloudformation describe-stacks --stack-name sbx-<me>-ws04 | grep StackStatus'

# Update(s)
aws cloudformation update-stack --stack-name sbx-<me>-ws04 --template-body file://./vpc.yml --parameters file://./params.json

# Delete
aws cloudformation delete-stack --stack-name sbx-<me>-ws04
```
