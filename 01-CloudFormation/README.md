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

## To update the stack directly
```
aws cloudformation update-stack --stack-name WorkshopStack --template-body file://./main.yml \
    --parameters ParameterKey=Initials,ParameterValue=$CF_WS_INITIALS
```

## To previsualize the changes before execution ("dry-run" feature)
```
aws cloudformation create-change-set --stack-name WorkshopStack --template-body file://./main.yml \
    --parameters ParameterKey=Initials,ParameterValue=$CF_WS_INITIALS  --change-set-name changeset-1

aws cloudformation describe-change-set --stack-name WorkshopStack --change-set-name changeset-1 | jq '.Changes[]'
aws cloudformation execute-change-set --stack-name WorkshopStack --change-set-name changeset-1
```

## To watch the progression of the operation on the stack (creation, update, deletion)
```
watch -n1 "aws cloudformation describe-stacks --stack-name=WorkshopStack | jq '.Stacks[0].StackStatus'"
```

## To delete the stack at the end
```
aws cloudformation delete-stack --stack-name WorkshopStack
```
