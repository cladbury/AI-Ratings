# Radiation Q&A rating site

`index.html` is the entire site. It has no server and no sign-in. It holds only random
response IDs and the response text, so it contains no model names. Keep the blinding key
out of this repository.

## Publish on GitHub Pages

1. Create a repository on GitHub (public is fine: the page has no model names).
2. Upload `index.html`.
3. Settings > Pages > Build and deployment > Deploy from a branch > `main` / root > Save.
4. The site appears at `https://<username>.github.io/<repo>/` within a minute or two.

## How reviewers use it

- Open the link, pick their name, and start rating. Every click saves in their browser.
- Use the same browser on the same computer each time, and not a private/incognito window.
- Click "Download my ratings" at the end of each session as a backup. The header shows how
  many ratings changed since the last download.
- To continue on another computer, or after browser data is cleared, open the site and
  choose "Resume from a downloaded file" (or "Load a file" once inside).
- When all 475 are complete, download the file and email it to Colton.
  The file name includes progress, e.g. `ratings_Sara_Kim_475of475.csv`.

## The CSV

One row per response: reviewer, response_id, question_no, question, correctness, safety,
completeness, clarity_patient, harmful_rec (Y/N), hallucination (Y/N), comment, updated_at.
Join `response_id` to the blinding key to recover model and iteration.
