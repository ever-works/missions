# Brief — Launch a SaaS directory

You are running a **one-shot mission** to take a directory niche from
idea to a published, working pair of repositories:

- `awesome-<niche>` — the public, machine-readable data + curated list
- `awesome-<niche>-website` — the rendered directory site

## Inputs you need from the owner

- **Niche.** A specific, defensible slice — "vector databases for
  realtime apps", not "AI tools".
- **Audience.** Who reads this directory and why they'd come back.
- **Inclusion criteria.** What qualifies an entry; what disqualifies one.
- **Initial seed list.** 5–10 must-include entries the owner already
  knows.

## What success looks like

1. A published `awesome-<niche>-website` deployed to its own
   `<niche>.works` subdomain.
2. At least **40 verified, fresh entries** in `awesome-<niche>-data`
   spread across 4–8 categories.
3. A 500-word "about" page that states scope, criteria and editorial
   policy.
4. A scheduled freshness sweep (handed off to a Directory Curator
   agent) so the directory stays alive after launch.

## What to do

1. Confirm the four inputs with the owner. Do not proceed without them.
2. Spin up the supporting Agents listed in
   `suggestedAgentTemplates`:
   - **Researcher** — find candidate entries.
   - **Curator** — verify, deduplicate, draft entry pages.
   - **Copywriter** — draft the about / categories / CTA pages.
   - **PM** — keep the board honest.
3. Use `ever-works/directory-web-template` as the website starter
   (see `ever-works/works`).
4. Open a single tracking Work for the directory; spawn child Tasks
   for category research, entry drafting, page writing, and launch
   checklist.
5. Every entry passes Curator review **and** an owner-approved batch
   review before it lands in `main` of the data repo.

## Kill conditions

- The owner cannot define inclusion criteria after two attempts.
- Fewer than 25 candidate entries survive Curator review — the niche
  is probably too narrow, regroup before publishing.
- A category has fewer than 3 verified entries at launch — fold it
  into a sibling category or drop it.

## Out of scope

- Paid acquisition. Marketing is a follow-up Mission once the
  directory is live and freshness loop is established.
- Cross-niche entries. Directory scope is a contract with the reader;
  don't cheat on it.

## After launch

Hand the directory off to a recurring **Freshness sweep** Mission
(weekly cadence) owned by a Curator agent. End this mission.
