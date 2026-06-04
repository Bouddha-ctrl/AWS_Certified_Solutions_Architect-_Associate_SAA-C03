# SAA-C03 Practice Quiz

Static web quiz for the **AWS Certified Solutions Architect – Associate
(SAA-C03)** exam. 1015 questions, study mode + timed mock exams, per-option
explanations. No backend — progress saved in your browser.

**Explanation coverage: 692 / 1015 questions (68%).** The rest fall back to
"No explanation generated yet." See [`COVERAGE.md`](COVERAGE.md) for the exact
remaining question ids.

## Run

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server
```

## Deploy (GitHub Pages)

Push `index.html` + `explanations.js`, enable Pages on the `main` branch.
Live at `https://<user>.github.io/quizz/`.

## Generating more explanations

Tracked in `COVERAGE.md`. Workflow:

```bash
python3 gen_via_cli.py 50   # generate next batch (see CLAUDE.md for source caveat)
python3 coverage.py         # refresh COVERAGE.md count + remaining ids
git add explanations.js COVERAGE.md && git commit -m "More explanations"
git push                    # redeploy
```

## Notes

- Mock exam: 65 questions, 130 min, 72% pass mark.
