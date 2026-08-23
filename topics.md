so in github i have know below topics





worflow

job

steps

output btw jobs

variable shared btw one step and another. 

each job run in differnt runnner

each step run in new shell process

workflow trigger event, workflow call, dispatch, push, pull, and other

inputs, output, secrets to reusable workflow

built in actions

custom composite action.

reusable job



🔴 High priority
Contexts
github.*
env.*
vars.*
secrets.*
inputs.*
steps.*
jobs.*
needs.*
runner.*
Environment variables
Workflow-level env
Job-level env
Step-level env
GITHUB_ENV
Artifacts
upload-artifact
download-artifact
Sharing files between jobs
Conditions
if:
success()
failure()
always()
cancelled()
Job dependencies
needs
Multiple dependencies
Conditional dependencies
Matrix strategy
strategy.matrix
Multiple OS/version combinations
include
exclude
Caching
actions/cache
Dependency caching
Docker Buildx cache
GitHub Environments
dev
staging
production
Environment secrets
Required reviewers
Deployment protection
🟠 Security
GITHUB_TOKEN
What it is
Permissions
permissions:
contents: read/write
packages: write
Secrets
Repository secrets
Environment secrets
Organization secrets
Secret masking
Secrets in reusable workflows
OIDC security
Trust policies
aud
sub
Least privilege
AWS role permissions
PR security
pull_request
Forked repositories
pull_request_target
Why secrets shouldn't blindly be exposed to PR code
🟡 Advanced / useful
Concurrency
concurrency:
Cancel previous runs
Prevent simultaneous deployments
Job/step failure handling
continue-on-error
if: failure()
if: always()
Artifacts vs cache
When to use each
Artifact retention
Self-hosted runners
Runner setup
Labels
Runner groups
Security considerations
GitHub-hosted runner details
ubuntu-latest
windows-latest
macos-latest
Preinstalled tools
Expressions
${{ }}
&&
||
!
contains()
startsWith()
format()
fromJSON()
Workflow commands
$GITHUB_OUTPUT
$GITHUB_ENV
$GITHUB_PATH
$GITHUB_STEP_SUMMARY
Job outputs vs workflow outputs
Step → Job → Reusable workflow → Calling workflow
🟢 For your DevOps pipeline
Docker image scanning
Trivy
SBOM
Syft
CycloneDX
SPDX
Image signing
Cosign
Signing by digest
Image attestations/provenance
Deployment workflows
Build → scan → sign → deploy
Deployment environments
Approval gates
GitHub Actions security best practices
Pinning actions
Least privilege
OIDC instead of long-lived AWS keys
Dependency review
Secret handling