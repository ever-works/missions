# Mission template — Launch a SaaS directory

A **one-shot** mission that takes a directory niche from idea to a
launched, populated `awesome-<niche>-website` + `awesome-<niche>-data`
pair using Ever Works' existing directory machinery.

## When to pick this

- You have a specific niche and an opinion about who reads it.
- You want the platform to coordinate the standard build pattern
  (data repo + website repo + curation + first 40 entries) without
  you running it.

## When not to pick this

- You want continuous output rather than a one-time launch — use
  `weekly-trend-digest` or `content-engine` instead.
- The niche isn't defined yet — sketch it in a Mission with type
  `ONE_SHOT` and title "Sketch directory niche" first.

## Defaults

| Field | Value | Why |
|---|---|---|
| `type` | `ONE_SHOT` | Launches have an end. The follow-up freshness loop is a separate Mission. |
| `autoBuildWorks` | `false` | The directory repos are non-trivial; humans approve the initial publish. |
| `outstandingIdeasCap` | `25` | Plenty for category research without flooding the board. |
| Requires human approval | `true` | Pre-launch — every Idea passes through the owner. |
| Suggested agents | PM, Researcher, Curator, Copywriter | The standard four-seat directory team. |

## Expected output

- One new `awesome-<niche>-website` GitHub repo deployed.
- One new `awesome-<niche>-data` GitHub repo with ≥ 40 entries across
  4–8 categories.
- An "about" page + editorial policy.
- A handoff to a recurring freshness-sweep Mission.

## Customisation

Edit `BRIEF.md` (the prompt) before activating. The four inputs
section is the one the platform will ask you for before the Mission
starts ticking.
