# pack-eleven-plus-sample — a quizmill learning pack

**11+ practice** for Years 4 to 6 — English, maths, verbal reasoning and
non-verbal reasoning — in
[quizmill](https://github.com/quizmill/quizmill) learning-pack format.
Hosted at **eleven-plus.quizmill.dev**.

This repo is a **28-question sample**: seven questions per subject, spread
across the three year groups and every question type the full bank covers
(comprehension passages, spelling, grammar, place value, fractions, ratio,
hidden words, letter codes, shape sequences, rotations, reflections …). Every
question has a worked explanation; the maths, English and verbal items link
to a concept card in the answer panel.

The **full bank** (`eleven-plus-practice-full`) has all the questions across
the same four subjects and three year groups and ships as a separate pack —
one bundle file you insert at `/packs` in the app. The app's upgrade card (on
Home, below the practice loop, and in Settings) links to it.

## Where the questions come from

Original questions written for this pack and checked one by one, following
the KS2 national curriculum strands the 11+ tests (each question's
`sourceRef` names its strand). No exam-board familiarisation papers, no
publisher practice books, no real exam items. The non-verbal questions carry
generated SVG diagrams in `assets/`.

The sample is drawn from the full bank unchanged, ids included, so the full
bank's ids are a superset of these.

## Subjects and years

| Subject | Sample | Years |
| --- | ---: | --- |
| English | 7 | 4, 5, 6 |
| Maths | 7 | 4, 5, 6 |
| Verbal Reasoning | 7 | 4, 5, 6 |
| Non-Verbal Reasoning | 7 | 4, 5 |

Use the **Year** filter to drill by year group.

## Local preview

```
npx quizmill@latest run .     # practice at localhost:3000
npx quizmill@latest build .   # static app in eleven-plus-practice-app/
```

## Deploy (Cloudflare Pages → https://eleven-plus.quizmill.dev)

`.github/workflows/deploy.yml` rebuilds this pack on the latest quizmill
engine and publishes `eleven-plus-practice-app/` to the Cloudflare Pages
project `eleven-plus-practice` on every push to `main`, on engine releases,
and on manual *Run workflow*. The first run creates the Pages project; the
custom domain `eleven-plus.quizmill.dev` is attached once in the Cloudflare
dashboard (Pages → project → Custom domains).

Required Actions secrets (same org-level ones every pack app uses):
`CLOUDFLARE_API_TOKEN`, `CLOUDFLARE_ACCOUNT_ID`.
