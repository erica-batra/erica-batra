# Hey, I'm Erica

**Infrastructure Security Engineer** | Cloud Security & IAM | Former DevOps

I spent the better part of five years building and running cloud infrastructure. Started in DevOps, ended up in security. Not because I planned it that way, but because after the hundredth time debugging why some service account had admin access to everything, I realized the problems I actually wanted to solve were security problems.

## How I Got Here

The transition from DevOps to infrastructure security wasn't really a pivot. More like... following breadcrumbs I was already leaving for myself.

```
2018-2021: DevOps Engineer
├─ Built CI/CD pipelines
├─ Managed AWS infrastructure
├─ Automated everything I could
└─ Started noticing security gaps

2021-2023: DevOps + Security Interest
├─ Kept finding IAM misconfigurations
├─ Started learning threat modeling
├─ Built security tools on weekends
└─ Realized this was more interesting than uptime

2023-Present: Infrastructure Security Engineer
├─ Full focus on cloud security
├─ IAM architecture and threat modeling
├─ Building security that doesn't break workflows
└─ Still automating everything
```

The DevOps background turned out to be useful. I already knew how infrastructure worked, how teams operated, and where things typically went wrong. Now I just think about it through a security lens.

## What I Actually Do

Right now I'm focused on making cloud infrastructure harder to compromise without making it harder to use. That's the trick, really—security that gets in the way just gets bypassed.

