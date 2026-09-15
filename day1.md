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

