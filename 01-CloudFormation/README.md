# Workshop01 : CloudFormation

## To create the stack
```
export CF_WS_INITIALS=<my-initials>
aws cloudformation create-stack --stack-name WorkshopStack --template-body file://./main.yml \
    --parameters ParameterKey=Initials,ParameterValue=$CF_WS_INITIALS
{
    "StackId": "arn:aws:cloudformation:eu-west-1:154040721022:stack/WorkshopStack/e9fc2680-6b1d-11e8-8ac3-503abe701c29"
}

aws cloudformation describe-stacks --stack-name=WorkshopStack
{
    "Stacks": [
        {
            "StackId": "arn:aws:cloudformation:eu-west-1:154040721022:stack/WorkshopStack/e9fc2680-6b1d-11e8-8ac3-503abe701c29",
            "StackStatus": "CREATE_COMPLETE",
            ...
        }
    ]
}
```

## To update the stack
```
aws cloudformation update-stack --stack-name WorkshopStack --template-body file://./main.yml \
    --parameters ParameterKey=Initials,ParameterValue=$CF_WS_INITIALS
```

## To delete at the end
```
aws cloudformation delete-stack --stack-name WorkshopStack
```
