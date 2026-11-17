# Humanizer 80 v1.0.0

By Vasyl & Mia

Humanizer 80 rewrites AI-sounding English into clear, human prose. It uses the "80% of the way to ASD-STE100" method that Andrej Karpathy shared on 2 October 2026. The skill keeps what the text says. It invents nothing.

## Two passes

- **Pass 1** removes 26 AI tells: not-X-but-Y, one-line closers, forced triads, dashes everywhere, stock AI words, inflated claims, chatbot residue. The full catalog lives in `references/ai-tells.md`. Ukrainian tells (U1 to U9) live in `references/uk-tells.md`.
- **Pass 2** rebuilds sentences with the structure of Simplified Technical English: one idea per sentence, short sentences, active voice, simple tenses, plain words. The rules live in `references/ste80-rules.md`. Strict mode lives in `references/strict-mode.md`.

## Modes

- **Humanize 80%** (default): Pass 1 fully, Pass 2 at 80%. The writer's voice stays.
- **Light**: Pass 1, plus only the worst sentences from Pass 2.
- **Strict**: Pass 1, Pass 2 at 100%. For procedures, safety notes, and maintenance text.
- **Warm**: chats, personal letters, and SMS. Warm and human, no STE.
- **Agent/Skill Spec**: system prompts, `SKILL.md` files, tool descriptions, and inter-agent protocols.

## Install

- **Google Gemini**: open the Skills editor, create a skill named `humanizer-80`, paste the `SKILL.md` text (without the YAML frontmatter) into the Instructions field, and upload the six files from `references/`.
- **Meta Muse / CLI**: copy this folder into your agent's skills directory. The checker needs Python 3.8 or later, and no extra packages.

## Checker

`scripts/ste_check.py` is a small heuristic linter. It flags Pass 1 tells, Ukrainian tells, and the measurable Pass 2 rules. It is not an AI detector and not a compliance check. Use it for all counts. Never count words in the answer.

```bash
python scripts/ste_check.py draft.md              # Humanize / 80%
python scripts/ste_check.py --strict runbook.md   # Strict STE
```

## Tests

`evals/` holds six test cases in the T-battery style:

- **T1** word cap: a 32-word sentence splits into sentences of 25 words at most.
- **T2** identifiers: backticked identifiers, URLs, versions, and "40+" stay exact.
- **T3** README rewrite: hype adjectives go, facts stay.
- **T4** kept-as-is: clean text gets no forced edits.
- **T5** creative refusal: a poem gets a short refusal, no rewrite.
- **T6** client-letter refusal: a client email gets a short refusal, no rewrite, no invented price.

Tested 17 November 2026: 6 of 6 pass in Google Gemini and 6 of 6 pass in Meta Muse.

## Sources and credits

- Andrej Karpathy, post of 2 October 2026: the "80% of the way to ASD-STE100" idea.
- `ste80-humanizer` v4.0.0 by Dodaios (MIT): the two-pass design, the tell catalog, and the checker this skill adapts.
- `blader/humanizer` by Siqi Chen (MIT): the original catalog of 26 AI writing patterns. See `THIRD_PARTY_NOTICES.md`.
- Wikipedia, "Signs of AI writing": the source of the tell list.
- ASD-STE100 Issue 9 (2025): the standard behind the structure rules. Rules here are paraphrases, not the official text.

## Disclaimer

Simplified Technical English and ASD-STE100 are a copyright and European Union Trade Mark (No. 017966390) of ASD, Brussels, Belgium. This skill is an independent clarity tool. It is not endorsed, certified, or affiliated with ASD or ASD STEMG. It gives "STE style", never "STE-compliant". The goal is readable text, not beating AI detectors.

## License

MIT. See `LICENSE`. Third-party notices live in `THIRD_PARTY_NOTICES.md`.
