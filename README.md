# job-application-tracker

> Seniors applying to new-grad roles waste time re-checking listings they have
> already applied to or already dismissed. The smallest version is a command
> that takes a job posting URL and logs it to a file, flagging anything that
> duplicates a role already in the log.

A command-line tool for keeping one honest record of every role you have
touched, so you stop opening the same listing three times in a week.

## The problem

New-grad listings get reposted constantly — the same role shows up under a
different URL, through a different job board, weeks apart. Without a record you
re-read a posting you already rejected, or worse, apply twice to the same job.

## What the MVP does

One command. You give it a URL, it writes a line to a local file, and it tells
you if you have seen that role before.

```bash
jobs add https://example.com/careers/data-analyst-2027
```

```text
Added: Example Corp — Data Analyst (New Grad 2027)
```

Run it on something you already logged:

```text
Already logged 2026-11-03 as "applied" — Example Corp, Data Analyst
```

## Planned commands

| Command | What it does |
| --- | --- |
| `jobs add <url>` | Log a posting; warn if it duplicates one already logged |
| `jobs list` | Show everything logged, newest first |
| `jobs status <id> <state>` | Mark a role applied / rejected / interviewing |

## Status

Early. Scope defined, MVP in progress. See [Issues](../../issues) for what's next.

## Setup

Not runnable yet. Setup and run instructions land here with the MVP.
