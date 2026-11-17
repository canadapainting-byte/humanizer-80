# T2: Identifiers preserved (Humanize mode)

## Purpose

Backticked identifiers, URLs, versions, and numbers stay exact. The rewrite never touches them.

## Mode

Humanize 80% (default).

## Input

> To start the worker, run `npm run worker -- --queue=mail --tries=3` with Node 20. The job writes to `logs/worker-2026-11-17.log` and reports to https://status.example.com. Version 2.3.1 adds the `--dry-run` flag, and 40+ jobs ran fine.

## Expected behavior

- Each identifier appears unchanged in the rewrite: `npm run worker -- --queue=mail --tries=3`, `logs/worker-2026-11-17.log`, https://status.example.com, `2.3.1`, `--dry-run`, `40+`, `Node 20`.
- "40+" stays "40+", not "about 40".
- The prose around the identifiers may change. The identifiers may not.

## Pass criteria

- Exact string match for each identifier listed above.
- The rewrite keeps each identifier exact. It rounds nothing and drops nothing.
