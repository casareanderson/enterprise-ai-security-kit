---
id: "03"
title: Prompt injection is not a prompt problem
theme: AI application security
structure: myth-mechanism
words: 155
sources: [OWASP Top 10 for LLM Applications - LLM01, MITRE ATLAS]
---

POST START

Prompt injection is not a prompt problem. It is a privilege problem.

The mechanism is one every security team already knows: the confused deputy. A trusted process acts on untrusted input, using authority the input's author should never have had.

An LLM reading a web page, a PDF, a support ticket or an email is reading attacker-controlled text. If that model can also call tools, it can be steered.

So stop trying to win the argument at the language layer. You cannot filter your way to safety in natural language.

Constrain the deputy instead:

— Tools get least privilege, per task, not per app
— Irreversible actions require a human confirmation step
— Untrusted content never shares a trust boundary with privileged tools
— Outputs are validated against a schema before anything acts on them

Better prompts reduce the odds. Better privileges reduce the blast radius.

Only one of those survives a determined attacker.

POST END

**Hashtags:** #AppSec #LLMSecurity #CyberSecurity #EnterpriseAI
**Visual:** Optional. A two-box diagram: untrusted input | privileged tools — and the boundary between them.
**Sources:** OWASP Top 10 for LLM Applications (LLM01: Prompt Injection); MITRE ATLAS.
