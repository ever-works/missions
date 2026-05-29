# Mission template — Weekly trend digest

A **scheduled** mission that publishes a short, high-signal weekly
digest of what actually changed in a defined domain.

## When to pick this

- You want a low-effort, recurring newsletter / blog post that earns
  its read time.
- You have 8–20 sources you already trust and you'd just like the
  scan + summarise loop automated.

## When not to pick this

- You want long-form opinion pieces — use `content-engine`.
- You don't have a defined domain yet — narrow it first.

## Defaults

| Field | Value | Why |
|---|---|---|
| `type` | `SCHEDULED` | Weekly cadence. |
| `schedule` | `0 7 * * 5` | Fridays 07:00 UTC — ready for owner approval before end-of-week sends. |
| `autoBuildWorks` | `false` | Digests are owner-approved before publish. |
| Suggested agents | Researcher, Copywriter | Sweep + summarise + polish. |

## Expected output

- A Friday digest your audience opens.
- 5–8 carefully chosen items per issue, each verified against its
  primary source.
- A monthly "sources to add / drop" Idea.
