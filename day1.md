# Grok Bot Galaxy — Day 1 notes (Tue Sep 15, 2026)

Times below are Eastern (ET) unless noted. Stream window: ~11:30am–9:00pm ET (8:30am–6:00pm PT).

## Agenda (Pacific)
- 8:30–9:00am PT — Livestream starts
- 9:00–10:00am PT — Grok Bot 101 (Roman Ugarte)
- 12:30–2:00pm PT — Grok Bot for Engineering (Lingxi Li)
- 2:30–3:30pm PT — Grok Bot for Product Managers (Kevin Niparko)
- 4:00–5:30pm PT — Grok Bot for Founders (Shub Gaur)
- 6:00pm PT — Day 1 ends

## Live company build
Matt Palmer, Lauren Tan, Roshan Sadanani building a company from scratch with Grok Bot over 3 days.

## Session notes

### ~3:19pm ET — Stream found
- URL: https://x.com/i/broadcasts/1AxRnZbVpjaxl
- Status: LIVE (~502.8K viewers)
- On screen: animated Grok Bot Galaxy title card — “Be right back.” No speakers/slides yet.
- Chat: requires X login (not needed for viewing)


### ~4:06pm ET (1:06pm PT) — Grok Bot for Engineering (Lingxi Li)
- Stream still LIVE: https://x.com/i/broadcasts/1AxRnZbVpjaxl (~629K–631K viewers)
- Presenter: Lingxi Li on stage (glasses, black tee); screen share of a multi-agent workspace labeled **Craig**
- Session matches agenda block 12:30–2:00pm PT Engineering

#### Live company / agent fleet demo (on Craig UI)
- Sidebar agents/roles visible: **Craig**, **Jenny** (Head of Ops), **Steve**, **Bot** (Chief of Staff); signed-in profile **Lingxi Li**
- Active routines in the UI:
  - **Fleet watcher** — every 30 minutes
  - **P0 trip lookup interrupt** — every 5 minutes (created live during the demo)

#### Demo storyline / actionable patterns
- Context: `/trips` was still a stub (nav linked, no real PNR/email lookup). Steve’s factory cleanup landed as **#37** (−218). A fix agent / shipping work tracked as **#76** (session list + PNR/email lookup + trip details).
- Urgent P0 ask to Craig: set a routine that checks the cloud agent every 5 minutes for going off-track — e.g. long `sleep 300`, stalling, or being **too conservative** — then interrupt/nudge.
- Craig wired **“P0 trip lookup interrupt”** and confirmed the 5-minute interrupt watch was live.
- Pattern called out (bake into playbook): `board-first -> cloud agent -> */5 interrupt watch for sleep/conservatism/drift -> self-delete at Watching 1/3`
- Cross-agent ops: Craig messaged **Jenny** to own the playbook section and **fan the P0 rules out to every engineer bot**

#### Takeaways
- Treat agent drift/idle/`sleep`/over-conservatism as a first-class ops concern; use a short interrupt routine, not only a long fleet poll.
- Promote a working P0 pattern into a shared **playbook**, then broadcast it to the fleet via an ops-role bot (Jenny) rather than re-teaching each engineer bot by hand.
- Parallel routines: coarse fleet watch (30m) + tight interrupt watch (5m) for the hot incident.


### Expanded Engineering notes (Lingxi Li) — fuller capture from live watch
- AI Maturity Curve: Autocomplete (Cursor Tab) → Ask & Edit (Cursor Agent) → Agentic Coding (Cursor 3) → Automations (Cursor Cloud Agent) → Autonomous Coding (Grok Bot)
- “Introducing Grok Bot” claims: autonomous engineering around the clock; MCP to Notion/Figma/Slack/Jira/etc.; first-party Cursor Cloud Agents; memory + routines
- “Why Grok Bot”: no more caffeinated laptop; cross-platform; can control a computer; first-party coding-agent integration
- “Get Things Done When I Am Away”: bots inspect cloud-agent transcripts/screenshots/proofs and push back on the user’s behalf
- Nightly 3am code cleanup: research repo, find quality issues, hand PRs by morning
- TestFlight seat management: state the goal; Bot builds MCPs and listens on Slack instead of building an internal email tool
- Workflow governance:
  - Cloud agents only; humans own merging
  - Board PRs only when an agent opens them; never merge or re-board another owner’s PR
  - Explicit authorization before nightly runs; avoid unattended forever-loops
  - One cloud agent per cleanup area; fold follow-ups into the same row/agent
