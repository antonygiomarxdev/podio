# Cross-cutting concerns

Every FRD answers each row: applies (how) or "n/a: <reason>".

| ID | Concern | Rule | Check |
|---|---|---|---|
| CC-1 | Security | A pull request may add, change or delete only its author's own entry (D-2). | `node --test` runs `scripts/validate.test.mjs` |
| CC-2 | Privacy | Only public data is used; private activity counts only as the daily count a user chose to show on their public profile (D-4). | none yet: the first spec that reads GitHub data adds one |
| CC-3 | Accessibility | The page works on a phone screen (PRODUCT section 6). | none yet: the first spec for the page adds one |
| CC-4 | Languages | Everything a visitor reads is Spanish with voseo; code, commits and issues are English (D-7). | none yet: the first spec for the page adds one |
| CC-5 | Performance budget | n/a for v1: no budget is decided; API rate limits at scale belong to the TP (L-3). | n/a |
