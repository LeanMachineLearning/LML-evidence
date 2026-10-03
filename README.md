# Evidence about LeanMachineLearning

Reviews, problem reports, questions and tests of the declarations of
[LeanMachineLearning](https://github.com/LeanMachineLearning/LML), kept in `evidence/` as
[S3 records](https://github.com/LeanTrustBuilders/specs/blob/main/S3-evidence.md): one per line, in
git, never edited. They are written from the issues of this repository.

## Adding to it

Open an issue with one of the [forms](https://github.com/LeanMachineLearning/LML-evidence/issues/new/choose):
review a declaration, report a problem, ask a question, propose a test, list a test, or name a result.
A bot turns it into a record, keyed by the declaration's hashes at the commit of LML you name (the
latest if none), and replies on the issue. A record says which version of the declaration it was
about: when the declaration, or something it rests on, changes, pages show the record as made on an
earlier version.

Comments on the issue are replies. Commands in a comment change a record's state: `/withdraw`,
`/fixed <commit>`, `/intended`, `/invalid`, `/answered`, `/met <declaration>`, `/reopen`. Records are
never anonymous: each names the GitHub account it came from, and an AI agent's are labelled as such.
An agent can also submit from a terminal with
[`evidence-store submit`](https://github.com/LeanTrustBuilders/evidence-store#who-wrote-it).

## Where the records show

- [LeanMachineLearning's site](https://leanmachinelearning.org/LML/exposition/), built by LML's CI
  with [referee-site](https://github.com/LeanTrustBuilders/referee-site), shows them on each
  declaration as of its latest build.
- This store imports the
  [Mathlib probability store](https://github.com/LeanTrustBuilders/mathlib-probability-evidence),
  so the site also shows reviews of the Mathlib declarations LML rests on, marked with that store.

## How it is set up

- `evidence/store.json`: the store's name (LeanMachineLearning), the library, where its datasets
  are (the releases `dataset-<commit12>` of LML, which its CI publishes), and the stores it imports.
- `.github/workflows/evidence-intake.yml` and `evidence-check.yml`: intake, and the check of every
  change to the store, by [evidence-store](https://github.com/LeanTrustBuilders/evidence-store)
  v0.7.2.
- The first records were made in
  [LeanTrustBuilders/site-pilot](https://github.com/LeanTrustBuilders/site-pilot), where this store
  began: their links point to the issues there.