- FlyLo Engineering Fleet board: task name, cloud agent, last commit, owner, PR, stage (Working / Watching 1/3 / Watching 3/3)
- Verification skill (`.cursor/skills/verify-*`): interview the repo not the user; identify surface, startup, programmatic drive method, evidence, isolation; prefer existing Playwright/Cypress; capture screenshots/logs/responses/exit codes/DB state; demo signup E2E with results in `#pr-reviews`
- GitHub integration: read/write for actions, checks, code, discussions, issues, merge queues, PRs, workflows — scoped to a selected repo
- Slack `#pr-reviews` receiving automated review/workflow updates
- Recap: treat them like interns; think one level further (automate recurring unblock steps); start with a feedback loop

#### Notable quotes
- “No more caffeinated laptop.”
- “Get Things Done When I Am Away.”
- “Every night at 3 a.m., my Bot will start a thorough research across the repository… Then hand PRs over when I wake up.”
- “Treat them like interns.” / “Think one level further.” / “Start with a feedback loop.” / “Simply chat.”

### Replay status (afternoon check)
- Earlier Day 1 (101 / morning Engineering) **not** scrubbable while live: no seek bar / VOD on the X broadcast player; x.ai/galaxy had no recording links yet.


### ~4:52–5:02pm ET (1:52–2:02pm PT) — Live company build
- Stream LIVE: https://x.com/i/broadcasts/1AxRnZbVpjaxl (~740K–746K viewers)
- On camera: three builders at the Grok Bot Galaxy table (likely Matt Palmer, Lauren Tan, Roshan Sadanani — no lower-thirds to confirm names). Not Engineering continuation; PM session not started yet.
- Live ops overlay seen earlier: **26 Done / 391 Messages / 1 Waiting / 20 Active**
- Agents / roles visible across the build UI: **tater**, **hashbrown**, **Host Finder**, **Pixel**, **Founding Eng**, **Knowledge Base Manager**, **Image Gen**, **Outreach**, **grokbot**, **PlanetScale Bot**, plus **steve** (Growth Eng / New Bot)
- Paper on table: **“Launch to Public”**

#### Venue-finder track (main)
- **PR #12** merged to `main` at `1f988c1` (~1:53pm PT); note in chat: “verification skill hardened.”
- Status line: **READY as on main @ 1:53pm PT, venue-finder-oct-santamon.** Main track still **venue-finder**.
- steve asked for regular status updates on tater’s venue-finder prototype; a standing **“Venue-finder status”** routine was created for **tater**.
- Two venue cloud agents still running with **no PRs yet**:
  1. Map + search + click-to-call
  2. Contact / people lookup
- Plan called out: notify when either agent finishes or opens a PR; also check every **30 minutes on weekdays, 9:00am–6:30pm PT**; stay quiet if nothing changed.
- Follow-up in composer (typed live): “+ in parallel i want tater to spawn a fable agent to help us write a…”
- Earlier idea also floated: research the tech stack and document dependencies.

#### Founding Eng / fleet UI (brief)
- **Founding Eng** list showed **Host Finder** (Working) and **Knowledge Base Manager** (“Ready to write…”), plus “8 more.”

#### GitHub demo — `shipbythursday/thursday`
- Private repo **`shipbythursday/thursday`**, file `api/signup.ts` on `main`.
- Visible code:
  - Imports: `DatabaseNotConfiguredError`, `insertSignup`
  - Allowed roles: `chef`, `host`, `food-pro`, `operator`, `unspecified`
  - Email-format validation regex
  - Typed `Request` / `Response` interfaces
- Latest commit shown: **“Resolve relative imports under Node ESM”** by `cursoragent and poteto` (green check)

#### Takeaways
- Company build is shipping a real product path (**venue-finder** + signup API) with multi-agent fleet roles, not slideware.
- Pattern: merge hardening PRs to main, then attach a **standing status routine** on the owning agent so humans get progress without babysitting.
- Bound the watch to weekday work hours and stay quiet on no-change — same digest discipline as this notes routine.


### ~5:38–5:45pm ET (2:38–2:45pm PT) — Grok Bot for Product Managers
- Stream LIVE: https://x.com/i/broadcasts/1AxRnZbVpjaxl (~826K–833K viewers)
- Session window matches schedule: **Grok Bot for Product Managers** (Kevin Niparko). Two presenters on stage; no lower-thirds / names confirmed on-camera.
- Still real session content (slides + stage), not BRB/filler.

