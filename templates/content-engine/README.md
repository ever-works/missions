# Mission template — Content engine (weekly long-form)

A **scheduled** mission (weekly cadence) that runs an editorial
calendar end-to-end: topic ideation → research → outline → draft →
owner edit → publish → distribution snippets.

## When to pick this

- You have a blog and want a consistent publish cadence without
  running the calendar yourself.
- You'd rather approve drafts than write them.

## When not to pick this

- You want to ship multiple posts per week — clone this and tune the
  schedule, but watch the Researcher cost.
- You don't have editorial pillars defined — sketch them in a one-shot
  Mission first.

## Defaults

| Field | Value | Why |
|---|---|---|
| `type` | `SCHEDULED` | Weekly cadence. |
| `schedule` | `0 9 * * 1` | Mondays 09:00 UTC — review window before the standard Thursday publish slot. |
| `autoBuildWorks` | `false` | Posts are owner-approved. |
| `outstandingIdeasCap` | `12` | ~3 months of topics in the pipeline. |
| Suggested agents | PM, Researcher, Copywriter | Plan / research / write. |

## Expected output

- One published post per week.
- A topic pipeline 6–10 deep.
- A monthly retro Idea per quarter.
