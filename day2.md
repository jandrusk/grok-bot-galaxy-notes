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


### ~2:40–2:45pm ET (11:40–11:45am PT) — Live company build resumes (CUPCAKE prototype)
- Stream LIVE again after a short “Be right back” intermission: https://x.com/i/broadcasts/1PKqrNyvmYwGb (~100K → ~101.3K views)
- Still in the gap before Sales (12:30–2:00pm PT agenda block)
- No on-screen nameplates; studio panel matches Day 2 company-build trio (curly-haired man in grey hoodie, bearded man, woman with glasses)

#### Studio panel
Three builders back at the Grok Bot Galaxy table after BRB holding screen (bot-icon ring + “Be right back”).

#### CUPCAKE app — low-fi wireflow (tldraw)
Screen-share of **tldraw.com** wireframes / clickable proto for a game-style app named **CUPCAKE** (browser tabs also showed “Game documentation…” and “Cupcake … proto…”).

**Core flow**
1. **Login** — “CUPCAKE login with X”
2. **Home** — header **@potato Diamond** / **@poteto Diamond** (spelling varied across frames); actions: **new match**, **team**, **log out**
3. **Choose captain** — captain selection screen; interaction log showed “Clicked dr eggbot captain card”
4. **Random options** — placeholders **random 1** / **random 2**
5. **Manage bots** — list under profile header:
   - **dr eggbot**
   - **tradbot** (note: “(automatically generated)”)
   - **steve**
6. **Hire** — text field **bot template url** + **HIRE** button
7. Confirmation — status text “Clicked Confirm team”

Ties back to earlier Day 2 bot-competition whiteboard (Grok Bot Template → Draft team → Set lineup → Compete; CHA/DEX/INT; “trad bot”).

#### Takeaways
- Company build is shipping a playful multiplayer/team game (“CUPCAKE”) where bots are roster units you hire from a template URL and pick as captain.
- Auto-generated **tradbot** + manual hires (**dr eggbot**, **steve**) suggest template-driven bot onboarding into the product.
- Still pre-Sales session; expect more build or a handoff around 12:30pm PT / 3:30pm ET.

### ~5:55–6:05pm ET (2:55–3:05pm PT) — Grok Bot for SDRs (Simon Lackowski) — prospecting army live
- Stream still LIVE: https://x.com/i/broadcasts/1PKqrNyvmYwGb (~277K → ~283K views)
- X title: “Grok Bot builds a Game Studio LIVE” (@bot)
- Agenda match: **Grok Bot for SDRs (Simon Lackowski)** (2:30–3:30pm PT)
- On-camera: short dark hair, black shirt (no nameplate); shared screen is the Grok Bot workspace, not CUPCAKE

#### Demo product: Simon Bot / Chief of Staff coordinating an SDR agent army
Left sidebar bots (tool integrations in parens):
- **Shakespeare** (Gmail) — drafting outbound email
- **PLG Bot** (Salesforce)
- **Amplemarket Bot** (Enrichment) — sometimes flagged with a warning
- **Company Research Bot** (Sumble)
- **Web Search Bot** (Exa)
- **Voice of the Customer Bot** (Gong)
- **Usage Bot** (Databricks)
- **Army Huddle**
- **Simon Soldier 5** / **Simon Soldier 1**

#### Prospecting Flyo / Grok Bot ICP run
- Artifact: `2026-09-16-flyo-prospecting-full.csv` (~237KB)
- Merged **25 Director+** prospects across Salesforce, Sumble, Gong, Enrich, Usage, and Exa
- Per row: unique email + LinkedIn connect/DM copy
- All 25 enrolled in sequence **`grokbot-cold-v1`** — **draft-only, nothing sent**
- Exa coverage: 25/25 with all five Soldiers
- Shakespeare finishing Gmail draft IDs (8 already live; 17 new/updated)
- Segment themes called out: OCC Desk, winter freeze, Atlas briefs, people-systems, FP&A board packs

#### Example personalized angles (on-screen)
- **Wendy** — “OCC brief that finishes itself”
- **Xena** — “Winter freeze rationale rewritten every Tuesday”
- **Quinn** — “Network Agent Desk + Grok Bot”

