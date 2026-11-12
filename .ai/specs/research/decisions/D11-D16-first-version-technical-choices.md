# D11–D16 — Choices for the first version made while specifying the import and the ancestors view

- Date, owner: 2026-11-12, Paweł Ciepliński (founder, product owner)
- Context and the options weighed: open questions of the spec `.ai/specs/2026-11-12-gedcom-import-ancestors-view.md`, answered by the founder in the chat. Verbatim answers where given in words: "2 b oraz integracja z Google Drive i podobnymi. 3 b." and "Pliki gedcom zawsze na serwerze, ale możliwa synchronizacja przez chmurę. Chmura jako darmowa opcją przechowywania zdjęć i dokumentów – synchronizacja z serwisem, czy to możliwe?" (quotes; translation: "2 b, plus integration with Google Drive and similar. 3 b." and "GEDCOM files always on the server, but sync through the cloud possible. The cloud as a free option for storing photos and documents — syncing with the service, is that possible?"). The other answers were option choices.
- Decisions and why (no further reasons were given unless stated):
  - D11: user accounts get their own spec and ship before the import and the ancestors view. Options: accounts first; a founder-only mode first; sign-in inside the import spec.
  - D12: trees are stored in a server database, and GEDCOM files are always kept on the server, with contact data (e-mail, phone, postal addresses) of presumed-living and unknown-status people removed. Options: browser-only storage; storing the file as uploaded. The removal was the agent's recommendation, accepted by the founder, because nothing uses that data and R01 implies data minimisation.
  - D13: the web application is built with Next.js. Options: TypeScript + React single-page app; Python backend with a separate frontend.
  - D14: the direct-ancestors view is a pedigree chart, one column per generation. Options: fan chart; list by generation.
  - D15: the import supports GEDCOM 5.5.1 and the newest version, GEDCOM 7. Option: 5.5.1 only.
  - D16: integration with Google Drive and similar services is its own spec: syncing GEDCOM files through the cloud. Using cloud drives as free storage for photos and documents is the founder's intention, whose feasibility that spec checks.
- Consequences, and what would make us revisit them: D11 makes the import depend on the accounts spec. D12 makes stored files differ from uploads. D16's photo and document storage is a later-scope proposal until its feasibility is checked.
- Status: active (D11–D16)
