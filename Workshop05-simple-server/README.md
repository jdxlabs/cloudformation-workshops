# cloudformation-workshops
Workshops about Cloud Formation on AWS

## Workshop05 : Simple server

### Commandss
```
export AWS_PRsOFILE=<aws-profile>
aws cloudformation validate-template --template-body file://./vpc.yml
aws cloudformation create-stack --stack-name <env>-ws05 --template-body file://./vpc.yml --parameters file://./params.json
watch -n1 'aws cloudformation describe-stacks --stack-name <env>-ws05 | grep StackStatus'

# Update(s)
aws cloudformation update-stack --stack-name <env>-ws05 --template-body file://./vpc.yml --parameters file://./params.json

# Delete
aws cloudformation delete-stack --stack-name <env>-ws05
```
