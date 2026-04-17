# Security Policy

## Reporting a vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Report privately via one of:

1. **GitHub Private Vulnerability Reporting** (preferred) — [report here](https://github.com/knowledgestack/ks-sdk/security/advisories/new).
2. **Email** — `security@knowledgestack.ai` (include "ks-sdk" / `ksapi` in the subject).

Include where possible:

- Affected version (`ksapi` PyPI version or commit SHA)
- Reproduction steps
- Impact (credential exposure, code execution, privilege escalation, DoS)
- Proof-of-concept if you have one

## Scope

This package is **generated from the Knowledge Stack OpenAPI spec**. In-scope security issues include:

- Vulnerabilities in generated client code (e.g. auth handling, request construction, response parsing)
- Supply-chain concerns in the published PyPI artifact
- CI / release pipeline misconfigurations

Out of scope (report to `security@knowledgestack.ai` directly):

- Vulnerabilities in the hosted Knowledge Stack API — those live on the backend
- Issues in forks or in generated clients for other languages hosted elsewhere

## Response

- Acknowledgement within **2 business days**
- Triage within **5 business days**
- Critical fixes target **7 days**
- Default disclosure window: **90 days** from report, adjusted by mutual agreement

## Safe harbor

Good-faith security research is welcomed. We won't pursue legal action against researchers who respect privacy, only test accounts they own, give us time to fix before disclosing, and don't monetize pre-disclosure.
