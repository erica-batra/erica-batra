# Hey, I'm Erica 👋

**Infrastructure Security Engineer** • Cloud Security & IAM • Former DevOps

## About Me

I spent years building and running cloud infrastructure as a DevOps engineer. Somewhere along the way, I realized I was more interested in *securing* the platforms I built than just keeping them up. So I made the shift to infrastructure security—with a focus on identity, access management, and building security controls that actually work in production (not just in theory).

### How I Got Here: DevOps → Security

This wasn't really a career pivot—more like following what I was already gravitating toward. After enough late nights debugging why some service account had way too many permissions, or figuring out how an attacker could move laterally through our VPCs, I realized security problems were the ones I actually enjoyed solving.

The transition made sense:
- I already understood cloud infrastructure deeply—now I'm focused on securing it
- I knew how DevOps teams worked—now I'm building security guardrails they'll actually use
- I'd automated deployments for years—now I'm automating security policies and detection
- I understood "is it fast enough?"—now I also ask "who can access this, and should they?"

This GitHub is basically my learning journal as I've gone deeper into infrastructure security, IAM design, and building defensible cloud architectures.

## What I Focus On

### Main Areas
Right now I'm deep in:
- **Cloud IAM** - Identity federation, cross-account patterns, privilege escalation paths, all that fun stuff
- **Infrastructure Security** - VPC design, network segmentation, hardening compute environments
- **CI/CD Security** - Making pipelines secure without slowing down deployments (the eternal challenge)
- **Policy as Code** - OPA, Sentinel, Cloud Custodian—encoding security rules that actually get enforced
- **Threat Modeling** - Thinking through how things break and designing accordingly

### The DevOps Perspective

Coming from DevOps definitely shapes how I approach security:
- I know where developers need flexibility and where you actually need controls
- I'm allergic to security theater—controls need to be operationally sustainable
- If a security process creates a bottleneck, people will find creative ways around it
- Automation is your friend (for security checks too, not just deployments)
- Detection matters as much as prevention—you're not stopping every attack

Basically: security needs to fit into how teams actually work, not the other way around.

## Tech I Work With

