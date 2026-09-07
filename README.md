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
| 13 | [S3 Object Storage](lessons/0013-s3-object-storage.html) | Buckets, storage classes, versioning, encryption |
| 14 | [Amazon Bedrock](lessons/0014-bedrock-genai.html) | Managed FM inference, Knowledge Bases, Guardrails, PrivateLink |
| 15 | [AgentCore, RAG & Multi-Agent](lessons/0015-agentcore-rag-multiagent.html) | AgentCore components, RAG internals, Strands orchestration patterns |
| 16 | [Lambda + Bedrock Agent Tools](lessons/0016-lambda-bedrock-agent-tools.html) | Tool-call loop, Gateway Lambda targets, event/response contract, entitlement checks, 10-step agentic build |
| 17 | [Amazon DynamoDB](lessons/0017-dynamodb.html) | Serverless NoSQL data model, boto3 CRUD, Query vs Scan, DynamoDB as AgentCore tool store and agent memory/audit |
| 18 | [AWS CDK](lessons/0018-aws-cdk.html) | App/Stack/Construct model, L1/L2/L3, synth/diff/deploy/bootstrap, grants, template tests, CDK vs Terraform |

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
git clone https://github.com/brendanteach/aws.git
cd aws
open index.html   # macOS
start index.html  # Windows
```

## Structure

```
aws/
├── index.html          # lesson index with descriptions
└── lessons/
    ├── 0001-aws-architecture-map.html
    ├── 0002-vpc-networking.html
    ├── ...
    └── 0012-cicd.html
```
