# Antenat — product brief

- Date: 2026-11-12 (first written 2026-11-11)
- Mode: own; Owner: Paweł Ciepliński (founder, product owner); Pass: full
- Evidence basis: the founder's first-person accounts (written chat answers, 2026-11-11 and 2026-11-12, including their own check of MyHeritage's views), a check of the founder's own GEDCOM export (2026-11-11) and the founder's confirmed decisions; no checked benchmarks or accounts from other people. Most consequential untested belief: A01.
- Coverage: 34 claims — 29 sourced (interview 9, data 4, document 16, product 0, benchmark 0), 0 synthetic, 5 assumed; 1 entry on the collection plan
- Synthetic hypotheses outside Coverage: 0
- Definition of Ready signed by: Paweł Ciepliński on 2026-11-12 for the GEDCOM import and the direct-ancestors view (D06, D09); not signed for the other-user part of the first version (D05), which waits on A01, see the [addendum](#definition-of-ready-addendum-own); ready for: research (A01) and implementation planning of the import and the direct-ancestors view
- Sources: `.ai/specs/research/interviews/2026-11-11-founder.md`, `.ai/specs/research/decisions/D01-audience.md`, `.ai/specs/research/decisions/D02-gedcom-import.md`, `.ai/specs/research/decisions/D03-family-statistics.md`, `.ai/specs/research/decisions/D04-first-version-scope.md`, `.ai/specs/research/decisions/D05-other-users-from-start.md`, `.ai/specs/research/decisions/N01-N02-non-goals.md`, `.ai/specs/research/decisions/D06-journey-view-later.md`, `.ai/specs/research/data/2026-11-11-gedcom-export-check.md`, `.ai/specs/research/decisions/D07-web-app.md`, `.ai/specs/research/decisions/D08-ai-no-cost-for-founder.md`, `.ai/specs/research/decisions/R01-consent-and-data-protection.md`, `.ai/specs/research/decisions/D09-first-version-outcome-check.md`, `.ai/specs/research/decisions/D10-living-relatives-blocks-release.md`, `.ai/specs/research/interviews/2026-11-12-founder-myheritage-check.md`

## Decision summary

The decision is the smallest first version of Antenat. The founder confirmed it on 2026-11-12 (D06, superseding D04) and chose to serve other people from the first version (D05), declining the agent's recommendation to start with the founder alone.

The founder researches their own family history, keeps the tree in MyHeritage, and finds it inconvenient to browse the tree when they want to see only direct ancestors without their siblings. They also want to answer where the family comes from and how it ended up where it lives now; this is a stated wish, without a described attempt or difficulty. See [Problems](#problems-with-evidence).

First version, for the founder and other people researching their families: user accounts, import of a GEDCOM file (D02) and a view of direct ancestors only. The founder's own export supports that view: all 32 recorded direct ancestors are reachable through parent links. The journey view moved later (D06): 11 of 32 ancestors have places, and the places are bare names without coordinates, so it needs a step to confirm each locality. Statistics (D03), documents and photos, the heatmap and the AI assistant also come later. See [Scope](#scope) and [Key flows](#key-flows).

What could change this: other people's needs are untested (A01). The founder checked MyHeritage: its limited view still shows relatives down to cousins, so the direct-ancestors view remains a gap for the founder (A04 held). Serving other users from the start brings a data-protection rule (R01); how it applies to living relatives who appear in an uploaded tree but do not use Antenat is open (Q07) and blocks release to other users. Antenat is a web application (D07).

Next action: implementation planning of the import and the direct-ancestors view can start; in parallel, the founder interviews other family researchers (A01), see the [Collection plan](#collection-plan). Dates open.

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
- The founder checked MyHeritage's views: a limited mode still shows relatives down to cousins; the founder also wants to hide siblings and other spouses. `[INTERVIEW]` interviews/2026-11-12-founder-myheritage-check.md
- The founder wants to know where the family comes from and how it ended up where it lives now. This was given as the question the proposed map, heatmap, timeline or AI should answer; no attempt to answer it, difficulty or current method was described. `[INTERVIEW]` interviews/2026-11-11-founder.md
- The founder searches records across several archive sites (szukajwarchiwach.gov.pl, genealogiawarchiwach.pl, FamilySearch, Geneteka); no difficulty with that search was described. `[INTERVIEW]` interviews/2026-11-11-founder.md
- That other family researchers have the same two problems is a hypothesis (A01).

## Product and how it stands out

- What it is: a family history app built around an imported family tree; the first version is defined in [Scope](#scope). `[DOCUMENT]` decisions/D02-gedcom-import.md
- What makes it different: the founder says MyHeritage lacks tree filtering and the views listed in the Vision. `[INTERVIEW]` interviews/2026-11-11-founder.md That these differences matter to other researchers is untested (A01).

| reference | what it does well | where it falls short for our users | checked on | link |
|---|---|---|---|---|

No reference product was checked with a recorded link; MyHeritage is described from the founder's account, including their own check of its views (A04).

## Goals and success criteria

- Business goal: not set; the founder has not stated one beyond serving their own family and others (D01).
- User outcome: the founder, using their own imported tree, sees their direct line without siblings; following where the family lived over time comes later (D06). Derived from the founder's stated needs; no outcome for other users is stated (A01). `[INTERVIEW]` interviews/2026-11-11-founder.md
- How the outcome is checked: the founder imports their own MyHeritage export and browses all 32 recorded direct ancestors without their siblings; agent proposal, accepted by the founder. `[DOCUMENT]` decisions/D09-first-version-outcome-check.md
- Primary metric, baseline today, threshold, date: not set; no metric was discussed, and what other users need is unresearched (A01).
- What must not get worse: none identified.

## Scope

- **Now (D05, D06):** for the founder and other people researching their families — user accounts (D05); import a GEDCOM file (D02); a view of direct ancestors only, without their siblings.
- **Later:** the journey view, with a step to confirm each locality on a map (D06, A05); family statistics (D03, Q02); documents and photos; the heatmap of ancestors' places; the AI assistant that reads records and answers questions, at no running cost to the founder (D08).
- **Not doing:** see Non-goals

## Domain glossary

| Term | Meaning | Owned by | Visible to |
|---|---|---|---|
| GEDCOM | The standard file format genealogy programs use to exchange family trees; Antenat's import format (D02). | founder | users |
| Direct ancestors | A person's parents, grandparents and earlier generations in the direct line, excluding the ancestors' siblings and other spouses (spouses who are not themselves direct ancestors, such as a great-grandmother's second husband; confirmed by the founder 2026-11-12). | founder | users |
| Journey view | The places where direct ancestors lived, shown on a map and in time order; later version (D06). | founder | users |

## Key flows

- Current state: the founder keeps the tree in MyHeritage, searches archive sites for records, and finds the full tree inconvenient to browse when they want only direct ancestors. `[INTERVIEW]` interviews/2026-11-11-founder.md
- Future state (D05, D06): create an account (D05) → export the tree from their genealogy program as GEDCOM (the founder: MyHeritage) → import it into Antenat (D02) → open the direct-ancestors view.
- In the founder's export, all 32 recorded direct ancestors, across 7 generations, are reachable from the founder through parent links; the line ends where the tree ends (15 have their own parents recorded). `[DATA]` data/2026-11-11-gedcom-export-check.md
- In the founder's export, 18 of 32 direct ancestors have any date and 11 have any place; the parents have no place. `[DATA]` data/2026-11-11-gedcom-export-check.md
- In the founder's export, all 13 distinct places are bare locality names without municipality, region or country, and none has coordinates. `[DATA]` data/2026-11-11-gedcom-export-check.md
- The founder's export carries e-mail and postal addresses of living people (R01, Q07). `[DATA]` data/2026-11-11-gedcom-export-check.md

## Business rules

| Id | Rule | Applies to | Source | Status | Review by | Required path to change | Owner | Supersedes |
|---|---|---|---|---|---|---|---|---|
| R01 | Users' family-tree data is stored only with consent and in line with GDPR and Polish and EU law | family-tree data users upload, from the first version (D05) | `[DOCUMENT]` decisions/R01-consent-and-data-protection.md | active | unknown | founder approves a superseding row | Paweł Ciepliński | none |

R01's wording was proposed by the agent and confirmed by the founder; how it applies to living relatives who do not use Antenat is Q07.

## Non-goals

| Id | We are not building | Why | Owner | Status | Review by | Required path to change | Source | Supersedes |
|---|---|---|---|---|---|---|---|---|
| N01 | A replacement for the archive search sites (szukajwarchiwach.gov.pl, genealogiawarchiwach.pl, FamilySearch, Geneteka) | The founder already searches there and described no difficulty with it; agent recommendation, confirmed by the founder | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/N01-N02-non-goals.md | none |
| N02 | Two-way synchronisation with MyHeritage | Import via GEDCOM (D02) is what the founder asked for; writing back was not discussed; agent recommendation, confirmed by the founder | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/N01-N02-non-goals.md | none |

## Decisions

| Id | Date | Decision | Why | Owner | Status | Review by | Required path to change | Source | Supersedes |
|---|---|---|---|---|---|---|---|---|---|
| D01 | 2026-11-11 | Antenat is for the founder's own family and for other people researching theirs | Founder's choice; no further reason given | Paweł Ciepliński | active | when A01 has a result | founder approves a superseding row | `[DOCUMENT]` decisions/D01-audience.md | none |
| D02 | 2026-11-11 | The first version imports family trees from GEDCOM files | Founder's choice, no reason given; context: the founder's tree is in MyHeritage; alternative considered: starting from an empty tree | Paweł Ciepliński | active | reviewed 2026-11-12 after A02, unchanged | founder approves a superseding row | `[DOCUMENT]` decisions/D02-gedcom-import.md | none |
| D03 | 2026-11-11 | Antenat includes family statistics, as in MyHeritage | Founder's requirement; which statistics is open (Q02) | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/D03-family-statistics.md | none |
| D04 | 2026-11-11 | First version: GEDCOM import, direct-ancestors view, journey view; statistics, documents, photos, heatmap and AI assistant later | Agent recommendation, confirmed by the founder: the direct-ancestors view answers the problem the founder described; the journey view answers the founder's stated question; the founder listed the map and the timeline separately, the agent merged them; statistics have no described situation yet; alternatives offered: smaller, import and the direct-ancestors view only; larger, statistics now (D03) | Paweł Ciepliński | superseded | — | founder approves a superseding row | `[DOCUMENT]` decisions/D04-first-version-scope.md | none |
| D05 | 2026-11-11 | The first version serves other people researching their families from the start, with user accounts | Founder's choice, no reason given; alternative declined: the agent's recommendation to serve the founder alone first, because other users' needs are untested (A01) and their data raises Q04 | Paweł Ciepliński | active | when A01 has a result | founder approves a superseding row | `[DOCUMENT]` decisions/D05-other-users-from-start.md | none |
| D06 | 2026-11-12 | First version: user accounts, GEDCOM import, direct-ancestors view; the journey view, with a step to confirm each locality, moves later | Agent recommendation, confirmed by the founder: the export check showed few places and bare names without coordinates (A02), so the journey view needs extra work, and the goal was the smallest first version; alternative: keep the journey view and add the confirmation step now; accepted cost: the founder's where-from question is answered later | Paweł Ciepliński | active | when A01 has a result | founder approves a superseding row | `[DOCUMENT]` decisions/D06-journey-view-later.md | D04 |
| D07 | 2026-11-12 | Antenat is a web application | Founder's answer to Q01; alternatives in the question: mobile, desktop; no reason given | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/D07-web-app.md | none |
| D08 | 2026-11-12 | The AI assistant must not create running costs for the founder | Founder's answer to Q03 ("Free for founder"); whether it is also free for users was not stated; no reason given | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/D08-ai-no-cost-for-founder.md | none |
| D09 | 2026-11-12 | The first version's outcome is checked by the founder importing their own MyHeritage export and browsing all 32 recorded direct ancestors without their siblings | Agent proposal, accepted by the founder; alternative: a check the founder describes | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/D09-first-version-outcome-check.md | none |
| D10 | 2026-11-12 | How R01 applies to living relatives who do not use Antenat (Q07) blocks release to other users, not implementation planning; the design must cover it | Founder's choice; alternative: also block planning; no further reason given | Paweł Ciepliński | active | unknown | founder approves a superseding row | `[DOCUMENT]` decisions/D10-living-relatives-blocks-release.md | none |

## Riskiest assumptions

| Id | Assumption | Importance | Evidence today | If false | Smallest test | Owner | By when | Result |
|---|---|---|---|---|---|---|---|---|
| A01 | Other people researching their families also want a direct-ancestors view and an answer to where their family came from `[ASSUMPTION]` founder's belief behind D01 and D05 | high | Only the founder's own account | The first version is built for users who may not need it; D01, D05 and D06 are revisited (Q05) | Talk to people who research their own family history about the last time they worked on their tree; note what they wanted to see, how they managed, where they keep their tree and whether they can export it as GEDCOM. Shows whether the founder's needs recur; does not show willingness to switch tools | Paweł Ciepliński | unknown | accepted untested (D05) |
| A02 | The founder's MyHeritage GEDCOM export contains, for direct ancestors, the parent links, places and dates needed for the direct-ancestors and journey views, and those places can be placed on a map `[ASSUMPTION]` no material | high | Checked 2026-11-11 on the founder's export: parent links hold; places and dates are sparse, and places are bare names without coordinates (see [Key flows](#key-flows)) | The journey view needs manual place and date entry or leaves the first version; D02 and D04 are revisited | Export the tree from MyHeritage as GEDCOM; for direct ancestors, check which have parent links, places and dates, and try placing a sample of the places on a map | Paweł Ciepliński | 2026-11-11 | refuted: the places part fails; led to D06 |
| A03 | A free AI service can read the founder's scanned records well enough to be useful `[ASSUMPTION]` founder's intention ("where possible") | medium | None | The AI assistant changes form or is dropped; only affects Later | Run a few of the founder's scanned records through free AI tools and compare with the founder's own reading | Paweł Ciepliński | before the AI assistant is planned | untested |
| A04 | MyHeritage does not already offer a view of direct ancestors without siblings that meets the founder's need `[ASSUMPTION]` founder's account, unchecked | high | The founder checked on 2026-11-12: MyHeritage's limited mode still shows relatives down to cousins; the founder also wants siblings and other spouses hidden (interviews/2026-11-12-founder-myheritage-check.md) | The direct-ancestors view is not a gap for the founder; D06 is revisited | Check MyHeritage's tree and chart views on the founder's tree for an ancestors-only option; note what is missing for the founder's purpose | Paweł Ciepliński | 2026-11-12 | held |
| A05 | A bare place name in a user's tree can be matched to one locality with little effort from the user `[ASSUMPTION]` no material; the agent expects some names to match several localities, unchecked | medium | The founder's places are bare names without coordinates; no lookup was run | The confirmation step needs more work or a different design; affects only the later journey view (D06) | The founder pins the 13 places from their export on a map and notes which names were ambiguous; or a gazetteer lookup, which sends the names to an external service and needs the founder's consent | Paweł Ciepliński | before the journey view is planned | untested |

## Kill criteria

- If a later export check shows the places still cannot be put on a map without the user's help (A05), the founder decides whether the journey view keeps its confirmation step or changes form. The first check (A02: 11 of 32 ancestors with places, all bare names without coordinates) led to D06.
- If conversations with other family researchers (A01) do not show the founder's needs, the founder decides whether to narrow Antenat to a personal tool (revisit D01, D05) and reviews the first-version scope (D06, Q05).
- No dates or numeric thresholds were set; the founder decides after each result.

## Hypotheses to test

None. No simulated walkthroughs were run.

## Open questions

| Id | Question | Blocking | Who can answer | Status |
|---|---|---|---|---|
| Q01 | Will Antenat be a web, mobile or desktop app? | yes — implementation planning of the first version | founder | closed 2026-11-12: web (D07) |
| Q02 | Which family statistics, as in MyHeritage, does the founder use and want? | no — blocks only planning the statistics (D03) | founder | open; 2026-11-12: the founder wants those that give the most interesting information, which ones is still to decide |
| Q03 | Does "free" AI mean free for users, no running cost for the founder, or both? | no — blocks only planning the AI assistant | founder | closed 2026-11-12: free for the founder (D08) |
| Q04 | How are living relatives' personal data handled when other people upload their trees? | yes — blocked implementation planning and release of the first version (D05) | founder, with legal advice if needed | closed 2026-11-12 in part: principle answered (R01); how living relatives' data is handled moved to Q07 (D10) |
| Q05 | Should the result of interviews with other researchers (A01) also trigger a review of the first-version scope (D06)? | no | founder | closed 2026-11-12: yes, the founder reviews D06 when A01 has a result |
| Q06 | If meeting R01 for living relatives (Q07) needs more than fits the first version, what happens to accounts for other people (D05)? | no — becomes relevant once Q07 is answered | founder | open |
| Q07 | How does R01 apply to living relatives who appear in an uploaded tree but do not use Antenat, and how are their data handled until then? | yes — blocks release of the first version to other users (D05, R01); not implementation planning, the design must cover it (D10) | founder, with legal advice if needed | open |

## Definition of Ready addendum (own)

Problems and Target group are supported for the founder only, by the founder's own accounts; other users are a decision (D01, D05) without research behind it (A01), and accepting that risk does not make it evidence. The scope is confirmed (D05, D06), the platform is web (D07), data protection follows R01 and the outcome check is agreed (D09). The import and the direct-ancestors view address the founder's supported problem, and the export check confirmed the parent links they need, so they are ready for implementation planning; the founder's MyHeritage check found no view that meets the need (A04 held). The other-user part of the first version (D05) has no supported problem yet and waits on A01. Release to other users also waits on Q07 (D10).

## Collection plan

### Do other people researching their families share the founder's needs?

- What decision or work needs it: whether the first version meets other users' needs (A01, D01, D05)
- Who can answer it: people researching their own family history with genealogy tools or archives
- How: interviews about the last time they worked on their tree
- Owner and by when: Paweł Ciepliński; date unknown
- Template: `.ai/specs/research/templates/interview-note.md`
