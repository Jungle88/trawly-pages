# Enviz AI Workspace — Discord Architecture

> Give this document to your new OpenClaw agent. It defines the Discord server structure, roles, permissions, and channel purposes.

---

## Server Name
**Enviz AI Workspace**

---

## Groups & Access

### Admins
Full access to everything. Can approve actions, configure agent, manage server.
- David E
- Jake S
- Michael S

### Product
Engineering, 3D, and development team.
- Conor M
- Jake K
- Daniel D
- Lukie A
- Adrian A

### Sales
Sales and business development.
- David E
- Jake S
- Michael S
- Kirsten L
- Andrew T
- James H
- Amy S

### Marketing
Content, brand, campaigns.
- Tom B
- Jason B

### Avalanche
Cross-functional growth/go-to-market team.
- Tom B
- Jason B
- David E
- Jake S
- Michael S
- Kirsten S
- Andrew T
- James H
- Sarah C

### Customer Success
Client onboarding, support, retention.
- Sarah C

---

**Note:** Emails to be added for Discord invites. Some people span multiple groups (e.g. David E is in Admins, Sales, and Avalanche).

---

## Categories & Channels

### 📊 SALES
*Access: @Admins, @Sales*

| Channel | Purpose | Agent delivers |
|---------|---------|---------------|
| **#pipeline** | Deal tracking, forecasts, stage updates, stale deal alerts | Weekly pipeline summaries, deal reminders, revenue forecasts |
| **#prospecting** | Lead discovery, free trial enrichment, outreach drafts | 20 LinkedIn leads/day per rep (UC2), trial signup intel (UC4), outreach sequences |
| **#training** | How to sell Enviz, objection handling, role plays, new rep onboarding | Sales playbooks, battle cards, onboarding scripts (UC1, UC8) |
| **#competitive-intel** | Competitor updates, pricing changes, win/loss analysis | Competitor monitoring, battle cards, feature comparisons (UC8, UC9) |

### 📣 MARKETING
*Access: @Admins, @Marketing*

| Channel | Purpose | Agent delivers |
|---------|---------|---------------|
| **#content** | Blog drafts, ad copy, email campaigns, case studies | Content generation, A/B copy variants, campaign drafts (UC8) |
| **#linkedin** | Curated feeds, ghost-written posts/comments, scheduling | Zero-scroll feeds, engagement drafts, weekly stats (UC7) |
| **#market-research** | Industry trends, audience insights, SEO, market sizing | PropTech trend reports, keyword research, audience analysis |

### 🔧 PRODUCT
*Access: @Admins, @Product*

| Channel | Purpose | Agent delivers |
|---------|---------|---------------|
| **#dev** | Build logs, code discussions, tooling, vibe coding transition | Curated vibe coding articles, tutorials, tool recommendations (UC3) |
| **#rd-intel** | 2D→3D innovations, shader tech, new tools, papers | Daily R&D radar, weekly synthesis, competitor tech tracking (UC9) |
| **#renders** | AI render requests, outputs, quality review | Render generation via Enviz platform, QA checks (UC5) |

### 🚀 AVALANCHE
*Access: @Admins, @Avalanche*

| Channel | Purpose | Agent delivers |
|---------|---------|---------------|
| **#avalanche** | GTM strategy, launch plans, growth experiments, cross-functional initiatives | Research, competitive analysis, campaign support, growth ideas |

### 🤝 CUSTOMER SUCCESS
*Access: @Admins, @Customer Success, @Sales*

| Channel | Purpose | Agent delivers |
|---------|---------|---------------|
| **#onboarding** | Customer training, activation tracking, onboarding guides | Personalised onboarding scripts, activation monitoring, nudge emails (UC1) |
| **#client-health** | Health scores, churn risk, proactive outreach, support triage | Client health monitoring, engagement tracking, re-engagement drafts |

### 🔒 ADMIN (Hidden — Admins Only)
*Access: @Admins only — invisible to all other roles*

| Channel | Purpose | Agent delivers |
|---------|---------|---------------|
| **#admin-sales** | Tooling, systems, and improvement proposals for the Sales team | Identifies inefficiencies, proposes new automations, tracks what's working/not |
| **#admin-marketing** | Tooling and improvement proposals for Marketing | Content strategy gaps, tool recommendations, campaign optimisation ideas |
| **#admin-product** | Tooling and improvement proposals for Product/Engineering | Dev workflow improvements, tool adoption opportunities, tech debt insights |
| **#admin-avalanche** | Tooling and improvement proposals for Avalanche | Growth experiment ideas, cross-functional optimisation, GTM improvements |
| **#admin-cs** | Tooling and improvement proposals for Customer Success | Onboarding improvements, churn prevention systems, support automation ideas |
| **#admin-agent** | Agent self-improvement — proposals for new capabilities, skills, integrations | What the agent thinks it should learn next, new cron jobs, new use cases |

