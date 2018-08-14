# TODO

* Attach to Route53 route
* Add SSL
* Add access policy

## Access policy example
```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "AWS": "*"
      },
      "Action": "es:*",
      "Resource": "arn:aws:es:<aws-region>:<account-id>:domain/<domain-name>/*",
      "Condition": {
        "IpAddress": {
          "aws:SourceIp": "<ops-team-cidr>"
        }
      }
    }
  ]
}
```
