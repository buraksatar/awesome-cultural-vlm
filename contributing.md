# Contribution guidelines

Thank you for helping keep this list accurate. Please open a pull request that adds, updates or removes one entry at a time so it can be reviewed quickly.

## What belongs here

- Benchmarks, datasets, methods and studies whose subject is cultural or geographic robustness in vision-language models: image, video, text-to-image or text-to-video.
- Text-only cultural NLP resources belong in [awesome-cultural-nlp](https://github.com/simran-khanuja/awesome-cultural-nlp) instead.
- Multilingual resources with no cultural framing (translation, OCR, scene text) are out of scope unless the paper makes a cultural claim.

## Adding an entry

1. Search the README first to avoid duplicates, including renamed papers.
2. Use this format, in the section that fits best, keeping entries newest first:

   `- [Name](paper-url) - One factual sentence with the numbers that matter. Venue Year. [Data](url) [Code](url)`

3. The paper link should be the arXiv abstract page, or the ACL Anthology, OpenReview or proceedings page when there is no arXiv version.
4. State the venue only if it is confirmed by the arXiv comments, the proceedings, or the project page. Otherwise write `arXiv, Year.`
5. Be honest about data access: add `No public data yet.`, `Data gated.` or `Data on request.` when that is the case, and drop the marker in a later pull request once the artifact is released.
6. Keep descriptions under 25 words, plain and specific. No marketing language.
7. Run `npx awesome-lint` before opening the pull request. The lint runs again on every pull request.

## Updating an entry

Renamed papers, new venues, released data and moved repositories are all welcome updates. Mention the source of the change in the pull request description.

## Removing an entry

Open an issue or a pull request explaining why: dead links, retracted work, or a resource that has been superseded by a maintained version.
