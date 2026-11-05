# Build on an open-source app

> This is the catalog listing. The template the platform actually reads (its `.works/mission.yml`, prompts and
> full README) lives in [`ever-works/build-on-open-source-app-mission-template`](https://github.com/ever-works/build-on-open-source-app-mission-template).

## What this template is

A weekly Mission for an App Work you already run: it proposes small product changes on your own copy of an
open-source application, waits for your approval, and keeps each change open until it is actually live.

## What you choose

| Field    | Meaning                                                                  |
| -------- | ------------------------------------------------------------------------ |
| Product  | What you are building for your business, e.g. "clinic booking".          |
| Business | Who it is for, e.g. "Riverside Physio".                                  |
| App Work | The App Work this Mission improves — it must already exist and be yours. |

## What it sets up

| Setting        | Value                          |
| -------------- | ------------------------------ |
| Cadence        | Mondays 08:00 UTC              |
| Output         | Tasks on the attached App Work |
| Tasks per week | up to 2                        |
| Open Tasks cap | 4                              |
| Approval       | New Tasks wait in **Backlog**  |
| Budget         | $15.00 per agent run           |
| Relation       | _Improves_ the chosen App Work |
| Goals          | two delivery Goals, in _Draft_ |

## What it recommends for the app itself

`agents.requireHumanMergePaths` for schema and migration paths, `agents.maxPullRequestChangedLines: 400`, and
`display.protectedPaths` for `LICENSE*` and `NOTICE*`. **Propose these rules** opens a Task that changes the App spec
by pull request; the template never edits it directly.

## Related files

- `mission.yml`: the catalog entry for this listing.
- `BRIEF.md`: the one-page brief.
- Runtime manifest and full README: [`ever-works/build-on-open-source-app-mission-template`](https://github.com/ever-works/build-on-open-source-app-mission-template).
