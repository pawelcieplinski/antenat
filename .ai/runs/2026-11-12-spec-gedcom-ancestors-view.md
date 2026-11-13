# Spec: GEDCOM import and direct-ancestors view

Goals:
- Specify the import of GEDCOM files (any version, as far as possible) and the direct-ancestors pedigree chart, the first slice of Antenat's first version
- Record the founder's choices made while specifying (D11–D19) in the product brief

Spec: [2026-11-12-gedcom-import-ancestors-view](../specs/2026-11-12-gedcom-import-ancestors-view.md)
Branch: docs/spec-gedcom-ancestors-view
Status: in-progress

---

## 2026-11-12
Scope: the spec `.ai/specs/2026-11-12-gedcom-import-ancestors-view.md` (Delta for `gedcom-import` and `ancestors-view`, architecture, data model, API, UI states, risks, 4-phase plan); decisions D11–D16 added to the product brief with their record in `research/decisions/`.
Decisions/gotchas: the founder chose server storage and a separate accounts spec, so this spec depends on an accounts spec that does not exist yet; the interface it needs is listed at the top. D10 (living relatives block release) is enforced by an import allowlist until Q07 closes. A first adversarial review found that "store the file as uploaded" was wrongly called the reversible option; the founder chose to strip living people's contact data (D12). Fixtures must be synthetic: the repository is public.
Next: write the accounts spec, then implement this spec phase by phase.

## 2026-11-14
Scope: the founder's corrections after reading the spec: the chart shows all generations by default with an optional limit; files are stored as uploaded with an import-contact-data option, on by default (D17, superseding D12); any GEDCOM version as far as possible, including ANSEL and ANSI encodings and `.gdz` (D18, superseding D15); the repository is to become private (D19). Brief Coverage recounted by script: 43 claims.
Decisions/gotchas: showing every generation needs the walk to expand a repeated ancestor once and reference it afterwards, or pedigree collapse grows it exponentially. The repository is still public on 2026-11-14, so the real export stays out of git until it is private. Lesson added: data removal and view limits are user options, not defaults.
Next: the founder answers Q07 when ready; write the accounts spec, then implement this spec.
