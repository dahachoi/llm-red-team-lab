# LLM Red Team Lab

Hands-on offensive security research against large language model
applications: prompt injection, agentic tool abuse, and automated
vulnerability scanning. Each exercise documents the target, the
technique, the root cause, and the mitigation.

## Focus

Application-layer LLM vulnerabilities. These are the failure modes that
appear when models are wired into tools, agents, and retrieval systems,
where the security-relevant behavior lives in the application rather
than in the model weights alone.

## Environment

- **Local inference:** Ollama (mistral-nemo, llama3.2). All testing
  runs against locally hosted models, with no external API dependency.
- **Language:** Python 3.11, Jupyter
- **Targets:** run in isolation, separate from this repo's history

## Contents

| Area | Status | Notes |
|------|--------|-------|
| Damn Vulnerable LLM Agent | Recon complete | ReAct-based agent; Thought/Action/Observation injection |
| MCP server security | Planned | Tool poisoning, indirect injection |
| garak automated scanning | Planned | Custom probe and detector |

## Structure

- `labs/` contains per-target recon notes and exploitation writeups
- `notebooks/` contains analysis and tooling

## Note

All work is performed against deliberately vulnerable applications in a
local environment, for educational and defensive research purposes.