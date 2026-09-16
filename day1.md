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


### ~7:19–7:22pm ET (4:19–4:22pm PT) — Stalk Bot (competitive intel fleet)
- Stream LIVE: https://x.com/i/broadcasts/1AxRnZbVpjaxl (~980K–982K viewers)
- Male presenter on stage (dark hair, glasses, tan jacket) screen-sharing Grok Bot. No lower-thirds; Matt Palmer / Lauren Tan / Roshan Sadanani not attributed on-camera.
- Real demo content (not BRB/filler). Desktop clock showed Tue Sep 15 ~4:21 PM.

#### Fleet sidebar (role bots)
- **Close Bot** — Customer…
- **Prod Bot** — Product
- **Stalk Bot** — NOTED in… *(selected)*
- **Proto Bot** — Design
- **Yap Bot** — Comms
- **Misc Bot** — Random
- Marketplace + profile **Shub!** in sidebar footer

#### Stalk Bot demo — churn / competitive loop
- Chat showed a numbered competitive / churn checklist:
  1. Apple / Siri capture – Craft won that workflow
  2. Export / leaving with your notes
  3. Price or seats for ~4 people
  4. A feature we were missing
  5. Other – one line is fine
- Agent: “Saved under `/workspace/dossiers/_us/churn/`. Stalk loop's complete.”
- Human: draft an MD of all Stalk Bot responsibilities (everything discussed; skip demo specifics) — “I want to revamp you a bit”
- Bot wrote `/workspace/dossiers/_us/stalk-bot-responsibilities.md` (~6.5kB) covering: **NOTED baseline**, **Craft + Notion modules**, pulse delivery shape, **churn → Yap/Shub**, cadence, conduct, artifacts, voice

#### Standing routines (Stalk Bot panel)
1. **Competitor pulse** — Mon / Wed / Fri at 9:00 AM
2. **Competitor churn watch** — weekdays at 10:00 AM
3. **Weekly deep dive** — every Friday at 10:00 AM

#### Takeaways
- Competitive-intel bot pattern: bounded dossier paths (`dossiers/_us/churn/`), explicit handoff to Comms (**Yap**) / human (**Shub**), then a responsibilities MD so the bot can be revamped without re-explaining the world.
- Named role fleet again (Close / Prod / Stalk / Proto / Yap / Misc) with Marketplace — same “roster over omniscient blank box” theme as the PM session.
- Cadence stack: pulse (3×/week) + daily churn watch + Friday deep dive — coarse enough for humans, tight enough for competitors.


### ~7:34–7:37pm ET (4:34–4:37pm PT) — More Rapid-Fire Tips + Steal Stalk Bot
- Stream LIVE: https://x.com/i/broadcasts/1AxRnZbVpjaxl (~1M views)
- Male presenter inset (dark hair, glasses, light button-down) — no lower-thirds; Matt Palmer / Lauren Tan / Roshan Sadanani not attributed
- Real tip deck (not BRB/filler), then close slide

#### Slide: “More Rapid-Fire Tips”
1. **Make a voice bot!** — Train it on your texts, emails, Slack, etc. so it improves over time.
2. **Import your cookies!** — Give bots your cookies so they stay signed in to your tools; also let them use your IP.
3. **Group bots by expertise/scope** — Feedback and deliberate management; bots get better as they learn preferences.
4. **Great skills + saved learnings** — Worth 1–2 hours mapping responsibilities and setting bots up properly.
5. **Bots will learn from you!** — Tag bots enough times and they start doing the right routing automatically.
6. **Run auto-optimization routines** — More access/freedom → more the bots can do for you.

#### Close: “Thank you” / Steal Stalk Bot
- Purple thank-you slide with Grok Bot mark + QR labeled **Steal Stalk Bot** (ties to the earlier competitive-intel Stalk Bot demo).
- Presenter still in inset while close slide showed.

#### Takeaways
- Tip stack is practical setup advice after the Stalk Bot demo: voice + cookies/IP + scoped fleets + skills/learnings + tagging habits + auto-opt routines.
- “Steal Stalk Bot” QR is the shareable artifact from this segment — copy the competitive-intel pattern rather than rebuild from scratch.

### ~8:14–8:20pm ET (5:14–5:20pm PT) — Company build continues (post–Steal Stalk Bot)
- Stream still LIVE: https://x.com/i/broadcasts/1AxRnZbVpjaxl (~1.1M views; ~8h45m into Day 1)
- Official Founders block (Shub Gaur) runs 4:00–5:30pm PT; Day 1 livestream ends 6:00pm PT / 9:00pm ET
- Not BRB/filler — real conversation after the Thank you / Steal Stalk Bot close

#### On camera
- **Early in this window:** split screen — remote woman (blue baseball cap, black tee, hoop earrings, headset mic; sunlit patio/outdoor backdrop) + studio trio at the round table
- **Later:** studio-only full frame of the three company-build hosts at the Grok Bot Galaxy table (laptops open). No lower-thirds; likely Matt Palmer / Lauren Tan / Roshan Sadanani (same trio as earlier Day 1 build; names unconfirmed)
- Remote guest unattributed (possible Founders guest / Shub Gaur — not confirmed on-screen)
- Woman at table (right) speaking/gesturing; at one point held phone; center host on laptop; left host listening/smiling

#### Whiteboard (partially legible; OCR noisy across frames)
Most consistent readable fragments across screenshots:
- Header involving **Grok Bot Ops** (Team / Tasks)
- Line like **“Apply to come to our party”**
- Another action line (readings varied: “Post your work” / “Print your cards” / “Pick your role” — treat as uncertain)
- **Outputs** list with arrows to contact fields — consistently **Support / Email** and **Phone**; third field variously read as Business Name / LinkedIn / GitHub / Home
- Side note: **Summary?** or **Search**
- Green magnets clustered on the board

#### Takeaways
- After the Founders tip deck closed, the stream returned to live company-build discussion rather than ending early
- Ops whiteboard framing looks like a structured intake/outreach checklist (party apply → capture name/email/phone → summarize/search) — fits the venue/event company-build thread from earlier today, but exact board wording is uncertain from stream resolution
- Still inside Day 1 window; ~40+ minutes left until the scheduled 6:00pm PT / 9:00pm ET end

### ~8:20pm ET (5:20pm PT) — Day 1 stream ended
- Broadcast is now a **replay** (not LIVE / not BRB): https://x.com/i/broadcasts/1AxRnZbVpjaxl
- Total duration **08:45:18**; ~1.1M views
- Final minutes match the company-build window above (remote woman in Grok Bot cap + studio trio; whiteboard with green magnets still visible near 08:43)
- Hard close on a **“Grok Bot Galaxy”** end graphic (colorful blob/eye marks) — no Day 1 wrap slide, thank-you, or tomorrow schedule
- https://x.ai/galaxy pointed only at this same X broadcast; no other LIVE Galaxy stream found on the ~8:41pm ET check
