# Project constraints

## Scope

- Build only what the scope sentence in SPEC.md describes.
- Python, standard library first. Justify any dependency before adding it.
- No web interface, no database, no accounts.

## Style

- Small functions with clear names. Comments explain why, not what.
- Fail with a readable message, not a traceback, when a URL is unreachable.

## Verification

- Check syntax before claiming something works.
- Tell me what you actually ran and what came back. A claim is not evidence.

## Safety

- Never commit credentials, tokens, or personal data.
- The log file stays local and gitignored.
- Do not commit or push on my behalf.
