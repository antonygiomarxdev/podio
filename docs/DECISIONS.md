# Decisions

The inbox of decisions not yet absorbed into the document they govern. A decision is done when that document says it; then it moves to `decisions/YYYY-MM.md`. Owner decisions are D-n, the lead's design calls L-n. This file stays under its line cap.

| ID | Date | Decision | Goes into |
|---|---|---|---|
| D-1 | 2026-11-25 | A member entry is the file `members/<login>.json` with the GitHub login and a country code. Only LATAM countries are allowed. | docs/join/PRD.md |
| D-2 | 2026-11-25 | A pull request may add, change or delete only the entry of its author. The check runs in CI against the pull request author. | docs/join/PRD.md |
| D-3 | 2026-11-25 | The categories are: contributions of the year, current streak, longest streak, merged pull requests in other people's repositories, and stars. | docs/ranking/PRD.md |
| D-4 | 2026-11-25 | Only public data is used. Private contributions count if the user chose to show them on their public profile, because that is public data. The pull-request category searches public repositories only. | docs/PRODUCT.md |
| D-5 | 2026-11-25 | Data is recalculated daily and the page is published without committing data to the repository. | docs/tp/TP.md |
| D-6 | 2026-11-25 | The page is static, with no framework and no build step, in the identity of antonygiomarx.dev (colors, fonts, flat 1px borders). | docs/tp/TP.md |
| D-7 | 2026-11-25 | The first member is the owner. Text for users is Spanish with voseo; code, commits and issues are English. | docs/PRODUCT.md |
| D-8 | 2026-11-25 | Goals in priority order: (a) a community built live on TikTok, with people from the chat contributing pull requests; (b) a showcase for LATAM developers; (c) healthy competition that brings people back to see movement. | docs/PRODUCT.md |
| D-9 | 2026-11-25 | Anti-gaming is accepted out of v1. Streaks and yearly contributions can be inflated; the limit is documented and the community proposes better categories later. | docs/ranking/PRD.md |
| D-10 | 2026-11-25 | The main view is one LATAM ranking with a country filter. | docs/ranking/PRD.md |
| D-11 | 2026-11-25 | Commits carry no attribution lines of any kind. | docs/CROSS-CUTTING.md |
| L-1 | 2026-11-25 | The existing uncommitted code is documented by the chain, not rewritten. Known defects from HANDOFF (`member.login` against `github`; PR search without `is:public`; accents) become fix specs on the FRDs once they exist. | docs/ops/ and docs/join, docs/ranking specs |
| L-2 | 2026-11-25 | Use `/scriptorium:init`, not `adopt`: the project has no product documents, only a handoff and a README. | docs/PRODUCT.md |
| L-3 | 2026-11-25 | API rate limits at scale (more than a few hundred members) belong to the TP, not PRODUCT. | docs/tp/TP.md |
| D-12 | 2026-11-25 | The default category when the page opens is contributions of the year. | docs/ranking/PRD.md |
| D-13 | 2026-11-25 | Success targets, as a floor, within 30 days of the first public page: at least 20 members from at least 5 countries; at least 5 merged pull requests from people who are not the owner; at least 1 contributor-proposed change merged. | docs/PRODUCT.md |
| D-14 | 2026-11-25 | The 20-country list is final for v1; a community pull request may add a country. | docs/join/PRD.md |
| D-15 | 2026-11-25 | The unverified claim that existing rankings list whole countries without asking is dropped; the problem is stated as "podio asks first and counts more than commits". | docs/PRODUCT.md and README.md |
| D-16 | 2026-11-25 | Goal c (people return) has no target in v1. The success targets in D-13 are indicative, not requirements: podio is a relaxed live-stream activity and nobody is expected to contribute. | docs/PRODUCT.md |
| L-4 | 2026-11-25 | The "stars" category is the sum of stars of the member's own public repositories, forks excluded, up to 100 repositories. | docs/GLOSSARY.md, docs/ranking/PRD.md |
| D-17 | 2026-11-25 | A member's country is the one they declare. It is not verified, only checked to be on the list of accepted countries. | docs/PRODUCT.md, docs/join/PRD.md |
| D-18 | 2026-11-26 | The page is designed phone first (vertical, about 400px); desktop is the wide version of the same page. | docs/ranking/PRD.md and the future UX document of the ranking slice |
| D-19 | 2026-11-26 | The top of the ranking is a literal podium (2nd, 1st, 3rd); the list follows from 4th. | docs/ranking/PRD.md and the future UX document of the ranking slice |
| D-20 | 2026-11-26 | Each ranking row shows position, GitHub avatar, display name and login, country flag, the value of the selected category, and a compact summary of the other categories. | docs/ranking/PRD.md and the future UX document of the ranking slice |
| L-5 | 2026-11-26 | The current streak counts consecutive days back from today, or from yesterday when today has no contribution yet; a day is the day as the GitHub contribution calendar records it. | docs/ranking/PRD.md |
| L-6 | 2026-11-26 | The freshness success criterion of the ranking PRD is indicative, like D-13 and D-16, not a requirement. | docs/ranking/PRD.md |
| D-21 | 2026-11-26 | When members tie in a category, the one whose entry was accepted first goes higher, so positions are distinct. Superseded by D-28. | docs/ranking/PRD.md |
| D-22 | 2026-11-26 | A member with a value of 0 in a category is shown, at the bottom, with 0. | docs/ranking/PRD.md |
| D-23 | 2026-11-26 | The category of merged pull requests in other people's repositories counts pull requests to any public repository not owned by the member's personal account, including organizations the member belongs to. | docs/ranking/PRD.md |
| D-24 | 2026-11-26 | If a member's GitHub login changes or the account disappears, the entry stays but is not shown while the login cannot be found; the member fixes it with their own proposal. | docs/join/PRD.md |
| D-25 | 2026-11-26 | A country proposal brings the country code, its name and why; a page-change proposal brings what changes, why, and that it still works on a phone. | docs/community/PRD.md |
| D-26 | 2026-11-26 | Outsiders may write issues and pull requests in Spanish or English; code and commits stay English (refines D-7). | docs/community/PRD.md |
| D-27 | 2026-11-26 | The visual direction is proposal C "Mezcla" from `docs/propuestas-ui/index.html`: text in Instrument Sans, numbers in monospace, a compact stepped podium, dense rows with a console touch. Chosen by the owner and the community. | the future UX document of the ranking slice |
| D-28 | 2026-11-26 | When members tie in a category, the one who reached that value first goes higher; if they are still tied (for example two equal current streaks), the one whose entry was accepted first goes higher. Replaces D-21. | docs/ranking/PRD.md |
| L-7 | 2026-11-26 | The acceptance moment of an entry is kept when a member edits their own entry (for example changes country) and starts again when a member leaves and joins again; no history is kept. | docs/join/PRD.md |
| D-29 | 2026-11-26 | The country filter lists all 20 accepted countries; choosing a country with no members shows an empty state that invites people from that country to join. | docs/ranking/PRD.md |