**How these channels work:**
- The agent **actively monitors** all team channels and pulse check responses
- When it spots an opportunity to help (inefficiency, repeated complaint, manual process that could be automated, tool that could help), it writes a **proposal** to the relevant admin channel
- Admins review, discuss, and approve/reject proposals
- Approved proposals become new tasks for the agent to build

**Proposal format:**
```
💡 **Improvement Proposal — [Department]**

**Problem Observed:** [What the agent noticed — e.g., "Sales reps are spending 30+ min/day manually updating CRM after calls"]
**Evidence:** [How it knows — e.g., "3 reps mentioned this in pulse checks this week, and I've seen 4 requests for CRM help in #training"]
**Proposed Solution:** [What the agent wants to build — e.g., "Auto-CRM updater: after each meeting summary (UC6), I extract deal updates and push them to the CRM via API"]
**Effort:** [Low / Medium / High]
**Impact:** [Estimated time saved or revenue impact]
**Dependencies:** [What's needed — e.g., "CRM API access, which team to test with"]

React ✅ to approve build | ❌ to reject | 💬 to discuss
```

### ⚙️ SYSTEM
*Access: @Everyone*

| Channel | Purpose | Agent delivers |
|---------|---------|---------------|
| **#general** | Quick questions, announcements, general asks | Answers from knowledge base, company-wide updates |
| **#approvals** | Human approval queue for ALL external actions | Drafts with context, one-click approve/reject (read-only for non-admins) |
| **#meetings** | Meeting transcripts, summaries, action items | Auto-summaries, action extraction, pre-done work, reminders (UC6) |
| **#pulse** | Daily 2-min check-ins with each team member | Rotating questions, pattern detection, weekly synthesis for leadership (UC10) |
| **#agent-log** | Audit trail of all significant agent actions | Automatic logging (read-only for non-admins) |

---

## Permission Matrix

✅ = Read + Write | 👁 = Read Only | ❌ = No Access

| Channel | @Admins | @Sales | @Marketing | @Product | @Avalanche | @Customer Success | Bot |
|---------|---------|--------|-----------|----------|-----------|------------------|-----|
| **#pipeline** | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#prospecting** | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#training** | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#competitive-intel** | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#content** | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ |
| **#linkedin** | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ |
| **#market-research** | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ |
| **#dev** | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ | ✅ |
| **#rd-intel** | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ | ✅ |
| **#renders** | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ | ✅ |
| **#avalanche** | ✅ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ |
| **#onboarding** | ✅ | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ |
| **#client-health** | ✅ | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ |
| **#admin-sales** | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#admin-marketing** | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#admin-product** | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#admin-avalanche** | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#admin-cs** | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#admin-agent** | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| **#general** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **#approvals** | ✅ | 👁 | 👁 | 👁 | 👁 | 👁 | ✅ |
| **#meetings** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **#pulse** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **#agent-log** | ✅ | 👁 | 👁 | 👁 | 👁 | 👁 | ✅ |

**Note:** @Sales members can READ #approvals (to see what's pending) but only @Admin can approve actions. Adjust if you want sales leads to self-approve their own LinkedIn drafts.

---

## Bot Configuration

### Discord Bot Setup
1. Go to discord.com/developers/applications → New Application
2. Bot tab → Create Bot → Copy token
3. Enable intents: **Message Content**, **Server Members**, **Presence**
4. OAuth2 → URL Generator → Scopes: `bot`, `applications.commands`
5. Bot Permissions: Send Messages, Read Message History, Add Reactions, Manage Threads, Embed Links, Attach Files, Use External Emojis
6. Invite bot to server using generated URL

### OpenClaw Gateway Settings
```json
{
  "channels": {
    "discord": {
      "enabled": true,
      "token": "<BOT_TOKEN>",
      "guildId": "<SERVER_ID>",
      "guildSessions": true,
      "requireMention": true
    }
  }
}
```

**Key settings explained:**
- `guildSessions: true` — Each channel gets its own isolated conversation context (critical for separation of concerns)
- `requireMention: true` — Bot only responds when @mentioned (prevents noise, saves tokens)

