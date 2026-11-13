# Offer data removal and view limits as options, not defaults

## Context
In the GEDCOM import spec the agent recommended removing living people's contact data from stored files and showing four generations by default, with fixtures limited to synthetic data because the repository was public. The founder accepted the removal at first, then on reading the spec corrected all three: nothing is removed from an uploaded file, contact data is imported unless the user opts out, every generation is shown by default with a control to limit it, and the repository will become private.

## Lesson
For a genealogy tool the user's own data is the product: default to keeping and showing everything the user brought, and propose any removal, filter or limit as a user option with the full-fidelity choice as its default. A legal or privacy concern goes on the record as an open question or a risk for the owner, not into a default that silently drops data. A repository's visibility is checked, not assumed from a plan.

## How to apply
When a spec for Antenat touches import, storage or display of family-tree data, write the full-fidelity behaviour as the default and present reductions as options; name the privacy risk next to Q07 instead. Before relaxing a rule that exists because the repository is public, check `gh repo view --json visibility`.
