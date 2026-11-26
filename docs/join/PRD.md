# Join PRD

Status: Approved (2026-11-26)
Approval: content nMBOrY3wslkQ; rests on ../PRODUCT.md D5xg7gIHCN91

## Summary

A developer joins the ranking by proposing an entry for themselves, and leaves by proposing to remove it. Nobody can add, change or remove anyone else's entry. The only country check is that the country is on the accepted list: a member's country is the one they declare. A rejected proposal tells its author why, in Spanish. Showing members and counting their activity belong to the ranking slice.

Last change: 2026-11-26, R-JOIN-9 says when the acceptance moment is kept or restarted (L-7); Why cites D-24 and D-28

Part of [the product overview](../PRODUCT.md). States what, not how: name no technology.

## Why
[REQ-2](../requests/REQ-2-only-who-sign-up.md): the owner wants nobody listed unless they asked, and nobody able to act for someone else. Decisions D-1, D-2, D-14, D-17, D-24, D-28 (which replaces D-21) and L-7 in [DECISIONS.md](../DECISIONS.md) set the rules below.

## Use cases
UC-1 (join the ranking) and UC-2 (leave the ranking), both from the product overview.

## Requirements
- **R-JOIN-1.** A developer can join by proposing an entry for themselves, made of their GitHub login and one country. After the proposal is accepted, they appear in the ranking after the next daily recalculation.
- **R-JOIN-2.** A proposal is rejected when its country is not on the list of accepted countries. The list has 20 countries and a community proposal may add one (D-14).
- **R-JOIN-3.** The country of an entry is the one the member declares. The slice does not verify it (D-17).
- **R-JOIN-4.** A proposal can add, change or remove only the entry of the person who makes it. A proposal that touches the entry of anyone else is rejected before it can be accepted (D-2).
- **R-JOIN-5.** A member can leave by proposing to remove their own entry. They disappear from the ranking after the next daily recalculation.
- **R-JOIN-6.** A person has at most one entry, identified by their GitHub login.
- **R-JOIN-7.** A rejected proposal tells its author in Spanish which rule it broke and what to change.
- **R-JOIN-8.** If a member's GitHub login changes or the account disappears, the entry stays but is not shown in the ranking while the login cannot be found. The member fixes it with their own proposal (D-24).
- **R-JOIN-9.** The moment each entry was accepted is kept, so the order of acceptance can be known (D-28). It is kept when a member edits their own entry, for example changes country, and starts again when a member leaves and joins again; no history is kept (L-7).

## Principles honored
Principle 1 shapes R-JOIN-1 and R-JOIN-5: a person appears only through their own proposal, and leaves the same way. Principle 2 shapes R-JOIN-4 and R-JOIN-6: no one acts for someone else, and a person has one entry that only they can change. Principle 7 shapes R-JOIN-7: what a person reads is Spanish.

## Non-goals
This slice does not verify where a person lives (D-17). It does not rank or count anything: that is the ranking slice. It has no accounts, no login and no editing on the page. It does not send notifications, keep a history of who joined and left, or list teams or organizations. A maintainer does not add people on their behalf.

## Dependencies
The ranking slice shows a joined member and recalculates daily. This slice defines who is a member; it does not wait for the ranking slice to be written.

## Success criteria
Within 30 days of the first public page, indicatively (D-13, D-16): at least 20 members from at least 5 countries. At every moment, zero entries that were added or changed by someone other than the person they name, checked on each accepted proposal.

## Open questions
None.
