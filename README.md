# cloudformation-workshops
Workshops about Cloud Formation on AWS

## Workshop #1
Make some CloudFormation templates in Yaml :
* A S3 bucket
* An EC2 instance
* A DynamoDB table

You have to create, securely modify (with changeset), then delete them.  
You also have to create Outputs to store the values on AWS.

## Workshop #2
Build a static website with Amazon S3, Route 53 and CloudFront.  
You have a process [explained here](https://aws.amazon.com/getting-started/projects/host-static-website/?trk=gs_card).  
You can create it manually, then build it with CloudFormation.  
Just print "Hello world !", the point is to be confortable with CloudFront.

## Workshop #3
Build an EC2 instance that hosts the Webpagetest program, with EC2 and ELBS (CloudFront isn't relevant for this usecase).  
You can access to the program [here](https://webpagetest.org).
