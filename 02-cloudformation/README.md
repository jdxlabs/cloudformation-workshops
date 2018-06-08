# Workshop02 : CloudFormation

```
aws cloudformation create-stack --stack-name WorkshopStack --template-body file://./main.yml
{
    "StackId": "arn:aws:cloudformation:eu-west-1:154040721022:stack/WorkshopStack/e9fc2680-6b1d-11e8-8ac3-503abe701c29"
}

aws cloudformation describe-stacks --stack-name=WorkshopStack
{
    "Stacks": [
        {
            "StackId": "arn:aws:cloudformation:eu-west-1:154040721022:stack/WorkshopStack/e9fc2680-6b1d-11e8-8ac3-503abe701c29",
            "Description": "Creates the landscape for our environment",
            "Tags": [],
            "EnableTerminationProtection": false,
            "CreationTime": "2018-06-08T13:14:45.872Z",
            "StackName": "WorkshopStack",
            "NotificationARNs": [],
            "StackStatus": "CREATE_COMPLETE",
            "DisableRollback": false,
            "RollbackConfiguration": {}
        }
    ]
}

aws cloudformation delete-stack --stack-name WorkshopStack
```
