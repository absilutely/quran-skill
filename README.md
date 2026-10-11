# quran-skill

**The research skill no longer lives here.** Since 2026-10-11 the one home of the Quran research method is the
`quran-researcher` skill package inside the engine repo: **`quran-sot/quran-researcher/`**
([github.com/absilutely/quran-sot](https://github.com/absilutely/quran-sot), folder `quran-researcher/`).

## Why it moved
The method had drifted across several copies: this repo's `Quran Researcher.md`, a vendored copy inside quran-sot,
prompt text inside the engine's Python, quran-sot's `guidelines/`, and an in-repo Claude skill. The engine is what
actually runs the research, so the method now lives next to it, in one skill package the engine reads every prompt
from and Claude Code loads as the `quran-researcher` skill. One copy, nothing lost.

## What is left here
- `Quran Researcher.md` and `Morphology Patterns.md` — short pointers to the new files. Their old text is in this
  repo's git history (commit d2f760d). The 3 lines that existed only here (Step 5's short form) are kept word for word
  in `quran-sot/quran-researcher/evals/other/from-quran-skill-repo.md`.
- `archive/research-history/` — the past research documents, unchanged, filed by date and topic
  (index: `archive/research-history/README.md`).
