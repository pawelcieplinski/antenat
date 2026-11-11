# Antenat — product brief

- Date: 2026-11-11
- Mode: own; Owner: Paweł Ciepliński (founder, product owner); Pass: full
- Evidence basis: one first-person account from the founder (written chat answers, 2026-11-11) and the founder's confirmed decisions; no data, checked benchmarks or accounts from other people. Most consequential untested beliefs: A01, A02.
- Coverage: 21 claims — 17 sourced (interview 8, data 0, document 9, product 0, benchmark 0), 0 synthetic, 4 assumed; 3 entries on the collection plan
- Synthetic hypotheses outside Coverage: 0
- Definition of Ready signed by: scope confirmed by Paweł Ciepliński on 2026-11-11 (D04, D05); not signed for implementation, see the [addendum](#definition-of-ready-addendum-own); ready for: research (A01, A02, A04)
- Sources: `.ai/specs/research/interviews/2026-11-11-founder.md`, `.ai/specs/research/decisions/D01-audience.md`, `.ai/specs/research/decisions/D02-gedcom-import.md`, `.ai/specs/research/decisions/D03-family-statistics.md`, `.ai/specs/research/decisions/D04-first-version-scope.md`, `.ai/specs/research/decisions/D05-other-users-from-start.md`, `.ai/specs/research/decisions/N01-N02-non-goals.md`

## Decision summary

The decision was the smallest first version of Antenat. The founder confirmed the scope below on 2026-11-11 (D04) and chose to serve other people from the first version (D05), declining the agent's recommendation to start with the founder alone.

The founder researches their own family history, keeps the tree in MyHeritage, and finds it inconvenient to browse the tree when they want to see only direct ancestors without their siblings. They also want to answer where the family comes from and how it ended up where it lives now; this is a stated wish, without a described attempt or difficulty. See [Problems](#problems-with-evidence).

First version, for the founder and other people researching their families: accounts for users, import of a GEDCOM file (D02), a view of direct ancestors only, and the places those ancestors lived on a map and in time order. Statistics (D03), documents and photos, the heatmap and the AI assistant come later. See [Scope](#scope).

What could change this: other people's needs are untested (A01); nobody has checked whether the founder's GEDCOM export holds the places and dates the journey view needs (A02) or whether MyHeritage already has an ancestors-only view (A04). Serving other users from the start makes the handling of living relatives' data (Q04) a blocker, alongside the platform choice (Q01).

Next action: the founder runs the three checks in the [Collection plan](#collection-plan), starting with the GEDCOM export (A02). Dates open.

## Vision

A tool for following a family's history through its tree, documents and photos, the places ancestors lived on a map and a timeline, and, where possible, a free AI assistant that reads records and answers questions about the family. This is the founder's intended direction, not a demonstrated benefit. `[INTERVIEW]` interviews/2026-11-11-founder.md

## Target group and stakeholders

- Customer (pays): not decided; no payment model was discussed.
- User (uses): the founder, researching their own family with MyHeritage and online archives. `[INTERVIEW]` interviews/2026-11-11-founder.md
- User (uses): other people researching their own families, chosen as a target by the founder (D01) and served from the first version (D05); their situation is not researched (A01). `[DOCUMENT]` decisions/D01-audience.md
- Stakeholders (decides, blocks, operates): the founder decides and builds; no other stakeholders were named.
- Decider for scope decisions: Paweł Ciepliński (founder)

## Problems, with evidence

- The founder wants to limit the tree to direct ancestors without the ancestors' siblings and finds browsing it otherwise inconvenient in MyHeritage. Only this one account supports it; frequency and cost were not described. `[INTERVIEW]` interviews/2026-11-11-founder.md
- The founder wants to know where the family comes from and how it ended up where it lives now. This was given as the question the proposed map, heatmap, timeline or AI should answer; no attempt to answer it, difficulty or current method was described. `[INTERVIEW]` interviews/2026-11-11-founder.md
- The founder searches records across several archive sites (szukajwarchiwach.gov.pl, genealogiawarchiwach.pl, FamilySearch, Geneteka); no difficulty with that search was described. `[INTERVIEW]` interviews/2026-11-11-founder.md
- That other family researchers have the same two problems is a hypothesis (A01).

## Product and how it stands out

- What it is: a family history app built around an imported family tree; the first version is defined in [Scope](#scope). `[DOCUMENT]` decisions/D02-gedcom-import.md
- What makes it different: the founder says MyHeritage lacks tree filtering and the views listed in the Vision. `[INTERVIEW]` interviews/2026-11-11-founder.md That these differences matter to other researchers is untested (A01).

| reference | what it does well | where it falls short for our users | checked on | link |
|---|---|---|---|---|

No reference product was checked; MyHeritage is described only from the founder's account (A04).

## Goals and success criteria

- Business goal: not set; the founder has not stated one beyond serving their own family and others (D01).
- User outcome: the founder, using their own imported tree, sees their direct line without siblings and can follow where the family lived over time. Derived from the founder's stated needs; no outcome for other users is stated (A01). `[INTERVIEW]` interviews/2026-11-11-founder.md
- Primary metric, baseline today, threshold, date: not set; no metric was discussed, and what other users need is unresearched (A01).
- What must not get worse: none identified.

## Scope

- **Now (D04, D05):** for the founder and other people researching their families — user accounts (D05); import a GEDCOM file (D02); a view of direct ancestors only, without their siblings; a journey view showing the places direct ancestors lived on a map and in time order.
- **Later:** family statistics (D03, D04); documents and photos; the heatmap of ancestors' places; the AI assistant that reads records and answers questions (Q03).
- **Not doing:** see Non-goals

## Domain glossary

| Term | Meaning | Owned by | Visible to |
|---|---|---|---|
| GEDCOM | The standard file format genealogy programs use to exchange family trees; Antenat's import format (D02). | founder | users |
| Direct ancestors | A person's parents, grandparents and earlier generations in the direct line, excluding the ancestors' siblings. | founder | users |
| Journey view | The places where direct ancestors lived, shown on a map and in time order (D04). | founder | users |

## Key flows

- Current state: the founder keeps the tree in MyHeritage, searches archive sites for records, and finds the full tree inconvenient to browse when they want only direct ancestors. `[INTERVIEW]` interviews/2026-11-11-founder.md
- Future state (D04, D05): create an account (D05) → export the tree from their genealogy program as GEDCOM (the founder: MyHeritage, A02) → import it into Antenat (D02) → open the direct-ancestors view → open the journey view to see where the line lived over time.

## Business rules

| Id | Rule | Applies to | Source | Status | Review by | Required path to change | Owner | Supersedes |
|---|---|---|---|---|---|---|---|---|

None agreed yet; rules for users' data wait on Q04.

## Non-goals

| Id | We are not building | Why | Owner | Status | Review by | Required path to change | Source | Supersedes |
|---|---|---|---|---|---|---|---|---|
| N01 | A replacement for the archive search sites (szukajwarchiwach.gov.pl, genealogiawarchiwach.pl, FamilySearch, Geneteka) | The founder already searches there and described no difficulty with it; agent recommendation, confirmed by the founder | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/N01-N02-non-goals.md | none |
| N02 | Two-way synchronisation with MyHeritage | Import via GEDCOM (D02) is what the founder asked for; writing back was not discussed; agent recommendation, confirmed by the founder | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/N01-N02-non-goals.md | none |

## Decisions

| Id | Date | Decision | Why | Owner | Status | Review by | Required path to change | Source | Supersedes |
|---|---|---|---|---|---|---|---|---|---|
| D01 | 2026-11-11 | Antenat is for the founder's own family and for other people researching theirs | Founder's choice; no further reason given | Paweł Ciepliński | active | when A01 has a result | founder approves a superseding row | `[DOCUMENT]` decisions/D01-audience.md | none |
| D02 | 2026-11-11 | The first version imports family trees from GEDCOM files | Founder's choice, no reason given; context: the founder's tree is in MyHeritage; alternative considered: starting from an empty tree | Paweł Ciepliński | active | when A02 has a result | founder approves a superseding row | `[DOCUMENT]` decisions/D02-gedcom-import.md | none |
| D03 | 2026-11-11 | Antenat includes family statistics, as in MyHeritage | Founder's requirement; which statistics is open (Q02) | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/D03-family-statistics.md | none |
| D04 | 2026-11-11 | First version: GEDCOM import, direct-ancestors view, journey view; statistics, documents, photos, heatmap and AI assistant later | Agent recommendation, confirmed by the founder: the direct-ancestors view answers the problem the founder described; the journey view answers the founder's stated question; the founder listed the map and the timeline separately, the agent merged them; statistics have no described situation yet; alternatives offered: smaller, import and the direct-ancestors view only; larger, statistics now (D03) | Paweł Ciepliński | active | when A02 and A04 have results | founder approves a superseding row | `[DOCUMENT]` decisions/D04-first-version-scope.md | none |
| D05 | 2026-11-11 | The first version serves other people researching their families from the start, with user accounts | Founder's choice, no reason given; alternative declined: the agent's recommendation to serve the founder alone first, because other users' needs are untested (A01) and their data raises Q04 | Paweł Ciepliński | active | when A01 has a result | founder approves a superseding row | `[DOCUMENT]` decisions/D05-other-users-from-start.md | none |

## Riskiest assumptions

| Id | Assumption | Importance | Evidence today | If false | Smallest test | Owner | By when | Result |
|---|---|---|---|---|---|---|---|---|
| A01 | Other people researching their families also want a direct-ancestors view and an answer to where their family came from `[ASSUMPTION]` founder's belief behind D01 and D05 | high | Only the founder's own account | The first version is built for users who may not need it; D01 and D05 are revisited; whether D04 is too is open (Q05) | Talk to people who research their own family history about the last time they worked on their tree; note what they wanted to see, how they managed, where they keep their tree and whether they can export it as GEDCOM. Shows whether the founder's needs recur; does not show willingness to switch tools | Paweł Ciepliński | unknown | accepted untested (D05) |
| A02 | The founder's MyHeritage GEDCOM export contains, for direct ancestors, the parent links, places and dates needed for the direct-ancestors and journey views, and those places can be placed on a map `[ASSUMPTION]` no material | high | None; the export has not been made | The journey view needs manual place and date entry or leaves the first version; D02 and D04 are revisited | Export the tree from MyHeritage as GEDCOM; for direct ancestors, check which have parent links, places and dates, and try placing a sample of the places on a map. Shows what the first version can draw from real data | Paweł Ciepliński | unknown | untested |
| A03 | A free AI service can read the founder's scanned records well enough to be useful `[ASSUMPTION]` founder's intention ("where possible") | medium | None | The AI assistant changes form or is dropped; only affects Later | Run a few of the founder's scanned records through free AI tools and compare with the founder's own reading | Paweł Ciepliński | before the AI assistant is planned | untested |
| A04 | MyHeritage does not already offer a view of direct ancestors without siblings that meets the founder's need `[ASSUMPTION]` founder's account, unchecked | high | The founder says MyHeritage lacks tree filtering; no check of its views was made | The direct-ancestors view is not a gap for the founder; D04 is revisited | Check MyHeritage's tree and chart views on the founder's tree for an ancestors-only option; note what is missing for the founder's purpose | Paweł Ciepliński | unknown | untested |

## Kill criteria

- If the GEDCOM check (A02) shows the export lacks the places or dates needed to draw the journey, the founder decides whether to add manual entry to the first version or drop the journey view from it.
- If conversations with other family researchers (A01) do not show the founder's needs, the founder decides whether to narrow Antenat to a personal tool (revisit D01, D05); whether the first-version scope changes too is open (Q05).
- No dates or numeric thresholds were set; the founder decides after each result.

## Hypotheses to test

None. No simulated walkthroughs were run.

## Open questions

| Id | Question | Blocking | Who can answer | Status |
|---|---|---|---|---|
| Q01 | Will Antenat be a web, mobile or desktop app? | yes — implementation planning of the first version | founder | open |
| Q02 | Which family statistics, as in MyHeritage, does the founder use and want? | no — blocks only planning the statistics (D03) | founder | open |
| Q03 | Does "free" AI mean free for users, no running cost for the founder, or both? | no — blocks only planning the AI assistant | founder | open |
| Q04 | How are living relatives' personal data handled when other people upload their trees? | yes — blocks implementation planning and release of the first version, which serves other users (D05) | founder, with legal advice if needed | open |
| Q05 | Should the result of interviews with other researchers (A01) also trigger a review of the first-version scope (D04)? | no — affects only when D04 is reviewed | founder | open |
| Q06 | If handling living relatives' data (Q04) needs more than fits the first version, what happens to accounts for other people (D05)? | no — becomes relevant once Q04 is answered | founder | open |

## Definition of Ready addendum (own)

Problems and Target group are supported for the founder only, by one first-person account; other users are a decision (D01, D05) without research behind it (A01), and accepting that risk does not make it evidence. The scope is confirmed (D04, D05); no assumption is tested. Ready for research (A01, A02, A04). Implementation planning waits on Q01 and Q04, and the first version's value to other users remains unsupported until A01 has a result.

## Collection plan

### What does the founder's MyHeritage GEDCOM export contain for direct ancestors?

- What decision or work needs it: whether the journey view stays in the first version (A02, D04)
- Who can answer it: the founder, from their own MyHeritage account
- How: export the tree as GEDCOM; for direct ancestors, record which have parent links, places and dates, and how many sample places could be put on a map
- Owner and by when: Paweł Ciepliński; date unknown
- Template: `.ai/specs/research/templates/data-request.md`

### Do other people researching their families share the founder's needs?

- What decision or work needs it: whether the first version meets other users' needs (A01, D01, D05)
- Who can answer it: people researching their own family history with genealogy tools or archives
- How: interviews about the last time they worked on their tree
- Owner and by when: Paweł Ciepliński; date unknown
- Template: `.ai/specs/research/templates/interview-note.md`

### Does MyHeritage already offer a direct-ancestors view?

- What decision or work needs it: whether the direct-ancestors view belongs in the first version (A04, D04)
- Who can answer it: the founder, on their own MyHeritage tree
- How: check MyHeritage's tree and chart views for an ancestors-only option and record what is missing for the founder's purpose
- Owner and by when: Paweł Ciepliński; date unknown
- Template: `.ai/specs/research/templates/benchmark-check.md`
