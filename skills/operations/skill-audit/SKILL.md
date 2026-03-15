---
name: skill-audit
description: Audit skills for security and quality before installation or activation. Use when reviewing third-party skills or validating internal SKILL.md files and scripts.
---

# Skill Audit

## Audit Scope

- `SKILL.md` quality and trigger clarity
- script safety (`scripts/`)
- data access behavior
- external calls and exfiltration risk

## Process

1. Check for dangerous patterns:
   - `rm -rf`
   - `eval` / dynamic shell execution
   - blind `curl|bash`
2. Check sensitive file access attempts:
   - SSH keys
   - local credential stores
   - hidden config/secrets
3. Check network behavior:
   - unexplained external POST/upload
   - hardcoded endpoints for data export
4. Check quality:
   - clear purpose
   - deterministic workflow
   - minimal permissions

## Classification

- **LIMPO**: no material risk found
- **ATENÇÃO**: suspicious or unclear behaviors
- **CRÍTICO**: clear unsafe behavior; do not install

## Output

Return:

- risk level
- findings list
- remediation actions
- final recommendation (`install` / `review first` / `block`)
