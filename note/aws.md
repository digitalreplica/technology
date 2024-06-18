---
is_a: "[[note]]"
of: "[[technology]]"
---
# Notes
Amazon Web Services (AWS) notes.

# Howto
## CLI Setup
- [Environment Variables](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html)
```
export AWS_ACCESS_KEY_ID=AKIAEXAMPLEEXAMPLE
export AWS_SECRET_ACCESS_KEY=EXAMPLE/EXAMPLE/EXAMPLEKEY
export AWS_DEFAULT_REGION=us-west-2
```

### Default region and output
```
[default]
region = us-west-2
output = text
```

## CLI Foo
Copy file to s3
aws s3 cp test.txt s3://mybucket/test2.txt

Find instance by tag
aws ec2 describe-instances --filters "Name=tag:tag-name,Values=tag-value"

## AWS Cloudshell
### Setup Environment
python3 -m venv venv3
echo "source ~/venv3/bin/activate" >>.bash_profile
source .bash_profile
pip3 install boto3

### Per Shell Setup
sudo yum install nano

### Optional tools
Cloudformation CLI
```
pip3 install cloudformation-cli-python-plugin
```

# AWS Auditing tools
- https://github.com/StanGirard/YATAS - best practice checks
- 