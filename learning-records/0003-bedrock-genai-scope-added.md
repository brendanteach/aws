# Mission Expanded to Include Amazon Bedrock (GenAI)

User asked to learn Amazon Bedrock's architecture, with the goal of adding an AI feature (chat assistant / document analysis) to the financial web app built in this series.

**Evidence:** Directly requested "what is architecture of aws bedrock solution?" tied to wanting a diagram and lesson; confirmed via clarifying question that the driver is an AI feature in the app, not general breadth or a vendor comparison.

**Implications:** MISSION.md updated to bring generative AI (Bedrock) in scope, while keeping custom ML training (SageMaker) out of scope — the distinction is managed foundation-model *inference* vs. training your own models. Bedrock lessons should build on the existing three-tier architecture ([[0002-core-architecture-complete]]): the app's ECS/Lambda backend calls Bedrock the way it currently calls RDS — as another managed AWS service reached over IAM-scoped API calls, ideally via VPC PrivateLink for a finance context. Future lessons can go deeper on Knowledge Bases (RAG over the app's own documents) and Guardrails (content/PII filtering) once the basic invocation pattern lands.
