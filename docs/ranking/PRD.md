# Ranking PRD

Status: Approved (2026-11-26)
Approval: content tSAuHd3_jvgK; rests on ../PRODUCT.md D5xg7gIHCN91

## Summary

The page shows all members of the region in one ranking, ordered by one category at a time, with a filter by country. There are five categories, each a separate ranking over the last 12 months of public GitHub activity, and the page opens on contributions of the year. Everything is recalculated every day, and the page says when and what each category counts, including how it can be inflated. Who is a member is decided by the join slice.

Last change: 2026-11-26, country filter lists all 20 countries with an empty state (D-29, R-RANKING-8); no open questions

Part of [the product overview](../PRODUCT.md). States what, not how: name no technology.

## Why
[REQ-3](../requests/REQ-3-more-than-commits.md): more ways to stand out than commit count. [REQ-4](../requests/REQ-4-showcase-latam.md): one ranking of the whole region with a country filter. [REQ-5](../requests/REQ-5-reason-to-come-back.md): positions that change, so people return. Decisions D-3, D-4, D-9, D-10, D-12, D-18, D-19, D-20, D-22, D-23, D-28 (which replaces D-21), D-29, L-4, L-5 and L-6 in [DECISIONS.md](../DECISIONS.md) set the rules below.

## Use cases
UC-3 (see the ranking), UC-4 (filter by country), UC-5 (switch category) and UC-6 (know how fresh and how fair it is), all from the product overview.

## Requirements
- **R-RANKING-1.** A visitor sees the members ordered in one category, and each row shows position, the member's GitHub avatar, display name and login, country flag, the value of the selected category, and a compact summary of the other categories (D-20).
- **R-RANKING-2.** The page opens on the contributions of the year category (D-12).
- **R-RANKING-3.** There are exactly five categories in v1, each a separate ranking over the last 12 months (D-3): contributions of the year, current streak, longest streak, merged pull requests in other people's repositories, and stars.
- **R-RANKING-4.** Contributions of the year is the total shown on the member's public profile calendar. Current streak is the number of consecutive days with at least one contribution, counted back from today, or from yesterday when today has no contribution yet; a day is the day as the GitHub contribution calendar records it (L-5). Longest streak is the longest such run in the last 12 months.
- **R-RANKING-5.** Merged pull requests counts pull requests made by the member that were merged into any public repository not owned by the member's personal account, including organizations the member belongs to (D-4, D-23).
- **R-RANKING-6.** Stars is the sum of the stars of the member's own public repositories, forks excluded, up to 100 repositories (L-4).
- **R-RANKING-7.** Only public data is used. Private activity counts only when the member chose to show it on their public profile, and then only as the daily count GitHub shows everyone (D-4).
- **R-RANKING-8.** A visitor can limit the ranking to one country and sees positions within that country. The country filter lists all 20 accepted countries, including those with no members. Choosing a country with no members shows an empty state that invites people from that country to join (D-29). With no filter, the ranking covers the whole region in one list (D-10).
- **R-RANKING-9.** All categories are recalculated every day, and the page shows the date of the last calculation.
- **R-RANKING-10.** For each category the page says what it counts and the known ways to inflate it, including that streaks and yearly totals can be inflated with automated commits (D-9).
- **R-RANKING-11.** Everything a visitor reads is in Spanish with voseo. The page is designed phone first, vertical at about 400px wide, and the desktop page is the wide version of the same page (D-18).
- **R-RANKING-12.** The top of the ranking is a podium showing 2nd, 1st and 3rd place, and the list below it continues from 4th (D-19).
- **R-RANKING-13.** When members tie in a category, the one who reached that value first goes higher. If they are still tied, for example two equal current streaks, the one whose entry was accepted first goes higher, so every position is distinct (D-28).
- **R-RANKING-14.** A member with a value of 0 in a category is shown, at the bottom, with the value 0 (D-22).
- **R-RANKING-15.** For each member and category, the moment the member reached their current value is known, so that ties can be broken (D-28). No other ranking history is kept.

## Principles honored
Principle 3 shapes R-RANKING-5 and R-RANKING-7: only public data, public repositories only for other people's work. Principle 4 shapes R-RANKING-3: no single number decides who is good. Principle 5 shapes R-RANKING-10: where a number can be inflated, the page says so. Principle 7 shapes R-RANKING-11 (language).

## Non-goals
This slice does not combine categories into one score. It does not keep or show ranking history, or how a position changed between days. It has no accounts, no login and no editing on the page. It does not protect against inflated streaks or yearly totals in v1 (D-9). It does not count private repository data, and it does not decide who is a member: that is the join slice.

## Dependencies
The join slice decides who is a member and which country each member declares. GitHub public data is the outside source for every number.

## Success criteria
Indicatively, not as a requirement (L-6): after release, on every day, the date of the last calculation shown on the page is no more than one day old, except when GitHub data is unavailable. The first-30-days targets for members and countries are in the product overview and are indicative (D-13, D-16). Goal c has no target in v1 (D-16).

## Open questions
None.
