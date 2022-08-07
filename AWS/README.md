When we have to delete or terminate the resources launched through CloudFormation template, it's a best practice to delete the cloudformation stack itself.

CloudFormation will delete and terminate the resources in a order. When we proceed to delete or terminate the resource, we might overlook and get billed at the end of the month.

In Resources.yaml file, every attribute of the EC2 instance are hard-coded. We have used `KeyName` attribute associated with the `Key Pair` available on one's AWS account.
One have to change value of `KeyName` attribute to the `Key Pair` available on one's AWS account. 
Otherwise, one might face with `ERROR: The Key Pair 'RSA-v1kt0r' was not found in AWS region us-east-1`
