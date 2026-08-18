# AgentCore Is the Current Path, Not Bedrock Agents Classic

User asked directly about AgentCore, how Knowledge Base RAG works internally, and how to build multi-agent systems on Bedrock — a natural deepening after [[0003-bedrock-genai-scope-added]]'s base invocation lesson.

**Evidence:** Requested all three topics in one question, prompting research into current (2026) AWS docs before teaching — Bedrock Agents Classic (the original console-based Agents feature with multi-agent collaboration) turned out to be closed to new customers and in maintenance mode, superseded by AgentCore as the actively developed path.

**Implications:** Any future lesson touching Bedrock agents should build on AgentCore (Runtime, Gateway, Identity, Memory, Observability) and frameworks like Strands Agents SDK or LangGraph — not the console Agents/action-groups workflow, which is legacy. User now has the RAG ingestion/query mechanics (chunk → embed → index; Retrieve vs RetrieveAndGenerate) and the three Strands orchestration patterns (Graph, Workflow, Swarm) for multi-agent design. Natural next steps: AgentCore Identity in depth, Guardrails configuration, or a hands-on Strands + AgentCore Runtime walkthrough once the user wants to actually build the app's AI feature rather than continue at the architecture level.
