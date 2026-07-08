# Ever Works — Missions catalog

This repository hosts **reusable Mission templates** for the
[Ever Works](https://ever.works) platform. A Mission template encodes
"here is a long-running, repeatable goal — its prompt, its cadence,
its guardrails, and the kind of Ideas it should generate". When a user
picks one in the Workshop, the platform creates a real `Mission` row
pre-filled with that template.

> Status: bootstrap. Three sample Mission templates ship here; the
> seed loader on the platform side (tracked in ADR-010) will read this
> repo's `manifest.json` once it lands. Until then, the platform reads
> `Mission.missionTemplateRepo` and resolves to entries here by slug.

## What lives here

```
schema/
  mission-template.schema.json    # JSON Schema for the mission.yml frontmatter
templates/
  saas-directory-launch/
    mission.yml                   # type, schedule, autoBuildWorks, guardrails
    BRIEF.md                      # the prompt the user can edit
    README.md                     # human-readable description
  content-engine/
  weekly-trend-digest/
manifest.json                     # auto-built index the platform reads first
```

## What a Mission is

A Mission is a long-running goal owned by an Agent (or a team of
Agents). It has:

- A **type** — `ONE_SHOT` (run once and complete) or `SCHEDULED` (tick
  on a cron and keep producing Ideas / Tasks / Works).
- A **prompt** — the human-language brief describing what success
  looks like.
- A **cadence** — for `SCHEDULED` Missions: how often to tick.
- **Guardrails** — caps on outstanding Ideas, on autonomous Work
  creation, and on the cost / time budget per tick.

When a Mission ticks, it produces:

- Zero or more **Ideas** (WorkProposals) — candidate things to build.
- Zero or more **Tasks** — concrete steps for itself or other Agents.
- Optionally, when `autoBuildWorks` is on and an Idea passes the
  guardrails, a new **Work**.

Mission templates in this repo describe the *defaults* for one of
those goal patterns. The user can tweak any field before activating.

## Format — one Mission template per folder

Each template is a folder under `templates/<slug>/` containing three
files:

| File | Purpose |
|---|---|
| `mission.yml` | YAML — the platform-mappable fields (type, schedule, guardrails, autoBuildWorks). Validated against [`schema/mission-template.schema.json`](schema/mission-template.schema.json). |
| `BRIEF.md`    | The prompt body the user reviews + edits in the wizard before activating. Becomes the Mission's `description`. |
| `README.md`   | Human-readable overview shown on the template card — when to pick this, when not to, expected output. |

## How the platform consumes this repo

1. At build time (or via a scheduled refresh), the platform fetches
   `manifest.json` from this repo's `main` branch.
2. For each entry it reads `mission.yml` + `BRIEF.md` and exposes the
   template on the Mission-creation surface (today: from the "Create
   from template" picker; soon: from the same prompt-driven flow as
   Ideas / Works).
3. When a user picks a template the wizard pre-fills type, schedule,
   `autoBuildWorks`, the guardrail overrides, and the BRIEF as
   `description`. The user can edit anything before activating.
4. The resulting `Mission` row stores `missionTemplateRepo =
   "ever-works/missions/<slug>"` so we can later trace which template
   spawned which Mission.

The platform's `Mission` entity is defined in
`packages/agent/src/entities/mission.entity.ts`.

## Adding a template

1. Pick a slug (lowercase, kebab-case, ≤ 60 chars). Use a verb-noun
   phrase that describes the *outcome* (`weekly-trend-digest`,
   `seo-content-engine`, `competitor-watch`).
2. Create `templates/<slug>/{mission.yml,BRIEF.md,README.md}`.
3. Validate the YAML locally:
   ```bash
   npx ajv validate -s schema/mission-template.schema.json \
     -d "templates/<slug>/mission.yml"
   ```
4. Add the entry to `manifest.json`.
5. Open a PR. CI will check the schema, paths and slug uniqueness.

## Naming conventions

- Slugs are *outcome-shaped*. `weekly-trend-digest` ✓ ;
  `marketing-mission-1` ✗.
- BRIEFs are in second person — "you will...", not "the agent will...".
  They will be edited by the user before activation.
- Mission templates should always include at least one *kill condition*
  in the BRIEF — when to stop.

## License

[Apache 2.0](LICENSE)