#### Routines panel (standing SDR automations)
- **50 Daily Prospects** — daily 8:00 AM
- **Inbox Manager** — weekdays 8:00 AM
- **Accounts Signal Scan** — weekdays 8:00 AM
- **Sequencer Daily** — weekdays 8:00 AM
- **Sequencer SF Triggers** — webhook

#### Takeaways
- SDR pattern = Chief of Staff bot orchestrating specialized tool bots (Gmail, Salesforce, enrichment, Sumble, Exa, Gong, Databricks) + “Soldiers” for parallel research.
- Safety default in the live demo: enroll cold sequence as **draft-only**.
- Daily prospecting + inbox + account-signal routines are the always-on layer; webhook Sequencer SF Triggers ties CRM events to sequencing.
- Screenshots: `/workspace/grok-bot-galaxy-screenshots/day2-evening-check-01.png`–`04.png`, `day2-evening-detail-01.png`–`08.png`

### ~6:40–6:50pm ET (3:40–3:50pm PT) — Company build resumes (Cupcake game studio fleet)
- Stream still LIVE: https://x.com/i/broadcasts/1PKqrNyvmYwGb (~319K → ~325K views)
- X title unchanged: “Grok Bot builds a Game Studio LIVE” (@bot)
- After the SDR block, screen share is back on the **game-studio company build** (not Simon Bot). Studio PiP: three builders on the Galaxy couch (company-build trio).

#### Studio bot fleet (left sidebar roles)
Specialized bots coordinating the Cupcake / game-studio build (names as shown on screen; some OCR-fuzzy):
- **Chief** — orchestration
- **Crit** — Game Designer (mechanics / SoT)
- **Duke** — Foundry / eng (PR merges, fastbuild)
- **Ping** — Slack bridge
- **Dot** — infra (“PlanetScale is connected”)
- **Echo** — Recording / client-vs-crit notes
- **Gina** (prototyping) / **dr. eggbot** / **Grok**
- **Bake** — asked to review client impl against Lauren’s SoT / rules

#### Crit mechanics SoT (on-screen design notes)
Clean version of combat / onboarding rules being locked for ship:
- **Captain + 2 mystery** (tape only) → secret order + no peek
- Type triangle: **CHA > INT > DEX > CHA** at **+33%**
- Ship first: **billboard the triangle**; glyph strip always on; three type icons under it; tape flashes +33% / edit loss
- One forced tutorial: you have CHA, they show INT → put CHA on it
- Teach on the **tape**, not pre-fight; keep **fog** until the fight
- After each round: full reveal of what resolved (one-line e.g. CHA>INT — scores)
- **Ghost NPC** with mid-setup types for onboarding only
- **No shop**; **Captain edge** and redeem later
- Older “product-plan-draft” mechanics path called dead until overruled

#### Agent workflow moments
- Dot → ask **Bake** to review client vs Lauren SoT; Bake pinged to surface gap list
- Looking up Lauren’s recent DM → Cupcake v1 **design critique cards** (Notion); instruct **dr. eggbot** to spin up a mechanics-expert game-design bot with that doc as context
- **Ping** Slack path: @mentions anywhere + DMs; Slack MCP connect card; message drafted to Lauren + Matt with Kanban / Cupcake board link
- Routines visible: Slack-mentions watcher; **Cupcake today punch** (weekday multi-fire)

#### Eng progress on Cupcake web
- PR opened/merged for **replay tape playback on web** (feat: play back the replay tape / “potato”)
- Gap list called out after merge: match shell → billboard → fixed CHA vs INT tutorial → fog reveal (+ kiss line); match-loop / billboard / fog reach still missing vs clerk + `/api/live` + admin on `apps/web`
- Kanban / Tasks board for Cupcake: site refresh, engine iterations, verify bot SQL, etc. (Todo / In Progress / Done)

#### Takeaways
- Company build pattern mirrors SDR army: **Chief + role bots** (Crit design, Duke eng, Ping Slack, Dot DB, Bake review, eggbot specialist spawn) over shared SoT + Notion critique cards.
- Mechanics are converging on fog-of-war tape reveal + rock-paper CHA/INT/DEX triangle — ship the billboard tutorial before shop/meta.
- Human loop stays in-chat: Lauren/Matt get Slack + Kanban; bots draft/send after connect card.
- Screenshots: `/workspace/grok-bot-galaxy-screenshots/day2-evening2-check-01.png`–`06.png`

