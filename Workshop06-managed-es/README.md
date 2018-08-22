# cloudformation-workshops
Workshops about Cloud Formation on AWS

## Workshop06 : Build a managed ES domain

### Commandss
```
export AWS_PROFILE=<aws-profile>
aws cloudformation validate-template --template-body file://./es.yml

aws cloudformation create-stack --stack-name <env>-ws06 --template-body file://./es.yml --parameters file://./params.json
watch -n1 'aws cloudformation describe-stacks --stack-name <env>-ws06 | grep StackStatus'

# Update(s)
aws cloudformation update-stack --stack-name <env>-ws06 --template-body file://./es.yml --parameters file://./params.json

# Delete
aws cloudformation delete-stack --stack-name <env>-ws06
```
