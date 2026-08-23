AWS:

IAM role for ECR:

1) OIDC provider:

Identity provider - token.actions.githubusercontent.com
Audience - sts.amazonaws.com

2) Role - workflow-role-ECR

permission policy - AmazonEC2ContainerRegistryPowerUser
Turst policy - Github OIDC identity provider(caller identity), subject(github repo)(who can call) and audience(sts) what it is allowed to do.

string equals: aud
String like: with * for sub

3) Workflow setup for aws cred

Explicitly mention aud as sts.amazonaws.com in aws credential configure steps.

Add this role arn as secret in the github repo.