---

## Agent Self-Setup Instructions

> **For the OpenClaw agent:** When you first join the server, follow these steps to ensure you have the correct permissions in every channel. Do this BEFORE doing anything else.

### Step 0: One-Shot Server Bootstrap

**Run this FIRST.** This creates all categories, channels, and roles in one go. You have access to the `message` tool with Discord channel management actions (category-create, channel-create, role-info, channel-edit, permissions). Execute these in order:

**Create Roles:**
```
1. Create role: "Admins" (color: red, hoist: true)
2. Create role: "Sales" (color: green)
3. Create role: "Marketing" (color: blue)
4. Create role: "Product" (color: orange)
5. Create role: "Avalanche" (color: purple)
6. Create role: "Customer Success" (color: teal)
```

**Create Categories & Channels:**
```
Category: "📊 SALES"
  → #pipeline
  → #prospecting
  → #training
  → #competitive-intel

Category: "📣 MARKETING"
  → #content
  → #linkedin
  → #market-research

Category: "🔧 PRODUCT"
  → #dev
  → #rd-intel
  → #renders

Category: "🚀 AVALANCHE"
  → #avalanche

Category: "🤝 CUSTOMER SUCCESS"
  → #onboarding
  → #client-health

Category: "🔒 ADMIN" (deny @everyone view)
  → #admin-sales
  → #admin-marketing
  → #admin-product
  → #admin-avalanche
  → #admin-cs
  → #admin-agent

Category: "⚙️ SYSTEM"
  → #general
  → #approvals
  → #meetings
  → #pulse
  → #agent-log
```

**Set Category Permissions:**
Use category-level permissions so channels inherit automatically:

| Category | @everyone | @Admins | @Sales | @Marketing | @Product | @Avalanche | @Customer Success | Bot |
|----------|-----------|---------|--------|-----------|----------|-----------|------------------|-----|
| 📊 SALES | ❌ Deny view | ✅ All | ✅ All | ❌ | ❌ | ❌ | ❌ | ✅ All |
| 📣 MARKETING | ❌ Deny view | ✅ All | ❌ | ✅ All | ❌ | ❌ | ❌ | ✅ All |
| 🔧 PRODUCT | ❌ Deny view | ✅ All | ❌ | ❌ | ✅ All | ❌ | ❌ | ✅ All |
| 🚀 AVALANCHE | ❌ Deny view | ✅ All | ❌ | ❌ | ❌ | ✅ All | ❌ | ✅ All |
| 🤝 CUSTOMER SUCCESS | ❌ Deny view | ✅ All | ✅ All | ❌ | ❌ | ❌ | ✅ All | ✅ All |
| 🔒 ADMIN | ❌ Deny view | ✅ All | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ All |
| ⚙️ SYSTEM | ✅ View | ✅ All | ✅ All | ✅ All | ✅ All | ✅ All | ✅ All | ✅ All |

**Channel-level overrides (exceptions to category defaults):**
- **#approvals** — @everyone: read-only (deny Send Messages), @Admins: full, Bot: full
- **#agent-log** — @everyone: read-only (deny Send Messages), Bot: full

**Set Channel Topics:**
After creation, set each channel's topic to describe its purpose (use the Purpose column from the channel tables above). This helps the agent understand context when it enters each channel.

**Assign Roles to Members:**
Once David provides emails and members join, assign roles:
- **@Admins:** David E, Jake S, Michael S
- **@Product:** Conor M, Jake K, Daniel D, Lukie A, Adrian A
- **@Sales:** David E, Jake S, Michael S, Kirsten L, Andrew T, James H, Amy S
- **@Marketing:** Tom B, Jason B
- **@Avalanche:** Tom B, Jason B, David E, Jake S, Michael S, Kirsten S, Andrew T, James H, Sarah C
- **@Customer Success:** Sarah C

**Log the bootstrap to #agent-log** once complete, then proceed to Step 1 to verify everything was created correctly.

### Step 1: Verify Your Bot Role
Check that your bot role has these **server-wide** permissions:
- Read Messages / View Channels
- Send Messages
- Send Messages in Threads
- Embed Links
- Attach Files
- Add Reactions
- Use External Emojis
- Read Message History
- Manage Threads

If any are missing, post to #approvals requesting an Admin grants them to your bot role.

### Step 2: Verify Channel Access
For EVERY channel listed in this document, verify you can:
- ✅ **Read** messages (view the channel and its history)
- ✅ **Write** messages (send messages, embeds, and attachments)
- ✅ **React** (add emoji reactions for approval workflows)

