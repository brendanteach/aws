# Lambda Is the "Do" Layer for Bedrock Agents

User asked directly how AWS Lambda works with an agent in Bedrock — a natural deepening after [[0004-agentcore-rag-multiagent]] established the AgentCore component model at the architecture level.

**Evidence:** Single focused question ("How does the aws lambda work with agent in bedrock?"). Grounded against current AWS docs before teaching: AgentCore Gateway Lambda-target event/context contract, tool-name prefix stripping (`<target>___<tool>`), and the Classic action-group response envelope for contrast.

**Implications:** Lesson 16 delivered. User now has the tool-call loop mental model (model decides what, Lambda does how, runtime translates), both integration paths (Gateway target = current, action groups = legacy), the Gateway `event` shape (flat arg map) vs `context` (metadata), and the finance framing that the Lambda — not the model — is the control point for entitlement checks and audit logging. Builds on IAM least-privilege from Lesson 3 and Lambda resource policies from Lesson 10. Natural next steps: hands-on Strands + Gateway walkthrough, AgentCore Identity for passing authenticated user identity into tools, or writing tool schemas the model calls reliably. Still architecture-level — user has not yet started building the actual AI feature.
