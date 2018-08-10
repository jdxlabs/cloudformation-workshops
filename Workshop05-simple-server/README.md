# cloudformation-workshops
Workshops about Cloud Formation on AWS

## Workshop05 : Simple server

### Commandss
```
export AWS_PRsOFILE=sl-sandbox-<me>
aws cloudformation validate-template --template-body file://./vpc.yml
aws cloudformation create-stack --stack-name sbx-ws05-<me> --template-body file://./vpc.yml --parameters file://./params.json
watch -n1 'aws cloudformation describe-stacks --stack-name sbx-ws05-<me> | grep StackStatus'

# Update(s)
aws cloudformation update-stack --stack-name sbx-ws05-<me> --template-body file://./vpc.yml --parameters file://./params.json

# Delete
aws cloudformation delete-stack --stack-name sbx-ws05-<me>
```
