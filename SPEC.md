# Spec

## Scope sentence

Seniors applying to new-grad roles waste time re-checking listings they have
already applied to or already dismissed. The smallest version is a command that
takes a job posting URL and logs it to a file, flagging anything that duplicates
a role already in the log.

## In scope for the MVP

- `jobs add <url>` — fetch the page title, store the entry, warn on a duplicate
- `jobs list` — print the log, newest first
- Storage in one local file (JSON or CSV), created on first run
- Duplicate detection on normalized URL, plus a company + title match

## Out of scope

- Any web interface
- Accounts, hosting, or a database
- Scraping behind a login
- Résumé tailoring, cover letters, or anything involving a model

## Decisions

- **Python.** The language I use most and can debug fastest.
- **A local file, not a database.** One user, one laptop. A database is setup
  cost with no payoff at this size.
- **Normalize URLs before comparing.** Job boards append tracking parameters,
  so `?src=linkedin` must not look like a different job.

## Done means

- A second person follows only the README and gets it running
- Adding the same URL twice produces a warning the second time
- The log survives closing the terminal