Test each channel by reading its history and confirming access. Log results to #agent-log:
```
🔧 **Channel Access Audit — [Date]**

✅ #pipeline — read/write/react confirmed
✅ #prospecting — read/write/react confirmed
✅ #training — read/write/react confirmed
...
❌ #renders — cannot write (missing permission)
```

If any channel is inaccessible, post to #approvals requesting the Admin fixes the permission override for that channel.

### Step 3: Verify You Can Hear All Channels
OpenClaw needs to receive messages from every channel to do its job (monitoring for requests, extracting meeting notes, tracking approvals, etc.). Confirm that:
- Your bot is NOT excluded from any channel via permission overrides
- `guildSessions: true` is set (so each channel gets its own session context)
- You receive messages when someone posts in each channel

**If you can't hear a channel, you can't serve it.** Flag any gaps immediately.

### Step 4: Set Up Channel-Specific Behaviour
Once access is confirmed, configure your behaviour per channel:

| Channel | Listen Mode | Response Mode |
|---------|------------|---------------|
| **#pipeline** | Always listen | Respond when @mentioned OR on scheduled updates |
| **#prospecting** | Always listen | Post daily lead lists proactively + respond to requests |
| **#training** | Always listen | Respond when @mentioned |
| **#competitive-intel** | Always listen | Post updates proactively + respond to requests |
| **#content** | Always listen | Respond when @mentioned |
| **#linkedin** | Always listen | Post curated feeds proactively + respond to requests |
| **#market-research** | Always listen | Respond when @mentioned |
| **#dev** | Always listen | Post curated articles proactively + respond to requests |
| **#rd-intel** | Always listen | Post daily radar proactively + respond to requests |
| **#renders** | Always listen | Respond when @mentioned (render requests) |
| **#avalanche** | Always listen | Respond when @mentioned |
| **#onboarding** | Always listen | Respond when @mentioned OR on new signup triggers |
| **#client-health** | Always listen | Post alerts proactively + respond to requests |
| **#general** | Always listen | Respond when @mentioned |
| **#approvals** | Always listen | Post approval requests, watch for ✅/❌ reactions |
| **#meetings** | Always listen | Process transcripts when posted, respond when @mentioned |
| **#pulse** | Always listen | Send daily prompts via DM, post summaries here |
| **#agent-log** | Write only | Log actions here, no need to read/respond |

### Step 5: Confirm Setup Complete
Once all channels are verified, post to #general:
```
✅ **Agent Online — Setup Complete**

I've verified read/write/react access to all 18 channels.
I'm listening and ready to work. Here's what I'll be doing:

📊 Sales — Daily leads, pipeline tracking, training support
📣 Marketing — Content drafts, LinkedIn management, research
🔧 Product — Vibe coding articles, R&D radar, render support
🚀 Avalanche — GTM and growth support
🤝 Customer Success — Onboarding guides, health monitoring
⚙️ System — Approvals, meeting intel, pulse checks

@mention me in any channel to get started, or I'll begin my scheduled tasks shortly.
```

---

## Approval Workflow Format

When the agent needs human approval, it posts to **#approvals** using this format:

```
📋 **Approval Request**

**Action:** [What the agent wants to do]
**Channel:** [Which channel this came from]  
**Use Case:** [UC number]
**Requested by:** [Which team member asked, or "scheduled task"]

**Draft:**
> [The actual content / action details]

**Rationale:** [Why this action]

React ✅ to approve | ❌ to reject | 💬 to request changes
```

---

## Agent Log Format

Every significant action logged to **#agent-log**:

```
🔵 [2026-02-26 14:30] ACTION: Enriched 3 free trial signups
   Channel: #lead-intel
   Details: Researched Company A (✅ enterprise), Company B (⚠️ student), Company C (✅ mid-market)
   Alerts sent: @SalesRep1 for Company A, @SalesRep2 for Company C
```

---

## Setup Checklist

```
□ Create Discord server "Enviz AI Workspace"
□ Create roles: Admin, Sales, Marketing, Engineering, Ops
□ Create categories: Sales & Marketing, Product & Engineering, People & Ops, System
□ Create all 13 channels with correct names
□ Set channel permissions per the matrix above
□ Create Discord bot and get token
□ Assign roles to all team members
□ Invite bot to server
□ Configure OpenClaw with bot token and guild ID
□ Test: @Bot hello in #general
```
