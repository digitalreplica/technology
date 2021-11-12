# AWS

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
