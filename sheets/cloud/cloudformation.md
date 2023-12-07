# CloudFormation commands

## To configure your AWS account
```bash
aws configure --profile <my-profile>
export AWS_PROFILE=<my-profile>
```

## To validate a template
```bash
aws cloudformation validate-template --template-body file://./template.yml
```

## To create a stack
```bash
aws cloudformation create-stack \
  --stack-name <my-stack> \
  --template-body file://./template.yml \
  --parameters ParameterKey=Initials,ParameterValue=<my-initials>
```

## To describe the stack
```bash
aws cloudformation describe-stacks --stack-name <my-stack>
```

## To update the stack directly
```bash
aws cloudformation update-stack \
  --stack-name <my-stack> \
  --template-body file://./template.yml \
    --parameters ParameterKey=Initials,ParameterValue=<my-initials>
```

## To previsualize the changes before execution ("dry-run" feature)
```bash
aws cloudformation create-change-set \
  --stack-name <my-stack> \
  --template-body file://./template.yml \
  --parameters ParameterKey=Initials,ParameterValue=<my-initials> \
  --change-set-name changeset-1

aws cloudformation describe-change-set \
  --stack-name <my-stack> \
  --change-set-name changeset-1 | jq '.Changes[]'

aws cloudformation execute-change-set \
  --stack-name <my-stack> \
  --change-set-name changeset-1
```

## To watch the progression of the operation on the stack (creation, update, deletion)
```bash
watch -n1 "aws cloudformation describe-stacks --stack-name <my-stack> | jq '.Stacks[0].StackStatus'"
```

## To delete the stack at the end
```bash
aws cloudformation delete-stack --stack-name <my-stack>
```

