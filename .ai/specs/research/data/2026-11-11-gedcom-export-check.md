# Data check — the founder's MyHeritage GEDCOM export, checked 2026-11-11

- Question it answers: does the founder's MyHeritage export contain, for direct ancestors, the parent links, dates and places the direct-ancestors view and the journey view need, and can the places be put on a map? (A02 in the product brief)
- Source system and owner: MyHeritage export supplied by the founder; file header: GEDCOM 5.5.1, UTF-8, exported 2026-11-08 by MyHeritage Family Tree Builder. The file is not stored in this repository.
- Filter and period: the whole file (128 people, 45 families). Direct ancestors are found by walking from the founder's own record through each person's parents (child-of family → husband and wife). The root record was chosen by the agent as the founder's record and confirmed by the founder on 2026-11-12. Events counted: birth, death, burial, christening, residence and other personal events, plus marriage events on families where the ancestor is a spouse.
- Method: a read-only script over a local copy; only aggregates are recorded here.
- Personal data present? Yes: names, dates, places, and the e-mail and postal addresses of living people. None of it is copied here; place names are summarised by count and format only, because this repository is public.

## Result

32 direct ancestors across 7 generations, with events dated 1810–2004.

| Generation (1 = parents) | Ancestors found | With any date | With any place | With birth place | With coordinates | Linked to their own parents |
|---|---|---|---|---|---|---|
| 1 | 2 of 2 | 2 | 0 | 0 | 0 | 2 |
| 2 | 4 of 4 | 2 | 2 | 0 | 0 | 4 |
| 3 | 8 of 8 | 4 | 2 | 1 | 0 | 3 |
| 4 | 6 of 16 | 3 | 2 | 2 | 0 | 2 |
| 5 | 4 of 32 | 3 | 3 | 2 | 0 | 2 |
| 6 | 4 of 64 | 4 | 2 | 2 | 0 | 2 |
| 7 | 4 of 128 | 0 | 0 | 0 | 0 | 0 |
| **Total** | **32** | **18** | **11** | **7** | **0** | — |

- Parent links: every recorded direct ancestor is reachable through parent links; the line ends where the tree ends, not because links are broken.
- Places: 13 distinct place strings across the ancestors' events. Every one is a bare locality name with no municipality, county, region or country.
- Coordinates: none. The export carries no `MAP`, `LATI` or `LONG` data for any place.
- The whole file carries e-mail addresses (2) and postal addresses (2) on residence records.

## Limits

- One tree, one export, one root person; other users' trees may differ (A01).
- Whether each bare place name identifies a single locality was not checked: no gazetteer or map lookup was run, because it would send the names to an external service. The agent's expectation that some names match several localities is unverified.
