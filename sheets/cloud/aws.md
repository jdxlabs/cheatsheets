# AWS



## EKS cluster

EKS doc : https://docs.aws.amazon.com/eks/latest/userguide/getting-started.html

```bash
brew install eksctl

# Create an EKS cluster
eksctl create cluster --name eks1 --region eu-west-1 [--fargate]

# Get the kubeconfig file
aws eks --region eu-west-1 update-kubeconfig --name eks1

# delete the cluster
eksctl delete cluster --name eks1 --region eu-west-1
```

## Some configuration tips on AWS

### Get the total size of a S3 Bucket
```bash
aws s3 ls --summarize --human-readable --recursive s3://BUCKETNAME/PATH
or
aws s3 ls s3://BUCKETNAME/PATH --recursive | awk '{total+=$3} END{print "total =",total/1024/1024," MB"}'


# or :
aws cloudwatch get-metric-statistics --namespace AWS/S3 \
  --start-time 2018-02-05T00:00:00 --end-time 2018-02-06T00:00:00 \
  --period 86400 --statistics Average --region eu-west-1 --metric-name BucketSizeBytes \
  --dimensions Name=BucketName,Value=BUCKETNAME Name=StorageType,Value=StandardStorage \
  | jq -r '.Datapoints[0].Average' \
  | awk '{total+=$0} END{print "total =",int(total/1024/1024)," MB"}'
```

### Get Userdata script associated to the current EC2
```bash
curl http://169.254.169.254/latest/user-data
```

### Relaunch userdata script on the current EC2
```bash
bash <(curl http://169.254.169.254/latest/user-data)
```

### See logs of the userdata script the current EC2
```bash
tail -f /var/log/messages -n1000 | grep cloud-init
```

### Get the number of EC2 instances on a region
```bash
aws ec2 describe-instances --query 'Reservations[*].Instances[*].[InstanceId]' --region eu-west-3 --output text | wc -l
```

### Get the private and public ips of running EC2 instances
```bash
aws ec2 describe-instances \
  --output text \
  --query 'Reservations[*].Instances[*].[Tags[?Key==`Name`], PrivateIpAddress, PublicDnsName]' \
  --filters Name=tag:Name,Values='myprefix*' Name=instance-state-name,Values=running
```

### Get the current account id
```bash
aws sts get-caller-identity --output text --query 'Account'
```

### Get the available engines versions provisioned on RDS
```bash
aws rds describe-db-engine-versions --engine aurora-postgresql --query 'DBEngineVersions[?contains(SupportedEngineModes,`provisioned`)].EngineVersion'
```

### Get the available Debian AMIs
```bash
aws ec2 describe-images \
    --owners 379101102735 \
    --filters 'Name=name,Values=debian-stretch*' 'Name=state,Values=available'
```

### Get the security groups rules in/out
```bash
aws ec2 describe-security-groups \
  --output json \
  --query 'SecurityGroups[*].[GroupName, IpPermissions[*], IpPermissionsEgress[*]]' \
  --filters Name=tag:Name,Values='my-env*' > sgs_my-env.json
```