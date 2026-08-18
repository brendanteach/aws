# Mission: AWS Architecture for Financial Web Applications

## Why
To design and deploy a production-grade financial web application — with frontend, backend, and database — using AWS-native services, leveraging existing Azure familiarity to accelerate the transition.

## Success looks like
- Able to draw a complete AWS architecture diagram for a financial web app from memory
- Know which AWS service to reach for in place of each Azure service used today
- Understand how to wire together frontend (S3/CloudFront), backend (ECS or Lambda), and database (RDS) on AWS
- Understand IAM, VPC, and security fundamentals well enough to make production-safe decisions
- Can articulate trade-offs between AWS architectural options (e.g. serverless vs containers, RDS vs DynamoDB)

## Constraints
- Has Azure experience — teach by analogy where it accelerates understanding, but flag where AWS differs meaningfully
- Goal is architectural understanding for real production use, not certification prep
- Finance domain: security, compliance (audit logging, encryption at rest/transit), and availability matter

## Out of scope
- AWS DevOps/CI-CD tooling (CodePipeline, CodeBuild) — unless it comes up naturally
- Custom ML model training/hosting (SageMaker etc.) — not the current goal
- Cost optimization deep-dives — note costs in passing but don't go deep

## Scope note (added 2026-08-17)
Generative AI is now in scope, specifically **Amazon Bedrock**, to support adding an AI feature (chat assistant / document analysis / similar) to the financial web app. This is managed foundation-model inference (Bedrock), not custom model training (SageMaker remains out of scope). See [[0003-bedrock-genai-scope-added]].
