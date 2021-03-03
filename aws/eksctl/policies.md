
## Policies


### AccessToEKSCluster
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "eks:*"
            ],
            "Resource": "*"
        },
        {
            "Effect": "Allow",
            "Action": [
                "ssm:GetParameter"
            ],
            "Resource": "arn:aws:ssm:eu-central-1:802989172362:parameter/aws/service/eks/optimized-ami/1.18/amazon-linux-2/recommended/image_id"
        }
    ]
}
```

### AccessToCloudFormation
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "sqs:*",
                "cloudformation:CreateStack",
                "cloudformation:DescribeStacks",
                "cloudformation:DescribeStackEvents",
                "cloudformation:DescribeStackResources",
                "cloudformation:GetTemplate",
                "cloudformation:ValidateTemplate",
                "cloudformation:ListStacks",
                "cloudformation:DeleteStack"
            ],
            "Resource": "*"
        }
    ]
}
```

<hr/>

## Groups

### EKS

Attach this policies to group, attach group for user:
- AccessToEKSCluster
- AccessToCloudFormation
- AmazonEC2FullAccess
- IAMFullAccess
- AmazonEKSClusterPolicy
- AmazonSSMFullAccess
- AmazonEKSServicePolicy


<br/>
<a href="https://docs.aws.amazon.com/eks/latest/userguide/getting-started-eksctl.html">Next steps</a>