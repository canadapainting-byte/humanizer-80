# T3: Marketing README rewrite (Humanize mode)

## Purpose

Marketing-flavored technical prose rewrites in Humanize mode. Marketing adjectives go. Facts stay.

## Mode

Humanize 80% (default).

## Input

> Our groundbreaking platform leverages a robust, seamless engine to deliver a world-class experience. It is not just a tool, it is a new way to think about teamwork. Additionally, our meticulous team showcases cutting-edge features every week.

## Expected behavior

- The rewrite removes each marketing adjective: groundbreaking, robust, seamless, world-class, cutting-edge.
- The rewrite removes the "not just X" framing and the "Additionally" opener.
- Each fact stays: platform, engine, teamwork, weekly features.
- No new fact appears.

## Pass criteria

- `python scripts/ste_check.py` (run from the skill folder in the full-cli edition) on the rewrite reports no `word` or `not-x-but-y` finding for the words above.
- All four facts above appear in the rewrite.