### ~7:19–7:27pm ET (4:19–4:27pm PT) — FlyLo Airlines support automation demo
- Stream still LIVE: https://x.com/i/broadcasts/1PKqrNyvmYwGb (~348.9K → ~354.2K views)
- X title unchanged: “Grok Bot builds a Game Studio LIVE” (@bot) — content switched away from Cupcake to a **FlyLo Airlines** support/ticket company build
- Male presenter in PiP (name not readable); solo desk/stage laptop demo

#### Product / knowledge sources
- Product: **FlyLo Unlimited WiFi** pass
- Knowledge: **Public Docs / FAQ** (Notion) + **Internal Policies**
- Policy snippets shown:
  - Refunds: email support for full review/reply
  - Cancel subscription: if refund unavailable, cancel at end of billing period (support can schedule)
  - FAQ **Pass sharing**: **No** — cannot share pass for simultaneous use (each traveler needs own pass)
  - FAQ troubleshooting: WiFi off/on → rejoin FlyLo WiFi → open browser → Connect

#### Support bot fleet (sidebar)
- **Reply** — connected to policy; answers tickets (Stripe + docs)
- **Demo Ticket Generator** — generates support tickets on a schedule
- **Alert** — monitors logs / posts to `#alerts-dg`
- **Tune** — learns from support; edits Public Docs FAQs
- **Build** — building features / connectors
- **Marketplace**

