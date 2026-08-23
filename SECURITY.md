# Security Policy

## Supported versions

Security fixes should target the latest version on the default branch.

## Reporting a vulnerability

Do not report vulnerabilities publicly. Use GitHub's **Security** tab and
**Report a vulnerability** when available, or contact the upstream Docker
maintainers through a verified private channel.

Provide reproduction steps, affected services and versions, impact, and a
minimal proof of concept using synthetic data. Never include real API keys,
AWS credentials, database passwords, prompts, retrieved documents, or tracing
data. Revoke any credential that may have been exposed.

## Deployment guidance

This repository contains development examples and is not production-hardened.

- Replace all example and default credentials before exposing any service.
- Keep `.env` files out of version control.
- Bind Neo4j, Ollama, and application ports only to trusted interfaces.
- Restrict cloud credentials to the minimum required permissions.
- Treat prompts, model output, retrieved documents, and uploaded files as
  untrusted input.
- Review what is sent to external LLM, embedding, and tracing providers.
- Do not put confidential data into LangSmith traces or logs.
- Pin and review container images and dependencies before deployment.