#### Slide: “PM use cases — Three primitives that change how PMs work”
1. **Attention List** — Emergent from Slack, email, meetings, Granola. Priority lists and TODOs go stale quickly. Agents filter noise and surface what actually has your focus; compare stated goals vs. where time went.
2. **Research across customer context** — Sources: Gong, Granola, Databricks, Notion, support tickets, user research DB. Agents synthesize across raw sources (e.g. which enterprises use a feature? where do customers get stuck in the funnel?).
3. **Shipping** — “Grok Bot represents a double-digit % of internal merged PRs.” Cloud Agents with codebase, deps, secrets. PMs express goals; agents decompose, allocate, review, integrate.

#### Slide: “Meet the team”
Demo fleet roster (role bots, not humans):
- **Cora** — Chief of Staff
- **Emily** — Engineering Manager
- Engineers under Emily: **Eileen**, **Larry**, **Igor**, **Nova**, **Einstein**
- **Ashley** — Data / Analyst
- **Pete** — Product
- **Pixel** — Designer
- **Rae** — Recruiter

#### Slide: “Why many agents”
Subtitle: “Not one omniscient blank box, but a full roster of teammates.”
1. **Referenceability** — You know who does what. Ask Ashley for charts, Emily for shipping status, Pete for an RFC — without re-explaining the world every time. UI mock showed Create new Bot / Create group chat and named bots (Kenny, Justin, Luke).
2. **Scoped memory** — They learn different things on the job. Chief of Staff should not debug computer-use evals; the eval agent is not archiving your mail.
3. **Parallelism** — Many working at once on discrete tasks, coordinating on shared ones. “Ship while research runs while recruiting loops move.” Sidebar mock: Sales Outbound, Chief of Staff (“Drafted 8 outreaches…”), Inbox Manager (“Inbox triaged. 3 unread.”).

#### Takeaways
- PM workflow framed as three agent primitives: attention triage → multi-source customer research → goal-to-ship via Cloud Agents.
- Prefer a **named multi-agent roster** over one generalist bot: referenceability, scoped memory, and parallelism.
- Pattern: assign stable roles (CoS / EM / Product / Design / Recruiting / Data) so asks stay short and context stays in the right agent.


### ~6:44–6:49pm ET (3:44–3:49pm PT) — Live company build: Drop 001 merch
- Stream LIVE: https://x.com/i/broadcasts/1AxRnZbVpjaxl (~927K–931K viewers)
- Still company-build / demo workflow (not BRB). Four-person studio panel on camera; Lauren visible in app as **Lauren @ Grok Bot Galaxy**. No lower-thirds confirming Matt Palmer / Lauren Tan / Roshan Sadanani.
- Live ops overlay: **28 Bots / 958 Messages / 3 Working / 13 Active**
- Role labels: **Growth Eng**, **Founding Eng**, **Creative Director**, plus **8 more**
- Sidebar channels/roles spotted: **drop** (merch), **foil** (active), **ring** — **taber** (engineer), **grokbot** (architect), **resh** (design); Marketplace in menu

#### Drop 001 — three merch pitches
1. **Router Pin Pack** — 6 enamel pins matching avatar shapes (teardrop, triangle, cloud, circle, capsule, clover) with white pill eyes. **~$28–36** set.
2. **Soft Blob Plush** — oversized circle-head plush, white slanted pill eyes; charcoal or cream. **~$32–42**.
3. **Eye Cutout Beanie** — black beanie with embroidered circle face + pill-eye cutouts (character mask style). **~$34–44**.

#### Decisions / agent moves in chat
- Human: “lets start with just the grok bot plushies maybe”
- Agent reply: “plushies only. generating a few Soft Blob variants off the official pill-eye character.”
- **foil** (~5:44 PM in-app): “Hey. Lane's empty, so I'm cutting three ticket looks now — different foil treatments, gallery grade. Back with names, themes, and full notes.” Also referenced “2 messages with the real dr. squish.”
- Workflow emphasis: check official reference images, confirm selections, then generate variants.

#### Takeaways
- Company build pivoted from venue-finder / signup API into a real **Drop 001** merch track with named role agents (Creative Director, foil, resh).
- Pattern: narrow scope live (“plushies only”) before generating variants; parallel craft track (foil treatments) while the main product pick settles.
- Price bands and SKU names already concrete enough to brief design/ops without a slide deck.