#### Stripe refund loop (Carter + Damon)
- User: “okay now try to answer carter and damon.”
- Reply runs refund loop: Rules → Stripe → reply
- **T-54 Carter Carr** (`carter@fake.com`): in policy (day 0) → canceled + **full $20 refund**, replied. **Trace 39**. Product shown earlier as “Unlimited All” monthly.
- **T-55 Damon Deer** (`damon@example.com`): out of policy (20 days) → **denied refund**, offered **cancel at period end**. **Trace 40**. Stripe sandbox customer on **Digital Collections Pro** monthly ($20 next invoice Oct 27).
- Both: assigned, **GB-Seen + GB-Answered**, snoozed **Waiting for Customer**
- Stripe UI shown in sandbox (“Changes you make here don't affect real customers”)
- Support ticket UI: threads for Damon / Susan Smith; Urgent flag on Damon’s thread

#### Tune ↔ Reply KB loop (Pass sharing / Power outlets)
- Tune editing **Public Docs FAQs**:
  - Earlier decision: keep **Power outlets** as green FAQ add; leave **Pass sharing** out (then revisited)
  - Later: **Pass Sharing** restored under Public/FAQ (green **No**); pinged Reply
  - Transient issue: Power outlets disappeared after add; Tune re-checking with Reply
- Decision UI pattern: A/B prompts (“Add Pass sharing?” / “Leave it”) with human confirm before KB write

#### T-56 Elena Ellis — low-confidence handoff → high-confidence reply
- Ticket: can I share my FlyLo Unlimited WiFi pass? Customer **Elena Ellis** (`elena01@aa.com`), company `aa.com`, assignee **David**, priority Normal, status Waiting for customer
- First pass (**Trace 41**): Reply could **not** auto-reply — Pass Sharing missing from Public Docs FAQ → handoff (`GB-Seen`, note, unassigned); asked Tune to restore FAQ line
- Tune: “Pass Sharing is live again under Public/FAQ (green No). Holding on Elena's customer reply until you say go…”
- User: “Okay can you try again now”
- Second pass (**Trace 42**): high-confidence reply — pass cannot be shared for simultaneous use; each traveler needs own pass. Assigned, **GB-Answered** / **GB-Seen**, snoozed Waiting for Customer
- Email failure surfaced: Elena’s address on a **suppression list** — retry won’t work until reactivated
- Next ticket visible: **T-57 VIP Victor Vance**

#### Slack: FlyLo Airlines `#ask-grok-bot`
- Workspace **FlyLo Airlines**; channels include `#ask-grok-bot`, `#alerts-dg`
- David: “Internal Q&A is live here. Ask FlyLo support questions and I’ll answer from Public Docs and Internal Policies. Tip: invite @Cursor … so the auto-reply routine can hear messages.”
- Cursor Agent added to channel for auto-replies
- Sample questions: “what is the refund policy?”, “A customer is asking me if the plane has outlets -- pretty sure yes”, “What is the Refund SOP?”

#### Takeaways
- Support pattern = **Reply** (ticket + Stripe actions) + **Tune** (KB/FAQ writes) + **Demo Ticket Generator** + **Alert** (Slack) + human A/B confirm on doc changes
- Policy-gated refunds: in-window full refund vs out-of-window deny + cancel-at-period-end
- Missing FAQ → low-confidence handoff; restoring FAQ unlocks high-confidence auto-reply (Trace 41 → 42)
- Internal agent Slack channel mirrors customer KB (Public Docs + Internal Policies) with @Cursor auto-reply
- Screenshots: `/workspace/grok-bot-galaxy-screenshots/day2-evening3-check-01.png`–`06.png`, `day2-evening3-detail-01.png`–`07.png`

### ~7:42–7:49pm ET (4:42–4:49pm PT) — Cupcake sound design (Suno) + product UI
- Stream still LIVE: https://x.com/i/broadcasts/1PKqrNyvmYwGb (~366.6K → ~368.3K views)
- X title unchanged: “Grok Bot builds a Game Studio LIVE” (@bot)
- After FlyLo support block, back on **Cupcake / game-studio company build**. Studio PiP: company-build trio (Matt / Lauren / Roshan) on the Galaxy couch.

#### Sound design track (Roshan Notion + Suno)
- Notion task (**Roshan's Space HQ → Tasks**): **“Sound design for the game”** — Cupcake H2H battle SFX, UI cues, stadium bed, win/lose stingers. Marked **off auth/FE↔BE critical path** (parallel track).
- Owner: **Tone**; status: **Foley v0 + Suno v6 mini refs + orch v4**; updated 2026-09-16 PT
- Doc: **Listen — Suno v3 mini refs (Roshan, 2026-09-16)** — “Orchestral Power Stadium” general refs; WIP goal: attach audio cues to GalaxyBot & build the soundtrack. Note to check a **Battle Suite** that is orchestral — no Roland.
- Suno refs listed (~2:30–2:35 each, one ~1:00): Suno ref 01–05
- **Foley v0 stubs (experimental)** in Notion: mute-first sketches, soft peaks (~-12 dBFS), click-to-play; **do not autoplay the bed in product**. Cue stubs:
  - 01 draft pick · 02 lineup lock · 03 reveal · 04 slot win · 05 slot lose · 06 match win
- Live Suno create (suno.com): generating with **v6-mini**; example prompts/tracks seen:
  - EDM workout / high-energy gaming prompt (128 BPM, D major) → tracks like **Fire Bus**, **Dot Fast-Entry**
  - Action-RPG boss theme: *“orchestral ostinato, aggressive strings, bold brass, hard timpani and taiko hits, minor key, high stakes duel, cinematic but game-score, big drops and builds, 132 BPM, no EDM drops, no chiptune…”* → **Final Duel**; also **Draft Room Energy** (menu music)
- Other tabs visible during share: Cursor Agent, Excalidraw, Strudel REPL, cupcake / bug-reports docs
- Notion sidebar people/channels visible during listen doc: Matt, Roshan, Lauren, Tiana, Igor, Grok, Radost, Shantanu

#### Cupcake web product UI (live)
- **CUPCAKE** app (cream UI, pink pig mark) signed in as **@poteto** — **GOLD · 1000**
- **Create a new bot** modal: “paste your bot template to create a new teammate”; URL field `https://x.ai/bot/marketplace/...`; Cancel / pink **CREATE**
- **Global leaderboard** screen (empty shell + Back) — product surface progressing beyond match/hire flows

#### Takeaways
- Audio is an intentional parallel workstream: Foley stubs + Suno mini refs feed Cupcake H2H without blocking auth/FE/BE.
- Soundtrack direction skews **orchestral stadium / boss-fight score**, not chiptune/EDM drops for the battle suite.
- Product UI progress: marketplace bot-template hire path + global leaderboard shell live in the Cupcake web app.
- Screenshots: `/workspace/grok-bot-galaxy-screenshots/day2-evening4-check-01.png`–`06.png`
