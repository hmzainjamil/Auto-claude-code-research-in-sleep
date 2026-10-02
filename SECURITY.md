# Security and data handling

This repository includes MCP bridges, model clients, research helpers, and monitoring scripts. Review the exact source and configuration before use.

## Research material and providers

MCP review and chat servers send prompts or message content to the configured provider or CLI. Do not send confidential, personal, or unpublished material until you have checked the provider, account, retention terms, and authorization for that data. Some tools make network requests to literature APIs.

## Credentials and local state

- Keep provider keys in protected local environment/configuration, not in Git.
- Review logs, prompt lengths, review history, and state directories for sensitive content.
- Use least-privilege credentials and separate research environments where practical.
- Inspect scripts before running them; the watchdog launches system inspection commands and writes state under its configured directory.

## Reporting

Do not disclose secrets or private research in public issues. Use GitHub private vulnerability reporting if enabled for this repository; otherwise contact the maintainer through the private method on the [GitHub profile](https://github.com/hmzainjamil).

This document is handling guidance, not a security audit or provider guarantee.
