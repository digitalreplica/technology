---
is_a: "[[note]]"
urls: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html
in: "[[aws tech notes]]"
Aliases:
  - Instance Metadata Service
  - IMDSv1
  - IMDSv2
---
# Notes
- Security
	- https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/configuring-instance-metadata-service.html
- SSRF Protections
	- https://aws.amazon.com/blogs/security/defense-in-depth-open-firewalls-reverse-proxies-ssrf-vulnerabilities-ec2-instance-metadata-service/
- Questions
	- Can Lambda functions access?
		- I think Lambda can't access metadata service at all.
		- https://stackoverflow.com/questions/38465466/aws-lambda-meta-data-like-ec2-meta-data-for-lambda
			- lambda context gives you some information like region, account, function name
			- like `arn:aws:lambda:us-east-1:741063561123:function:lambda_context`