# Notes for Claude — pack-eleven-plus-sample

- **This is the frozen sample.** 28 questions, seven per subject, copied
  verbatim (ids included) from the full bank. Don't add questions here; a
  bigger sample is a decision, not a drift.
- **Ids are the full bank's.** Never renumber. A fix to one of these questions
  is made in the full bank too, the same evening.
- **The `upgrade` block in `pack.json`** is the only place that mentions the
  full bank's listing; the engine renders it as a card on Home and in
  Settings. Keep `url` https and leave the `?ref=` to the engine.
- **Non-verbal** questions need their SVGs in `assets/` (one per prompt and
  per option, named by letter) — copy them with the question.
- `npx quizmill@latest validate .` must pass before pushing; `main` deploys.
