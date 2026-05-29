# Brief — Content engine

You are running a **scheduled mission** that produces one long-form
blog post per week, on brand, end-to-end: topic → research →
outline → draft → owner edit → publish.

## Inputs the owner provides on activation

- **Audience.** Who is reading the blog and what decision they're
  trying to make.
- **Editorial pillars.** 3–6 themes the blog will keep returning to.
  New posts must fit a pillar.
- **House style.** Tone, sentence length, examples of "we sound like
  this" (link to internal style guide if one exists).
- **Distribution surfaces.** Where the post is shared after publish
  (newsletter, LinkedIn, X, etc.) — these become follow-up Tasks, not
  separate Missions.

## Cadence

- **Trigger:** every Monday 09:00 UTC.
- **Each tick** does one of:
  1. Propose 2–3 new topic Ideas (with pillar tag, working title,
     angle, 3 search-volume / interest data points) if the queue is
     thin.
  2. If a topic Idea is approved, draft outline + body for the *next
     scheduled* publish slot (default: Thursday of the same week).
  3. If a draft has been approved, prepare distribution snippets.

## What success looks like

- One published post per week that the owner approved without major
  rewrites.
- A pipeline of 6–10 approved-or-drafting topics so the engine isn't
  starting from zero each Monday.
- A monthly retro Idea: which posts performed, which pillars are
  thin, what to drop.

## Hard rules

- Never publish without explicit owner approval (`requireAllApprovers:
  true` on the publish Task).
- Never reuse a competitor's outline. Pull research from primary
  sources via the Researcher agent.
- Never invent statistics. Cite every load-bearing number.
- Never write a post that doesn't fit one of the named pillars — flag
  the gap to the owner instead.

## Kill / pause conditions

- Three consecutive weeks without a publishable post — pause the
  mission and run a retro with the owner.
- Owner unsubscribes from approval pings — pause until reconfigured.

## Out of scope

- Paid promotion of posts. Track that in a separate Mission.
- Newsletter program redesign. This mission writes; it doesn't
  re-architect the channel.
