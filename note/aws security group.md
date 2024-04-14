---
aliases:
  - aws security groups
  - SGs
id: 
is:
  - "[[note]]"
of:
  - "[[personal/technology/note/aws|aws]]"
---
# Notes
Restricting outbound access
- Per [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/security-group-rules.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/security-group-rules.html)
> By default, security groups contain outbound rules that allow all outbound traffic. You can delete these rules.
- A security group with no outbound rules will
	- Allow DNS to the Route 53 Resolver (hidden AWS rule)
	- Block all other outbound access
