# simgate sandbox

A sandbox repo that Simgate's agent acts on. Everything here is fictional: a docs site for an
online software store. Nothing in this repo is real, and nothing it "sends" leaves GitHub.

- `site/` is deployed to GitHub Pages by `.github/workflows/pages.yml` on every push to `main`.
- `.github/workflows/announce.yml` runs after each deploy and *pretends* to email subscribers
  (it only writes an artifact). It waits `ANNOUNCE_DELAY_SECONDS` (repo variable, default 90)
  first, which is the window Simgate's verifier has to cancel it.
- `.simgate-sandbox` names this repo. Simgate refuses to touch any repo without it.

Reset daily to the `sandbox-baseline` tag.
