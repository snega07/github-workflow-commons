IDE:

Static code analysis - Software composition analysis(checks libraries we are using)(SCA), Static Application Security Testing(SAST) 
secret scanner - pre-commit in github repo

In pipeline:

SBOM - Artifact generated during build stage, with versions of third party libraries. We can run this periodically to scan the new vulnerability.

In Testing:
Owasp zap
Dynamic Application Security Testing(DAST) -SQl injection, hyjacking, cross site injection

Artifactory: Image scanners

Scan images for vulnerabilties in the Docker Hub, Jfrog

Find vulnerability

docker scout
docker scout cves

How to fix -> chaingaurd(distroless image for nginx, go and other)

use alpine images with limited libraries
distroless

SBOM generation

Secret Scanner → "Did I leak a secret?"

SAST           → "Is my CODE insecure?"

SCA            → "Are my DEPENDENCIES insecure?"

SBOM           → "WHAT COMPONENTS are in my software?"

CVE Scan       → "Are those components KNOWN to be vulnerable?"

DAST           → "Can I ATTACK the RUNNING application?"


| Area                     | Purpose                                          | Recommended tool | Alternative                  |
| ------------------------ | ------------------------------------------------ | ---------------- | ---------------------------- |
| **Secret scanning**      | Detect leaked API keys, passwords, tokens        | **Gitleaks**     | TruffleHog                   |
| **SAST**                 | Find security issues in your own source code     | **Semgrep**      | SonarQube                    |
| **SCA**                  | Find vulnerable Maven/npm dependencies           | **Snyk**         | OWASP Dependency-Check       |
| **SBOM**                 | Generate inventory of software components        | **Syft**         | Trivy                        |
| **CVE / image scanning** | Find vulnerabilities in Docker image             | **Trivy**        | Docker Scout, Snyk Container |
| **Image signing**        | Sign/prove authenticity of image                 | **Cosign**       | Notary                       |
| **DAST**                 | Test running application for web vulnerabilities | **OWASP ZAP**    | Burp Suite                   |
| **IaC scanning**         | Find Terraform/K8s misconfigurations             | **Checkov**      | tfsec, Trivy                 |
| **K8s security**         | Scan Kubernetes manifests/configuration          | **Kubescape**    | Trivy                        |
| **Container runtime**    | Detect runtime threats                           | **Falco**        | Tetragon                     |
| **Dependency updates**   | Automatically detect outdated dependencies       | **Dependabot**   | Renovate                     |