**Main areas:**
- Cloud IAM design (mostly AWS, because that's where the complexity lives)
- Infrastructure security architecture
- CI/CD pipeline security
- Policy as code
- Threat modeling for infrastructure

**The DevOps perspective matters:**

Coming from operations means I know where flexibility is actually needed versus where you need hard controls. I've seen what happens when security becomes a bottleneck—people find creative workarounds. So I try to build security that fits into existing workflows instead of fighting them.

Also learned that detection matters as much as prevention. You're not going to stop every attack. Better to know when something's happening and have a plan for it.

## My Approach to Security

A few things I've learned (some the hard way):

**Least privilege actually means least privilege.** Not "least privilege except for this one service account that needs admin because it's easier." Every wildcard permission is a future incident waiting to happen.

**Defense in depth isn't optional.** One control fails? You want another one to catch it. Then another one after that. Layers matter.

**Assume breach.** Design like someone's already inside your network, because statistically, they might be. Limit blast radius, segment access, log everything.

**Automate or it won't happen.** Manual security processes don't scale. They get skipped when people are busy, which is always. If it's not automated, it's not really a control.

**You can't protect what you can't see.** Logging and monitoring aren't nice-to-haves. They're how you know if any of your other controls are actually working.

## Tech Stack

**Cloud Platforms:**
AWS (primary), Azure, GCP

**Identity & Access:**
AWS IAM, Azure AD, Okta, SAML/OIDC federation

**Infrastructure as Code:**
Terraform (daily), CloudFormation (when required), experimenting with Pulumi

**Policy Engines:**
Open Policy Agent, HashiCorp Sentinel, Cloud Custodian

**Security Tools:**
ScoutSuite, Prowler, CloudMapper, Trivy, Checkov, Prowler

**CI/CD:**
GitHub Actions, GitLab CI, Jenkins, Bitbucket Pipelines

**Containers & Orchestration:**
Docker, Kubernetes, ECS, EKS

**Secrets Management:**
HashiCorp Vault, AWS Secrets Manager, Azure Key Vault

**Languages:**
Python (for tools), Bash/PowerShell (for scripts), HCL (Terraform), YAML (for everything else apparently)

**Detection & Monitoring:**
CloudWatch, CloudTrail, VPC Flow Logs, AWS Security Hub, GuardDuty

## Projects & Research

### Infrastructure Security Scenarios

Hands-on scenarios for securing cloud infrastructure. Each one has:
- Threat model (what are we defending against?)
- Baseline insecure setup
- Hardened configuration
- Attack simulations
- Detection mechanisms

**Current scenarios:**
- VPC security and network segmentation
- Container security (Docker hardening, secrets management)
- More coming (IAM escalation, secrets management, compliance)

These aren't theoretical. I built them to learn this stuff myself. Deploy the insecure version, attack it, see what breaks. Then deploy the hardened version and verify the attacks don't work anymore.

### Cloud IAM Architecture

IAM is complicated. This is me documenting patterns I've learned—often the hard way.

**What's in there:**
- Federation setups (SAML, OIDC)
- Cross-account access patterns
- Privilege escalation paths (there are more than you think)
- Trust policy analysis
- Defensive IAM architectures

Also built a policy analyzer tool that scans IAM policies for common issues. Catches things like admin wildcards, unrestricted PassRole, privilege escalation vectors. Tested it against 19 different policy scenarios—100% detection rate, zero false positives.

### Security Tools I've Built

**IAM Policy Analyzer**
Scans IAM policies for security issues. Detects admin wildcards, privilege escalation actions, dangerous permissions, loose trust policies. Python-based, works on single files or entire directories.

**AWS Misconfiguration Scanner**
Checks live AWS accounts for common security gaps. Public S3 buckets, overly permissive security groups, IAM users without MFA, missing CloudTrail, unencrypted resources. Provides remediation guidance.

**Privilege Escalation Detector**
Identifies IAM privilege escalation paths in policies. Covers single-action techniques (like PutUserPolicy) and combination attacks (PassRole + Lambda). Explains exploitation methods and mitigations.

All three tools are production-ready with comprehensive test suites.

### Other Research Areas

**Secure CI/CD Patterns**
How to not make your pipeline the weakest link. Artifact verification, secrets management, least privilege for runners, supply chain security, policy enforcement.

**Policy as Code Framework**
Production examples using OPA, Sentinel, Cloud Custodian. Governance policies, compliance checks, automated remediation.

**Zero Trust Infrastructure**
Implementation patterns for zero trust in cloud environments. Network micro-segmentation, identity-based access, continuous verification.

**Threat Modeling for IAM**
Frameworks for modeling identity-based threats. Attack paths, escalation techniques, defensive architectures.

**Network Security Architecture**
VPC design patterns, transit gateways, PrivateLink, service mesh security, egress controls.

**Secrets Management**
Vault integration, dynamic credentials, rotation strategies, least privilege access to secrets.

**Security Guardrails for DevOps**
Shift-left security, automated policy checks, developer-friendly controls that actually get used.

## My Security Research

I keep a separate research repo where I experiment with different security concepts:

**Areas I'm exploring:**
- Vulnerability research and analysis
- Penetration testing methodologies
- Malware analysis techniques
- Incident response procedures
- Threat modeling frameworks
- Exploit development (in controlled environments)
- Bug bounty approaches
- Zero trust architectures

It's a mix of learning by doing, documenting what I find, and building tools to automate the boring parts.

## Certifications

**Current:**
- AWS Certified Solutions Architect - Professional
- AWS Certified Solutions Architect - Associate

**In progress:**
- AWS Certified Security - Specialty
- CISSP

## What I'm Learning Right Now

**IAM federation in practice.** The documentation makes it sound straightforward. It's not. There are edge cases everywhere, and the trust relationships get complicated fast.

**Privilege escalation paths in AWS.** Turns out there are dozens of ways to go from limited permissions to admin. I'm documenting them, building detection for them, and figuring out how to prevent them architecturally.

**Container security beyond the basics.** Distroless images, runtime protection, secrets management, escape prevention. Docker makes it easy to deploy things. Also makes it easy to deploy insecure things.

**Building detection that actually works.** Prevention is great, but you need to know when something bad is happening. Working on CloudWatch queries, Security Hub rules, and custom detection logic that catches real attacks without drowning you in false positives.

## Career Transition: DevOps to Security

If you're thinking about making a similar move, here's what helped me:

**Start where you are.** I was already dealing with IAM policies, security groups, and access controls in DevOps. Just started paying more attention to the security implications.

**Build things.** Reading about security is useful. Building security tools and breaking things in test environments is how you actually learn.

**Document everything.** This GitHub is basically my learning journal. Writing things down forces you to understand them well enough to explain them.

**The DevOps skills transfer.** Infrastructure knowledge, automation, CI/CD, scripting—all of it's useful in security. You're just applying it differently.

**Security is a mindset shift.** In DevOps, you're optimizing for availability and speed. In security, you're thinking about what could go wrong and how to limit the damage when it does.

## How My GitHub is Organized

```
erica-batra (you are here)
├─ Profile and overview
│
├─ Infrastructure Security Scenarios
│  ├─ VPC Security (complete)
│  ├─ Container Security (complete)
│  └─ More scenarios (in progress)
│
├─ Security Tools
│  ├─ IAM Policy Analyzer
│  ├─ AWS Misconfiguration Scanner
│  └─ Privilege Escalation Detector
│
├─ Architecture & Patterns
│  ├─ Cloud IAM Architecture
│  ├─ Zero Trust Infrastructure
│  ├─ Network Security Architecture
│  └─ Secrets Management Patterns
│
├─ CI/CD & DevOps Security
│  ├─ Secure CI/CD Patterns
│  ├─ Security Guardrails for DevOps
│  └─ Policy as Code Framework
│
└─ Research
   ├─ Sec-Research (private)
   ├─ IAM Threat Modeling
   └─ Cloud Security Projects
```

## Some Things I've Learned

**Security theater is worse than no security.** Controls that don't actually work but make people feel safe are dangerous. Better to know you're exposed than think you're protected when you're not.

**Make the secure way the easy way.** If your security process is painful, people will find ways around it. Design security that fits into workflows, not against them.

**Developers aren't the enemy.** They're trying to ship features. If your security controls break their workflow, they'll bypass them. Work with them, not against them.

**Perfect is the enemy of good enough.** You can't secure everything perfectly. Prioritize based on actual risk, not theoretical worst cases.

**Detection matters as much as prevention.** You're not going to stop every attack. Know when something's happening and have a response plan.

**Automation is your friend.** Manual security processes don't scale. They get skipped when people are busy. Automate or accept that it won't happen consistently.

## Get in Touch

**Email:** erica.batra@gmail.com  
**Location:** Canada  
**LinkedIn:** [linkedin.com/in/erica-batra](https://linkedin.com/in/erica-batra)

Always happy to talk about infrastructure security, IAM architecture, career transitions from DevOps to security, or why your service account probably has too many permissions.

## A Note on This Profile

This GitHub is me learning infrastructure security in public. I'm documenting what I'm figuring out as I transition from DevOps to security engineering.

Everything here is:
- Technically solid (I test it)
- Based on real scenarios, not just theory
- Something I can explain if asked
- Honest about what I know versus what I'm still learning

I believe in learning by doing. These repos are me building things to understand them better. Some of it's polished, some of it's rough, all of it's real work.

If you're on a similar path—DevOps to security, operations to engineering, builder to defender—feel free to reach out. Always happy to compare notes.

---

*Last updated: January 2025*
