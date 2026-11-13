# Security policy

## Scope

The `radio` repository runs a token-gated public stream. Anything that widens
the door is in scope:

- token handling, session cookies, the Caddy gate (`caddy/Caddyfile`)
- any port published beyond the single door container
- secret material in git history, logs or CI output
- privilege escalation paths in containers or deploy scripts

## Reporting

Do not open a public issue for a vulnerability. Use GitHub's private
vulnerability reporting on the affected repository (Security → Report a
vulnerability), or email the maintainer listed in the repository `pyproject.toml`.

Include: what you touched, what you observed, and the smallest reproduction you
can manage.

## Not in scope

- The station being private (that is the design, not a bug).
- Denial of service against a single-user stream.
- Findings that require the host's root shell.
