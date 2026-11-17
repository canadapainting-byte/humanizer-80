# T1: Word cap (Humanize mode)

## Purpose

A sentence over the 25-word description cap splits into shorter sentences. No fact drops.

## Mode

Humanize 80% (default).

## Input

> The new cache layer, which stores repeat answers in memory and refreshes them every hour, cuts repeat database calls and keeps response times under one second during peak traffic on weekday mornings.

The input sentence has 32 words.

## Expected behavior

- The rewrite splits the input into sentences of 25 words at most.
- Each fact stays: cache layer, memory storage, hourly refresh, fewer database calls, response under one second, peak traffic, weekday mornings.
- No new fact appears.

## Pass criteria

- `python scripts/ste_check.py` (run from the skill folder in the full-cli edition) on the rewrite reports no sentence-length finding.
- All seven facts above appear in the rewrite.
