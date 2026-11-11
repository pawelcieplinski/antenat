# Antenat product brief

Goals:
- Establish the product context for Antenat with `om-discover` (mode `own`)
- Decide the smallest first-version scope and record it with its evidence, decisions and open questions
- Refresh the brief with the founder's GEDCOM export check (A02)

Spec: none
Branch: docs/product-brief
Status: done

---

## 2026-11-11
Scope: `.ai/specs/product-brief.md` from a three-round `om-discover` session with the founder; founder interview note, decision records D01–D05 and N01–N02, and capture templates (interview note, data request, benchmark check) under `.ai/specs/research/`.
Decisions/gotchas: the only source is the founder's own account, so problems are supported for the founder only and other users' needs stay an assumption (A01, accepted untested by D05). The founder chose to serve other users from the first version against the agent's recommendation, which makes Q04 (living relatives' personal data) and Q01 (platform) blockers for implementation planning; the brief is ready for research only. Two independent skeptic passes ran: one on the full draft and one on the content changed by D05; corrections applied, two owner questions recorded as Q05 and Q06. Polish quotes are kept verbatim with English marked as translation.
Next: the founder runs the collection plan, starting with the GEDCOM export check (A02), then `/om-discover --refresh` with the results.

## 2026-11-12
Scope: `om-discover` refresh after the founder's MyHeritage GEDCOM export check: aggregate data note `research/data/2026-11-11-gedcom-export-check.md`, new decision D06 (journey view moves later, supersedes D04), A02 refuted, new A05 (place-name matching), D02 reviewed and unchanged, Q05 closed, GEDCOM entry removed from the collection plan.
Decisions/gotchas: the repository is public, so the data note keeps only counts: no names, place names or addresses, and the `.ged` file stays outside the repository (it holds living people's e-mail and postal addresses). Places in the export are bare locality names without coordinates, which is why the journey view needs a confirmation step. A skeptic pass caught that "linked to their parents" overstated the data (15 of 32 have their own parents recorded; all 32 are reachable); corrected.
Next: the founder checks MyHeritage's ancestor views (A04) and interviews other family researchers (A01).
