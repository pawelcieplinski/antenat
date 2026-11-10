# Add the product discovery layer

Goals:
- Turn on the product layer of the agent pipeline with `om-setup-discovery-pipeline`
- Add the Discovery stage, Product owner role, Definition of Ready and protected product decisions to `SDLC.md`
- Create the research directory `om-discover` reads and writes

Spec: none
Branch: chore/discovery-pipeline
Status: done

---

## 2026-11-10
Scope: `om-setup-discovery-pipeline` run: `discovery` block in `.ai/agentic.config.json` (enabled, no domain expert, no designer), product-layer blocks in `SDLC.md` (before-intake paragraph, Product owner role, Discovery and Intake rows replaced, Definition of Ready and Product decisions sections, amending paragraph), `.ai/specs/research/.gitkeep`.
Decisions/gotchas: the config block was inserted as text after `"version": 1,` rather than through `jq`, so no existing line is reformatted. The generic delivery Designer bullet stays untouched. `AGENTS.md` has no task-routing table, so no routing row was added. Product skill coverage: all four installed.
Next: run `/om-discover` to write `.ai/specs/product-brief.md`.
