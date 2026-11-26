# Community PRD

Status: Approved (2026-11-26)
Approval: content cb6SxvBfjQ6z; rests on ../PRODUCT.md D5xg7gIHCN91

## Summary

Anyone can propose a new category, a new country or a change to the page, and a written process in Spanish tells them what the proposal needs. Only the maintainer accepts a proposal. Contributing is optional: podio is a relaxed live-stream activity and nobody is expected to propose anything. Joining the ranking is the join slice, and showing it is the ranking slice.

Last change: 2026-11-26, Why cites D-25 and D-26 and no longer says the guide covers categories only

Part of [the product overview](../PRODUCT.md). States what, not how: name no technology.

## Why
[REQ-1](../requests/REQ-1-build-it-live.md): the owner wants podio built live with the chat, with people from the stream contributing. A contribution guide exists today, with no outside use yet. Decisions D-8, D-13, D-14, D-16, D-25 and D-26 in [DECISIONS.md](../DECISIONS.md) set the rules below.

## Use cases
UC-7 (propose a category or change), from the product overview.

## Requirements
- **R-COMMUNITY-1.** A person who is not the maintainer can propose a new category, a new country, or a change to the page.
- **R-COMMUNITY-2.** A written process in Spanish tells the person what each kind of proposal must contain, before they make it.
- **R-COMMUNITY-3.** A category proposal states what is measured and how it is calculated from public GitHub data, why it is fair to participants of different sizes, and gives an example with at least one real member.
- **R-COMMUNITY-4.** A category proposal that needs private data is not accepted (principle 3).
- **R-COMMUNITY-5.** A proposal becomes part of podio only when the maintainer accepts it. The maintainer decides the categories.
- **R-COMMUNITY-6.** A new country can be added by a community proposal (D-14). The country list stays final for v1 until such a proposal is accepted.
- **R-COMMUNITY-7.** The process is reachable from the project's front page.
- **R-COMMUNITY-8.** A country proposal brings the country code, its name and why. A page-change proposal brings what changes, why, and that it still works on a phone (D-25).
- **R-COMMUNITY-9.** Outsiders may write issues and pull requests in Spanish or English. Code and commits stay English (D-26, refines D-7).

## Principles honored
Principle 6 shapes R-COMMUNITY-1 and R-COMMUNITY-2: proposals are open to anyone and the process is written down. Principle 3 shapes R-COMMUNITY-4. Principle 7 shapes R-COMMUNITY-2: what a person reads is Spanish.

## Non-goals
This slice does not require anyone to contribute (D-16). It does not give rewards, badges or titles to contributors. It does not decide who is a member (join slice) or how a category is shown and ordered (ranking slice). It has no accounts, forum or chat of its own, and it does not moderate the stream chat.

## Dependencies
The ranking slice carries every accepted category. The join slice holds the country list that a country proposal changes.

## Success criteria
Within 30 days of the first public page, indicatively (D-13, D-16): at least 5 merged pull requests from people who are not the owner, and at least 1 contributor-proposed change merged. Goal c has no target in v1 (D-16).

## Open questions
None.
