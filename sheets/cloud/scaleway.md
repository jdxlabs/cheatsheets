# Scaleway CLI cheatsheet

## Install

First, install the client

```bash
mise use scw@latest

scw version
scw --help
```

## Login

```bash
# You can create a new API keypair using the command :
scw login

# You can also use environment variables to set the credentials :
export SCW_ACCESS_KEY=<access-key>
export SCW_SECRET_KEY=<secret-key>
export SCW_DEFAULT_REGION=<region>

# To handle your credentials, it's here : https://console.scaleway.com/iam/api-keys
# related doc : https://www.scaleway.com/en/docs/iam/how-to/create-api-keys/
scw init -p <project-alias> \
  access-key=<access-key>\
  secret-key=<secret-key>\
  organization-id=<organization-id>\
  project-id=<project-id>

# To manage ssh keys, if needed : https://console.scaleway.com/project/ssh-keys
# related commands
scw ssh-key list
scw iam ssh-key create name=my-rsa-key public-key="$(cat ~/.ssh/id_rsa.pub)"
scw iam ssh-key delete <name>

# To get information about your configuration :
scw config info
```

## Storages

Handle storages

```bash
scw object bucket list

# You can get infos about a bucket :
scw object bucket get <bucket-name>

# And make some operations on the bucket
scw object bucket --help
```

To operate directly on object, you need to use aws-cli :

```bash
aws configure --profile scw-user
export AWS_PROFILE=scw-user

aws --endpoint-url https://s3.fr-par.scw.cloud s3 ls
aws --endpoint-url https://s3.fr-par.scw.cloud s3 ls s3://test-user/

aws --endpoint-url https://s3.fr-par.scw.cloud s3 cp local-file s3://test-user/remote-file
aws --endpoint-url https://s3.fr-par.scw.cloud s3 cp s3://test-user/remote-file local-file
aws --endpoint-url https://s3.fr-par.scw.cloud s3 rm s3://test-user/remote-file
```

List compute instances
```bash
scw instance server list
```
