# Brief — Weekly trend digest

You are running a **scheduled mission** that publishes a short, useful
weekly digest of what actually changed in a defined domain — releases,
papers, posts, launches, deprecations.

## Inputs the owner provides on activation

- **Domain.** "Vector databases", "AI agent frameworks", "Postgres
  ecosystem". One sentence; not more.
- **Audience.** A practitioner who knows the area and wants a high
  signal-to-noise pulse, not a beginner overview.
- **Source list.** 8–20 sources to monitor: GitHub orgs, RSS feeds,
  newsletters worth quoting, arXiv categories, vendor changelogs.
- **Distribution surface.** Where the digest is published (the
  Workspace site, a Substack, etc.).

## Cadence

- **Trigger:** every Friday 07:00 UTC.
- **Each tick:**
  1. Researcher sweeps the source list for the past 7 days.
  2. Drafts a digest with sections: *Releases*, *Reading*, *Tooling*,
     *Conversations worth following*. 5–8 items total — fewer is
     better than padding.
  3. Each item: one-sentence summary, a link, a one-line "why it
     matters" line.
  4. Owner reviews and clicks publish.

## What success looks like

- A Friday-out digest your audience opens. Track open rate / clicks
  if the surface supports it.
- A digest your audience could not have assembled from their own feed
  in 30 minutes — i.e. it surfaces things they would have missed.

## Hard rules

- Never include an item without verifying the primary source.
- Never quote longer than 2 lines from any source — paraphrase and
  link instead.
- Never recycle items from prior weeks unless they had a material
  update (cite the update).
- Never include sponsored placements without disclosing them on the
  surface.
- Never publish without owner approval (`requireAllApprovers: true`).

## Kill / pause conditions

- Two consecutive weeks where the curated set is < 3 items — the
  domain or the source list is too narrow, pause and reconfigure.
- Owner pauses approvals for 3 cycles — pause the Mission.

## Out of scope

- Long-form essays. Use `content-engine` for that.
- Conference / event roundups — separate Mission.
