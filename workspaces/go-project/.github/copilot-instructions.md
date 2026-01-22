# Copilot Workspace Instructions (Go Project)

## Purpose
These instructions define the **mandatory** operating standards for this enterprise Go workspace. They are **non-optional** and apply to all work performed here.

## Non-Negotiable Requirements
- **Security First (Enterprise):** Follow least-privilege, zero-trust assumptions, and secure-by-default coding. Never expose secrets, credentials, tokens, or proprietary data. Sanitize logs and error messages. Avoid unsafe defaults and insecure network calls.
- **No MCP Servers:** **MCP servers are forbidden** in this workspace. Do not configure or use MCP servers.
- **FAANG-Grade Quality (Minimum):** Code must be scalable, readable, tested, and maintainable with strong correctness guarantees, clear interfaces, and robust error handling.
- **Agentic Execution:** Use agentic workflows wherever possible, delegating to specialized agents for planning, review, and execution.
- **Approval Gate:** **No code changes** are allowed until the user explicitly approves the PRD and the TODO plan.

## Mandatory Workflow (Strict)
1. **PRD Agent (Planner):**
   - Produce a complete PRD and high-level plan.
   - Must identify scope, constraints, risks, and success metrics.
2. **Parallel Reviews (Go + XML):**
   - PRD is reviewed **in parallel** by:
     - **SPEC Agent** (Go + XML focus)
     - **SENIOR SOFTWARE ENGINEER Agent** (Go + XML focus)
   - **SPEC Agent** must produce an **exhaustive spec sheet** covering all project aspects, industry-standard requirements, and making **privacy and security the primary concerns**.
3. **Task Planner:**
   - Creates an **elaborate TODO** with ordering, dependencies, and acceptance criteria.
   - The TODO is stored centrally at **/TODO.md**.
4. **User Approval Gate:**
   - The user **must approve** the PRD and TODO before any coding begins.
5. **Module Implementation (Multiple Agents):**
   - After approval, **multiple agents** build modules in parallel.
6. **Testing & Senior Review (Mandatory):**
   - **All code** must be exhaustively unit tested.
   - **Senior Engineer Agent** must review all code **before delivery**.
7. **Error Handling Policy:**
   - Any errors, test failures, or issues are added back to **/TODO.md** at **highest priority**, with concrete correction suggestions.

## Tooling Policy (Massive Tool Library, No MCP)
Use any applicable tools available in this environment (search, read, edit, diagnostics, tasks, terminal, diffs, etc.), **except MCP servers**. Prefer tooling over manual reasoning when it improves accuracy or safety.

## Engineering Standards (Go + XML)
- Idiomatic Go, explicit errors, contexts, and concurrency safety.
- Strict linting and formatting.
- XML handling must be secure (no unsafe entity expansion; validate schemas if provided).
- Unit tests must be comprehensive: table-driven tests, edge cases, and concurrency tests where relevant.

## Security & Compliance Checklist (Required)
- No hard-coded secrets or credentials.
- Validate all external input.
- Use secure defaults and explicit configuration.
- Threat-model any public APIs or file IO.
- Ensure logs do not leak sensitive data.

## Communication & Delivery
- Provide proposals first.
- Keep responses concise, professional, and technical.
- Always link to relevant files when referencing changes.