**Cloud**: AWS mostly (it's where the IAM complexity lives), some Azure and GCP  
**IAM/Identity**: AWS IAM, Azure AD, Okta, federation (SAML/OIDC)  
**IaC**: Terraform primarily, CloudFormation when I have to, experimenting with Pulumi  
**Policy Engines**: OPA, Sentinel, Cloud Custodian  
**Security Scanning**: ScoutSuite, Prowler, CloudMapper, Trivy, Checkov  
**CI/CD**: GitHub Actions, GitLab CI, Jenkins (legacy but still everywhere)  
**Containers**: Docker, K8s, ECS/EKS, admission controllers  
**Secrets**: Vault, AWS Secrets Manager, Key Vault  
**Languages**: Python for tooling, Bash/PowerShell for scripts, HCL for Terraform, YAML for everything else apparently  
**Detection**: CloudWatch, CloudTrail, VPC Flow Logs, Security Hub, GuardDuty

## Projects I'm Working On

### Main Repos

#### 🔐 [cloud-iam-architecture](https://github.com/erica-batra/cloud-iam-architecture)
IAM is complicated. This repo is me documenting patterns I've learned (often the hard way) - federation setups, cross-account access, how privilege escalation actually happens, etc. More "here's what I figured out" than "definitive guide."

#### 🏗️ [infrastructure-security-scenarios](https://github.com/erica-batra/infrastructure-security-scenarios)
Hands-on exercises for securing infrastructure - VPCs, compute instances, network segmentation, all that. I built these while learning this stuff myself. Each scenario has a threat model (what are we defending against?), implementation steps, and how to actually detect if someone's doing what we're trying to prevent.

#### 🔧 [secure-ci-cd-patterns](https://github.com/erica-batra/secure-ci-cd-patterns)
How to not make your CI/CD pipeline the weakest link. Covers artifact verification, secrets management (please don't commit your AWS keys), least privilege for runners, supply chain stuff, and where to put policy checks so they actually get run.

#### 🕵️ [iam-threat-modeling](https://github.com/erica-batra/iam-threat-modeling)
Threat modeling frameworks specifically for identity and access management. Covers attack paths, privilege escalation techniques, and defensive architectures.

#### 📋 [policy-as-code-framework](https://github.com/erica-batra/policy-as-code-framework)
Production-ready policy-as-code examples using OPA, Sentinel, and Cloud Custodian. Includes governance policies, compliance checks, and automated remediation.

#### 🔍 [cloud-misconfiguration-scanner](https://github.com/erica-batra/cloud-misconfiguration-scanner)
Custom tools for detecting cloud misconfigurations: public resources, overly permissive IAM policies, missing encryption, weak network controls.

#### 🛡️ [zero-trust-infrastructure](https://github.com/erica-batra/zero-trust-infrastructure)
Zero trust architecture implementation for cloud infrastructure. Network micro-segmentation, identity-based access, continuous verification.

#### 🔑 [secrets-management-patterns](https://github.com/erica-batra/secrets-management-patterns)
Secure secrets management patterns: Vault integration, dynamic credentials, rotation strategies, least privilege access to secrets.

#### 🌐 [network-security-architecture](https://github.com/erica-batra/network-security-architecture)
Network security at scale: VPC design patterns, transit gateways, PrivateLink, service mesh security, egress controls.

#### 🚧 [security-guardrails-devops](https://github.com/erica-batra/security-guardrails-devops)
Security guardrails for DevOps teams: shift-left security, automated policy checks, developer-friendly security controls.

### Active Security Research

🔬 [Sec-Research](https://github.com/erica-batra/Sec-Research) - Ongoing security research covering vulnerability analysis, threat modeling, cloud security, and incident response.

☁️ [cloud-security](https://github.com/erica-batra/cloud-security) - Hands-on AWS cloud security labs focusing on IAM, data protection, logging, and infrastructure security.

## 🎓 Certifications

- **AWS Certified Solutions Architect** – Professional
- **AWS Certified Solutions Architect** – Associate

*Working toward: AWS Certified Security - Specialty, CISSP*

## How I Think About Security

### Principles I Try to Follow
1. **Least privilege** - Give the minimum permissions needed. Seriously, stop using `*` in policies
2. **Multiple layers** - If one control fails, you want another one to catch it
3. **Assume you're already compromised** - Design to limit damage, not just prevent entry
4. **Automate everything** - Manual security processes don't scale and get skipped when people are busy
5. **You can't protect what you can't see** - Logging and monitoring aren't optional

### Stuff I Learned from DevOps
- Catch security issues early (shift-left), not in production
- Make the secure way the easy way, or people will route around it
- If developers hate your security controls, you've failed—they'll just find workarounds
- Security can't break normal operations. If it does, it won't last
- Prevention is great, but detection and response are just as important (you won't catch everything)

## What I'm Currently Digging Into

- IAM architectures and how identity federation actually works in practice (it's more complicated than the docs make it sound)
- Building out test environments to practice security controls—can't just read about this stuff
- Privilege escalation paths in AWS (turns out there are a lot of ways to get from limited permissions to full admin)
- Trying to contribute to some open source security tools when I have time
- Writing down patterns that might help other platform/DevOps teams thinking about security

## Get in Touch

**Email**: erica.batra@gmail.com  
**Location**: Canada  
**LinkedIn**: [linkedin.com/in/erica-batra](https://linkedin.com/in/erica-batra)

Always happy to chat about infrastructure security, IAM nightmares, or career transitions.

## Quick Note on This Profile

This GitHub is basically me learning infrastructure security in public. I'm documenting what I'm figuring out as I transition from DevOps to security engineering—building test scenarios, writing tools, and researching how things actually break in cloud environments.

Everything here is meant to be:
- Technically solid (I test this stuff)
- Based on real scenarios, not just theory
- Something I can actually explain if asked (like in an interview)
- Honest about what I know vs what I'm still learning

I'm a big believer in learning by doing. So yeah, that's what these repos are—me building things to understand them better.

---

*"Security is not about making things impossible to break. It's about making the cost of breaking them higher than the value gained."*
