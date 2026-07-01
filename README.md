# AWS Architecture — 12-Lesson Series

A self-paced curriculum for building a production-grade financial web app on AWS. Taught by analogy to Azure — if you know Azure, this series maps every concept to what you already understand.

## What You'll Build

A complete financial web application stack:

```
Users → CloudFront → S3 (React SPA)
                  → ALB → ECS Fargate (Python API)
                              → RDS PostgreSQL (Multi-AZ)
                              → ElastiCache Redis
                              → SQS → Lambda (async jobs)
Cognito (auth) · Secrets Manager · CloudWatch · X-Ray
```

## Lessons

| # | Title | Topics |
|---|-------|--------|
| 01 | [AWS Architecture Map](lessons/0001-aws-architecture-map.html) | Azure→AWS translation, full stack overview, 3 key differences |
| 02 | [VPC Networking](lessons/0002-vpc-networking.html) | Subnets, Security Groups, NAT Gateway, traffic flow |
| 03 | [IAM](lessons/0003-iam.html) | Roles, policies, ARNs, Task Role vs Execution Role |
| 04 | [ECS Fargate](lessons/0004-ecs-fargate.html) | Containers, rolling deploys, auto-scaling, secrets |
| 05 | [RDS PostgreSQL](lessons/0005-rds.html) | Multi-AZ, encryption, RDS Proxy, backups |
| 06 | [S3 + CloudFront](lessons/0006-frontend-s3-cloudfront.html) | OAC, ACM cert, SPA routing fix, cache headers |
| 07 | [Complete Architecture](lessons/0007-complete-architecture.html) | All services together, provisioning order, open decisions |
| 08 | [Cognito](lessons/0008-cognito.html) | User Pools, JWT flow, local token validation, TOTP MFA |
| 09 | [Terraform](lessons/0009-terraform.html) | HCL, remote state, modules, real resource blocks |
| 10 | [SQS + Lambda](lessons/0010-sqs-lambda.html) | Async jobs, DLQ, visibility timeout, batchItemFailures |
| 11 | [CloudWatch](lessons/0011-cloudwatch.html) | Structured logging, alarms checklist, X-Ray tracing |
| 12 | [CI/CD with GitHub Actions](lessons/0012-cicd.html) | OIDC auth, parallel deploy pipeline, ECS rolling deploy |

Each lesson includes:
- Azure analogies for every concept
- Financial-app specific callouts (compliance, security, HA)
- Annotated code samples (Python, HCL, YAML, JSON)
- A 4-question quiz with immediate feedback

## Prerequisites

- Familiarity with web application concepts (frontend / backend / database)
- Azure cloud experience is useful but not required
- No prior AWS experience needed

## How to Use

Open [index.html](index.html) in a browser to navigate the series, or open any lesson file directly. Each lesson is a self-contained HTML file — no build step, no dependencies.

To view with working navigation links, clone and open locally:

```bash
git clone https://github.com/liubrend/teach-aws.git
cd teach-aws
open index.html   # macOS
start index.html  # Windows
```

## Structure

```
teach-aws/
├── index.html          # lesson index with descriptions
└── lessons/
    ├── 0001-aws-architecture-map.html
    ├── 0002-vpc-networking.html
    ├── ...
    └── 0012-cicd.html
```
