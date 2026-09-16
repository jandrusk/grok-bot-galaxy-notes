# Grok Bot Galaxy — Day 2 notes (Wed Sep 16, 2026)

Times below are Eastern (ET) unless noted. Stream window: ~11:30am–9:00pm ET (8:30am–6:00pm PT).

## Agenda (Pacific)
- 8:30–9:00am PT — Day 2 Livestream Starts
- 9:00–10:30am PT — Grok Bot for Sales Engineering (Amrita Venkatraman)
- 12:30–2:00pm PT — Grok Bot for Sales (SpaceXAI Sales Team)
- 2:30–3:30pm PT — Grok Bot for SDRs (Simon Lackowski)
- 4:00–5:00pm PT — Grok Bot for Customer Support (David Gan)
- 6:00pm PT — Day 2 Livestream Ends

## Live company build
Matt Palmer, Lauren Tan, Roshan Sadanani continuing the 3-day company build (seen early Day 2 before role sessions).

## Stream
- Day 2 URL: https://x.com/i/broadcasts/1PKqrNyvmYwGb
- Hub: https://x.ai/galaxy

## Session notes

### ~11:55am–12:00pm ET (8:55–9:00am PT) — Live company build (pre–Sales Engineering)
- Stream LIVE: https://x.com/i/broadcasts/1PKqrNyvmYwGb (~22.7K → ~25.6K views during first check)
- Title on X: “Day 2: Grok Bot Galaxy Livestream” (@bot)

#### Product-needs whiteboard
Handwritten “product needs” list on digital whiteboard:
- ads
- marketing
- more team members!! (interns?)
- seed funding?
- figure out distribution (hey chat)
- call us
- X Chat

Presenter PiP: curly-haired man in grey hoodie (studio).

#### Bot competition / game workflow (whiteboard)
Flow: **Grok Bot Template → Draft your team → Set your lineup → Compete!**
- Attribute boxes labeled **CHA / DEX / INT** (RPG-style)
- Notes: “cool names for these abilities”; boxes for Ability INT / Ability CHA; “trad bot”
- Studio PiP: two men at desk (curly hair + bearded)

#### Studio panel
Three builders at the Grok Bot Galaxy table (curly-haired man, bearded man, woman with glasses/reddish hair typing). Overlay: “Grok Bot Galaxy Day 2”. Likely continuing company build.

#### Engineering / MVP plan review
Screen share of GitHub `docs/plans/01-mvp.md` with female presenter in PiP.
- TypeScript `BotSource` shape in plan:
  - `templateId`, `canonicalUrl` (`https://x.ai/bot/...`), `templateUrl` (`https://cursor.com/api/bot/templates/...`), `sourcePayload`, `sourceDigest`, `fetchedAt`
- Open checklist items:
  - Parse only supported `https://x.ai/bot/...` templateId (boundary tests for invalid URLs)
  - Fetch `https://cursor.com/api/bot/templates/` before storage (missing / oversized payload checks)


### ~12:01–12:10pm ET (9:01–9:10am PT) — Grok Bot for Sales Engineering (Amrita Venkatraman)
- Stream still LIVE: https://x.com/i/broadcasts/1PKqrNyvmYwGb (~27.1K → ~36K views)
- Speaker slide / role: **Amrita Venkatraman — Lead Field Engineer**
- Matches agenda block 9:00–10:30am PT Sales Engineering

#### Agenda
1. Welcome
2. Introducing Grok Bot
3. Why Grok Bot
4. Sales Engineer Use Cases
5. Demo
6. What we learned
7. Q&A
8. Build

#### AI Maturity Curve
1. **Ask (Chatbots)**
2. **Do a task (Copilots)**
3. **Delegate outcome (Bot)**
4. **Staff function (Team of Bots)**

#### Introducing Grok Bot (annotated product UI)
Example bots in sidebar: Sales Assistant / Sales Dashboard, Deal Assistant, Cloud Architect, Internal Manager, Website Designer.
Callouts:
- Create bots for different jobs
- Message bots like teammates
- Bots keep context in memory and improve as they go
- Log bots into your tools and they use them like you
- Set up automations and routines
- Easily share your bots with others

#### Why Grok Bot
- **Easy as iMessage** — messaging-first threads (e.g. Sales Outbound, Hire Manager)
- **Always-on agents** — 24/7
- **Uses your tools like you** — e.g. “Log in to Salesforce”; computer-use character in demo
- **Finishes the work** — create bots for jobs, give directions, automations/routines
- **Shareable Templates** — e.g. “Feng shared Remy with you” / “Peng shared Kenny with you”

#### Sales Engineer use cases (four bots)
1. **“Engineer” Technical Resource** — Turns technical questions into clear customer-facing text for Slack/Email; digs into docs or codebase for evidence.
2. **Customer Expert** — Uses plugins (Databricks, PlanetScale, etc.) to check customer usage, update account plans, flag unusual usage, highlight power users.
3. **“Echo”** — Live-updates your deck during/after discovery; turns Granola/Gong transcripts into “What we heard” slides and next steps.
4. **Competitive Intel** — Uses competitor products; tracks releases via X and blogs; keeps battlecards current.

#### Demo — bot **Mimi** (Customer Proof Point Researcher)
- Sidebar sections: FE Work, Housekeeping, Product, Unassigned; **Mimi** under FE Work
- Compiling customer proof points for **Jellyfish** and **SpaceX**
- Example proof point content:
  - Solution: BugBot as first-line AI review (18 engineers, before/after)
  - Impact: PR throughput more than doubled (+110%, PRs 82% smaller, fewer changes & bugs)
  - Quote attributed to Irene, Senior Software Engineer
- Live coaching loop: user asked to change impact header to “PR throughput more than doubled while bugs decreased”; Mimi confirmed rewriting + fresh screenshot
- Right pane: Routines / Media / Computer tabs; “Mimi’s screen” computer-use view active

#### Takeaways
- SE bots as a small fleet: technical writer, usage/account expert, post-call deck builder, competitive intel — not one mega-bot.
- Messaging-first + shareable templates are the packaging for field teams.
- Demo pattern: proof-point researcher with computer use + tight human edit loop in chat.

