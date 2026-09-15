# Pomegranate — Frequently Asked Questions

Everything you're likely to ask while getting set up and running: what Pomegranate is,
what people use it for, and how to operate it. Organized by what you're trying to get
done rather than by which screen it lives on.

This page is the reference the onboarding assistant answers from. It is versioned — fetch
it fresh rather than working from a cached copy.

**Contents**
1. [What Pomegranate is, and what people use it for](#1-what-pomegranate-is)
2. [The mental model — folders, subfolders, and what happens to corrections](#2-the-mental-model)
3. [Adding content — what happens when a document comes in](#3-adding-content)
4. [Organizing, renaming, archiving, deleting](#4-organizing-renaming-archiving-deleting)
5. [Structured tracking — templates and data agents](#5-structured-tracking)
6. [Automating what comes in — connected apps, schedules, content rules](#6-automating-what-comes-in)
7. [Controlling who (and what AI) sees what](#7-controlling-who-sees-what)
8. [Working through it with your team — Collab and Work agents](#8-collab-and-work-agents)
9. [Account, access, and admin housekeeping](#9-account-access-and-admin)
10. [How your data is processed — models and pipeline](#10-how-your-data-is-processed)
11. [Where your data is stored](#11-where-your-data-is-stored)
12. [How your data gets in — the five routes](#12-how-your-data-gets-in)
13. [Removing your data](#13-removing-your-data)

---

## 1. What Pomegranate is

**What is Pomegranate, in one paragraph?**

Pomegranate is a **context vault**: a place your team puts the things it needs to keep straight —
decisions, requests, insights, status, rules — so that both people and AI assistants can get a
straight answer about what's currently true. You feed it documents, notes, transcripts, and
messages; it reads each one and pulls out the individual statements worth keeping, then answers
questions from those statements **with citations back to where each one came from**.

**What problem does it actually solve?**

The thing your team knows is scattered across documents, threads, call transcripts, and people's
heads, and most of it is out of date without being marked as out of date. So two things go wrong:
people re-ask and re-decide things that were already settled, and AI assistants — which now do a
lot of the drafting — work from whatever context someone happened to paste in, producing confident
work that contradicts a decision made last month.

Pomegranate fixes the second problem by making your team's actual context something an agent can
query, and the first by making the newest statement on a topic automatically win over older ones,
so you get what's true now rather than an archaeological dig.

**How is that different from a wiki or a notes app?**

Three ways:

- **It doesn't need curating to stay correct.** A wiki page is only right if somebody remembers to
  edit it. Here, a correction supersedes the old statement automatically; the old one stays
  readable as history (see [§2](#2-the-mental-model)).
- **It answers rather than stores.** You ask a question in plain language and get an answer with
  citations, or an honest "I don't know" — not a search results page.
- **It's built for agents as much as people.** Claude, ChatGPT, and Cursor can query it directly, so
  the drafting they do for you is grounded in your team's real context.

**Do I have to use it as a team, or is it useful on my own?**

Both, and the two are different jobs. On your own it's a memory that agents can reach — everything
you'd otherwise re-explain at the start of every chat. As a team it's the shared record that stops
people from working off different versions of the truth. Each role below is split along exactly
that line.

---

### Use cases by role

Pomegranate isn't role-specific — it's a place to track things, and every role tracks different
things. What follows is what people actually set up.

#### Product Managers

*On your own* — Keep a running inbox of **feature requests** as they arrive from anywhere, then let
an agent cluster, dedupe, and triage them instead of doing it by hand. Keep the **user insights**
from interviews and calls so an agent can pull the relevant ones when you're drafting. Draft a
**PRD** grounded in that stored research rather than from memory.

*As a team* — Store PRDs and, critically, **the changes to them**, so anyone can see what the spec
says now and what it used to say. Track **project status** so "where is X?" is answerable without
a meeting. Track **dependencies** between people and teams so blockers surface before they bite.
Track **OKRs** and their check-ins.

#### Go-to-market and Marketing

*On your own* — Park **social media ideas** and their schedule somewhere an agent can pick them up.
Keep your own campaign briefs and notes.

*As a team* — Run **prospecting** and a lightweight **CRM** for a team too small to justify a real
one. Keep a register of **campaigns and their performance**, so next quarter's planning starts from
what actually worked. Track **goals** against results. Store the team's **brand voice** so every
draft can be checked against it before it ships.

#### Sales

*On your own* — Per-account notes from your calls, your pipeline, and what you owe whom by when.

*As a team* — Shared **account history**, so a deal can be picked up by someone else without a
handover meeting. **Objection and competitor responses** built from what actually gets said on
calls. **Won/lost reasons**, so the pattern becomes visible. **Pricing and discount decisions**, so
nobody improvises a number that contradicts last week's call.

#### Customer Support

*On your own* — Your own log of how you solved the awkward ones.

*As a team* — **Known issues and their workarounds**, kept current as they change. **Canonical
answers**, so two people don't tell the same customer different things. **Escalation paths and
ownership**. Recurring **complaint themes**, which is the feed product should be reading.

#### Technical teams

*On your own* — A decision journal, and a record of what you shipped that writes your standup for
you.

*As a team* — **Architecture decisions** with their supersession history, so "why is it like this?"
has an answer. **Runbooks and incident postmortems**. **Onboarding context**, so a new engineer can
ask the codebase's history questions directly. **Conventions and standards**, which drafts and PRs
can then be reviewed against.

#### Program and Project Managers

*On your own* — Your own roll-up across the things you're accountable for.

*As a team* — **Cross-project status** in one place. A **dependency and blocker register**. A
**risks and issues log**. **Milestone and date-change history**, so slippage is visible as a
pattern rather than a surprise.

#### Operations and Admin

*On your own* — Vendor notes and the renewals you personally need to chase.

*As a team* — A **contract register** with renewal dates and terms. **Accounts payable**.
**Procurement** requests and their approvals. **Inventory**, for teams small enough that a
dedicated system would be overkill. Internal **policies and how-we-do-it** answers.

#### Compliance, Legal, and Risk

*On your own* — The obligations you personally own and their deadlines.

*As a team* — A **policy book** that states the rules as they currently stand. **Review drafts
against those rules** and get back citations to the specific rule, rather than a vague opinion. An
**audit trail** of who accessed what. **Regulatory changes** tracked as they supersede each other.

#### Knowledge management

*On your own* — A personal reference vault your agents can reach.

*As a team* — **Track the documents that matter** and keep what's current actually current. Put an
answer-with-citations layer over material that's otherwise scattered across drives and threads —
the point being not to store more, but to make what's stored answerable.

#### Founders and Leadership

*On your own* — Everything you'd otherwise re-explain to an assistant at the start of every
conversation: strategy, positioning, what you've already decided and why.

*As a team* — **Strategy and positioning** as the reference every piece of work can be checked
against. **Decisions and their reversals**, so the team stops relitigating. **Goals** and where
they actually stand. And a way to see what the team is asking about and **what the context is
failing to answer** (<a href="#9-account-access-and-admin">§9</a>).

---

## 2. The mental model

*The confusion that causes most of the others.*

**A "folder" contains "subfolders" — isn't that just nested folders? What's actually different?**

A **folder** is a whole workspace: its own database of knowledge, its own members, settings,
integrations, and billing. A **subfolder** is a partition inside one folder — each has its own
template (what kind of information it tracks) and its own set of nodes, but subfolders in the same
folder share the same document store, the same members, and the same team-wide features (Ask the
team, Automations, and so on).

You can't nest a subfolder inside a subfolder. It's a flat, one-level split, not a filesystem tree.

**If subfolders are separate, why do they "share documents"?**

A document is stored once at the folder level, then routed into whichever subfolder(s) it's
actually about. If it's relevant to two subfolders, each extracts its own nodes from it — but
there's still only one copy of the source document. Deleting a subfolder removes its nodes, not the
shared document (see [§4](#4-organizing-renaming-archiving-deleting)).

**Should my team run one folder with many subfolders, or separate folders per team/project?**

Use **subfolders** when the content should be askable together and administered by the same people
— e.g. "Product," "Marketing," "Customer voice" as subfolders of one company folder, so "Ask the
team" can span all of them at once.

Use a **separate folder** when you genuinely want separate membership, separate billing, or
separate admin control — a different company, or a sandbox you don't want mixed into production
data.

**I wrote something and later corrected it — does the old, wrong version stick around and confuse
future answers?**

No. Newer statements on the same topic take precedence over older ones — the correction wins. The
older version isn't erased, though: it's archived in a *supersession chain* so the history stays
readable if you ever need to see what changed and when.

**The library says "12 active nodes · 54 archived in supersession chains" — where did those 54 go?**

They're still there, just not part of the current-answer set. Archived nodes are superseded
versions kept for history — nothing is deleted and nothing you did needs undoing. Day-to-day
questions and reports only draw on the active ones.

---

## 3. Adding content

**When I add a document, does it go live right away, or wait for someone to approve it?**

By default it **applies immediately**. There is no approval queue between adding something and it
being usable. The router reads the document, decides which subfolder(s) it belongs to, and files it
straight in.

**Is there ever a case where it does wait for a decision?**

Exactly one: when the router genuinely can't tell where a document belongs, or thinks it warrants
an entirely new subfolder that doesn't exist yet. In that case it *holds* the document and asks you
to approve, pick an existing subfolder instead, or reject it — nothing is filed anywhere until you
answer. Outside that case, there's no manual review step.

> **If you see wording that says otherwise:** the in-app "How to use" guide still says in
> places that "nothing is saved to your graph until you approve it." That describes an earlier
> design and is out of date — the two answers above are how it behaves today.

**A document landed in the wrong subfolder (or the default one instead of where I expected) — how
do I get routing right?**

Routing reads each subfolder's **Description** (what it's for) and its auto-generated **Content
summary** (what it currently holds) to decide fit. If a description is vague or missing, documents
that should go there will keep missing it. Sharpening the description is usually the actual fix —
not a one-off correction to a single document.

**I want everything about a specific topic or client to always land in one exact subfolder — how do
I force that?**

Two ways:
- Write `#the-subfolder-slug` anywhere in the text you're adding (each subfolder's slug is shown
  next to its name in Setup), or
- In **Add sources**, pick the subfolder directly from the destination dropdown instead of leaving
  it on "Automated."

Either overrides the router for that document.

**What does "Instructions" do when I'm adding a source?**

It hands the document to an agent instead of the plain router. You can tell it things like "pull
out the people mentioned into a People folder, create it if it doesn't exist," and it acts on that
instruction rather than filing by best guess.

---

## 4. Organizing, renaming, archiving, deleting

**I made a typo in a subfolder's name, or its purpose changed — how do I fix it without losing
content?**

Click the pencil icon next to the subfolder's name (sidebar, or Setup → Subfolders) to rename it
inline. Renaming doesn't touch its contents. You can update its Description separately at any time
— editing it locks it against auto-refresh, so it stays what you wrote until you change it again.

**A subfolder nobody uses anymore — archive it or delete it?**

**Archive** if you might want it back, or just want it out of the active list: it hides the
subfolder but keeps every node intact. **Delete** only when you're sure — it's permanent and
removes the subfolder's nodes, candidates, edges, and wiki pages for good.

**I deleted a subfolder by mistake — can I undo it?**

If you *archived* it, yes — nothing was lost. If you used the permanent **Delete** action, no. It
requires confirming twice precisely because it can't be undone.

**If a document is shared into two subfolders and I delete one of them, does the document disappear
from the other?**

No. Deleting a subfolder removes only what's local to it (its nodes, candidates, edges, wiki
pages). The document is stored at the folder level; any other subfolder routed the same document
keeps its own copy and its own nodes, untouched.

**Can I move a note between subfolders, or merge two subfolders?**

Not directly — there's no move or merge action today. The practical workaround is to re-add the
source content into the target subfolder (pinned with its `#slug`), then clean up or archive the
original.

**Why can't I delete or archive the very first ("default") subfolder?**

Every folder needs at least one place for content to land when nothing else fits, so the original
subfolder is protected from archiving and deletion. You can still rename it and change its
description — you just can't remove it.

**Our folder's name is wrong — how do I rename the whole folder (not a subfolder)?**

There's currently no rename control for a folder itself; Setup shows only its permanent ID, not an
editable name field. The practical fix today is creating a new folder with the right name and
moving content and members over. There is no in-place rename.

**How do I delete an entire folder, and what actually happens?**

Setup → **Delete folder** removes every graph node, candidate, review, source, MCP connection
token, audit row, and uploaded file belonging to it. The action is logged right before it runs,
you're signed out of the folder immediately after, and it cannot be undone. There is deliberately
no second "are you sure" beyond the one confirmation — only do this when you mean it.

---

## 5. Structured tracking

*Templates and data agents.*

**Everything I add just becomes a generic note — I want actual to-dos, decisions, or open questions
instead.**

Attach a **data agent** to the subfolder. A data agent pulls structured, typed entries out of every
document instead of writing one plain note per document — e.g. a to-do list that tracks new tasks
and priority changes, or a decision log that tracks decisions made and reversed. Open the
subfolder's Library view and use **Attach one** next to the "No data agent attached" banner.

**What's the difference between a "template" and a "data agent"?**

A **template** is the reusable definition — its name, its job, and what kinds of entries it
extracts. A **data agent** is that same template once it's attached to a subfolder and switched on.
Same object; the word changes depending on whether you mean the design or the running thing.

(Neither is the same as a *Collab* or *Work* agent — see [§8](#8-collab-and-work-agents).)

**I attached a data agent, but my older documents weren't processed — how do I backfill?**

When attaching, choose **All documents, right now** instead of **New documents only**. That
reprocesses everything already in the subfolder through the new template.

**What are the 12 built-in templates?**

To-do list (tasks, status changes, priority changes) · Project status (status sections) ·
Appointments · Decision log (decisions made / reversed) · Evidence log · Goals & metrics (goals
set / check-ins) · People list (contacts, status updates) · Policy book · Spec sheet (spec
additions, resolutions, open questions) · Strategy · User insight (interview notes) · Brand voice
(voice attributes, voice rules, lexicon, specimens).

**None of them fit what I'm tracking — can I make my own?**

Yes. **New template** lets you define a name; a one-paragraph description of the job it does (this
is what the extraction prompt is built from, so be concrete); its cardinality (Many standalone
entries, a Fixed replaceable set of fields, or a Dated log); and its **entry kinds** — the sections
it extracts, each with a color and a label.

**I edited one of the standard templates — did I just change it for everyone?**

No. Editing a standard template automatically forks a private custom copy for your workspace. The
built-in original is untouched and still available to everyone else exactly as it was.

**I want to stop structured tracking on a subfolder — what happens to what's already extracted?**

Detaching a data agent stops new documents being processed through it; the subfolder returns to
plain notes for anything added afterward. Everything already extracted stays in the graph.
**Detach** and **Change template** are separate actions — Change swaps the template going forward,
also without removing what's there.

**Who's allowed to create, attach, or delete templates?**

The workspace owner or an admin — not every member. One person can't accidentally reshape how the
whole subfolder is tracked for everyone else.

**What's the "Report," and when would I use it instead of browsing the subfolder?**

The Report is a single readable page generated from a subfolder's current content — meant to be
read end to end and handed to someone as-is, including someone outside Pomegranate, rather than
them browsing individual nodes. Use **Generate** on the subfolder's Report card, then view or
share.

---

## 6. Automating what comes in

**How do I get Gmail, Slack, Drive, Notion and friends flowing in automatically instead of
copy-pasting?**

**Add sources → From your apps**, then connect the app. Gmail, Drive, Slack, Notion, GitHub, Jira,
Teams, and Fathom are supported today; Linear is coming soon. Connecting goes through a hosted
OAuth broker — you sign in on the real app's own consent screen, and Pomegranate only ever receives
a connection reference, never your actual login token.

**I only want a slice of my inbox — one client, one label — not everything.**

Use the **What to pull** field after connecting. It takes a plain-language query like "emails from
george@example.com" or "invoices from last quarter" rather than importing the whole mailbox.

**How do I make it check on a schedule instead of clicking "Add sources" every time?**

Set up a **Scheduled pull** (Automations → Scheduled pulls). Connect the app once and it's checked
automatically on your chosen cadence. A one-time "Add sources" pull only grabs what matches right
now.

**Is my Gmail app password actually stored?**

It's stored encrypted, specifically for connecting your own account, and is never shown again once
saved — not even to you. It's used only to pull your mail on your behalf. Treat it like any other
app-specific password you'd generate for a third-party integration.

**How do I disconnect an app?**

Setup → Integrations → **Connected apps** has a disconnect action per app. Disconnecting stops
future pulls; it does not retroactively remove documents already pulled in.

**I don't want certain content (PII, customer names, casual chatter) stored at all — how do I
enforce that?**

Write a **Content rule** (Automations → Content rules) in plain language — e.g. "Hide PII from
customer call transcripts," or "Do not index casual chatter in call transcripts and Slack
communication." Each rule has its own audience scope (who the shaping or redaction applies for) and
can be previewed before you switch it on, so you can confirm it catches what you meant.

---

## 7. Controlling who sees what

Three audience levels govern every note: **Only me**, **My AI agents**, and **Team**.

**I wrote something sensitive — how do I guarantee teammates, and even their AI tools, can never
see it?**

Set that note's audience to **Only me**. Only you, inside the app, can see it — your own AI agents
can't even use it as context, let alone a teammate's.

**I want my own AI assistant to use something as context, but keep it invisible when a teammate
asks — is that real?**

Yes, that's the middle tier, **My AI agents**. You and your own connected AI tools (Claude, ChatGPT
and so on) can draw on it; teammates and their AI agents cannot. **Team** is the only tier everyone
in the folder — and their AI agents — can see.

**If I invite a teammate to my folder, do they instantly see everything I've ever written?**

No. Sharing is per item, not per folder. Adding someone to a folder gives them access to nothing by
itself; they see only the individual notes marked **Team**. Anything marked **Only me** or **My AI
agents** stays invisible regardless of membership.

**I marked something visible to the team and want to undo that — does it retroactively pull back?**

You can change a node's audience at any time (per node, or in bulk for a whole category via that
section's **Share** control). It stops future visibility and future use as context. It cannot reach
into an answer or a draft already generated and already handed to someone — that's already out.

**Does the audience setting apply everywhere, or just the web app?**

Everywhere the content can be reached — web app, Slack, and anything connected via MCP (Claude,
ChatGPT, Cursor). The same three levels govern what any surface is allowed to retrieve.

---

## 8. Collab and Work agents

**I don't see "Ask the team" or any agents in my sidebar — how do I get them?**

They're an early-preview feature, off by default. Turn on **Sidebar agents** in Setup → Agents &
templates.

Note this toggle is remembered **per browser, per folder** — it is not workspace-wide. A teammate
turning it on for themselves doesn't turn it on for you, and it won't follow you to another
browser or device.

**What's the difference between a Collab agent and a Work agent?**

**Collab agents** act outward, on the team's shared context — asking questions of it, watching it,
checking things against it (Ask the team, Get updates, and others in that catalog). **Work agents**
act on your own context only — drafting, synthesizing, catching you up on your own work (Give
updates, and others). Neither is a **data agent**, which is a per-subfolder extraction template
([§5](#5-structured-tracking)).

**How do I add or remove specific agents?**

Each group has its own **+ Add collab agent** / **+ Add work agent** control, opening a catalog
scoped to that group. Enable only the ones you want visible.

**What's the difference between "Ask the team" and "Get updates"?**

**Ask the team** answers one plain-language question right now, with citations, from what's already
written down. **Get updates** is a standing watch — describe a topic once and it sends you a
synthesized, cited update on a cadence you pick, instead of you re-asking.

**Can I ask a teammate's folder something directly?**

Yes, if you're a member of it. **Ask the team** lets you add another folder or teammate to the
question, and each folder answers on its own from what it actually holds.

**I keep manually writing status updates — can I generate them instead?**

That's **Give updates** (a Work agent): describe what to report on once, and it watches your own
folder and sends teammates a synthesized, cited update on your cadence. There are ready-made
presets — a weekly "what I shipped" summary, a "decisions I made" digest.

**The assistant said "I don't know" about something I'm sure is documented — why?**

Answers only ever come from what's actually stored *and visible to you*. If nothing relevant has
been added, or it's marked in a way you can't see, it says "I don't know" rather than guessing.
Check the folder's **Usage** page and filter to **Unanswered** to see exactly which questions have
been getting this response — that's your list of real gaps.

---

## 9. Account, access, and admin

**How do I make sure "ask your folder" by my name or handle in Slack resolves to me?**

Fill in your profile under Setup → **General** — display name, Slack handle, Slack member ID.
That's what lets teammates and their AI tools reference you by name, email, or @handle and resolve
correctly to your folder, from Slack, claude.ai, or Claude Code alike.

**How do I add a teammate who hasn't signed up yet?**

Setup → Team & access → **Folder Members** lets you invite by email before their first sign-in —
access is waiting the moment they log in with that address. If they're on your company's email
domain, you can tap them from the quick-add list instead of typing the address.

**What can a regular member not do that an admin can?**

Members read and contribute to the graph. Admins additionally manage connections, members, and
folder settings — inviting and removing people, connecting apps, deleting the folder.

**How do I find out whether a colleague already has a folder before I create a duplicate?**

Setup → Team & access → **Explore folders**. It lists everyone sharing your email domain and which
folder(s) each belongs to, so you can find an existing one and request access instead of standing
up a redundant one.

**I'm in more than one folder — how does Pomegranate know which to use?**

Each surface has its own **default folder** (Setup → Integrations → Default folder), set
independently for "All surfaces," Slack, and MCP (claude.ai / Claude Code). Your Slack default and
your MCP default don't have to match.

**How do I connect Pomegranate to Claude.ai, ChatGPT, or Cursor?**

Setup → Integrations → **Claude.ai connector** generates a one-click connector URL; paste it into
claude.ai → Settings → Connectors, no separate auth step. The URL *is* the credential and is shown
only once, so save it when you create it. For Claude Code, Claude Desktop, or Cursor, use
**Connection token** instead — it mints a raw token you configure the client with directly.

**How do I audit and clean up old connectors?**

They're listed under Setup → Integrations → Claude.ai connector, each showing when it was created
and last used. Revoke (trash-can icon) any you no longer recognize.

**Is there a log of who accessed what and when, for compliance?**

Yes — Setup → General → **Audit log** records sign-ins, graph changes, source uploads, deliverable
submissions, context accesses (who asked and the shape of the request, never the verbatim
content), and MCP token issuance and use. It exports as CSV and is built to feed a SIEM.

**How do I check whether anyone's actually using this, and what it's failing to answer?**

Setup's sibling page, **Usage**, lists every request made against the folder — who asked, what,
whether it was answered, how many citations backed the answer, and latency. Filter to
**Unanswered** to see where the content has real gaps.

---

## 10. How your data is processed

**What actually reads my documents?**

A language model, on every document that comes in. Pomegranate doesn't store your documents as a
pile of files to search later — it reads each one and extracts the individual statements worth
keeping (those are the **nodes** you see in the Library). A model is involved at several points in
that pipeline, not just one.

**Which model, though?**

It depends on which version of Pomegranate you're running.

- **The hosted app** (app.pomegranate.expert) runs **Qwen** by default, served through
  [Together AI's](https://together.ai) OpenAI-compatible endpoint. A deployment can be switched to
  **Anthropic's Claude** instead via a single environment setting. The choice is a launch-time
  configuration, not a per-request one — one provider is active for the whole deployment.
- **The desktop app** runs a model **on your own machine**: Qwen3-1.7B, embedded via llama.cpp, in
  the app's own process. No external daemon, no network call, works fully offline.

Either way, every model call goes through a single seam in the code, so the rest of the product
behaves identically regardless of which backend is active.

**What about the semantic search — is that a model too?**

Yes, a separate and much smaller one. Text is converted into **embeddings** (numeric vectors) so
that "what did we decide about pricing" can find a note that never used the word "pricing." The
hosted app uses OpenAI's `text-embedding-3-small`; the desktop app uses `nomic-embed-text-v1.5`,
again locally through llama.cpp. Embeddings are stored alongside each node.

**What are all the different things the model is used for?**

Roughly a dozen distinct jobs, each with its own purpose-built prompt:

| Stage | What the model does |
|---|---|
| **Routing** | Decides which subfolder(s) a document belongs to, or proposes a new one |
| **Capture** | Extracts the individual statements worth keeping out of the document |
| **Classification** | Types each one against the subfolder's template (task, decision, goal…) |
| **Deduplication** | Judges whether a new statement restates, updates, or supersedes an existing one |
| **Glean** | Second pass to recover content the first capture missed |
| **Edge inference** | Works out how nodes relate to each other |
| **Query** | Answers your questions from the nodes, with citations |
| **Review** | Checks a draft against what's currently held and returns red/yellow/green findings |
| **Wiki & reports** | Composes readable pages from the underlying nodes |
| **Media reading** | Transcribes audio and reads images into text |
| **Agents** | Powers Ask the team, Get updates, the surface bots, and source instructions |

**Is my content used to train anyone's model?**

Your content is sent to the configured provider only to produce the result for that specific call —
extracting nodes, answering your question. On the desktop app, nothing leaves your machine at all
until you choose to sync.

**Is there a record of what the model was asked to do?**

Yes. Every model call appends a line to an internal call log recording who, what, which task, which
prompt version, token counts, and latency — but deliberately **not** the prompt body or your
verbatim text. It exists for cost and reliability monitoring, not content retention.

---

## 11. Where your data is stored

**Where do my actual files end up?**

Two different places, by type:

- **Documents, files, and media** — the originals you upload or that get pulled in — are kept in
  **file storage**, as files.
- **Nodes** — the extracted snippets of information, which is what questions actually get answered
  from — are kept in a **database**, together with their embeddings, their links to each other, and
  the citation back to the document they came from.

That split is why deleting a subfolder removes its nodes but not the underlying document (see
[§4](#4-organizing-renaming-archiving-deleting)) — they're two separate stores.

**And on the desktop app?**

Everything is on your own computer: the sources, the extracted nodes, the database, and the model
doing the extracting. Nothing is on our servers and nothing requires a network connection.

That stays true until **you sync**. Syncing pushes a copy of your local content up to the server
storage — which is what makes it shareable with your team. Until you do that, the desktop app is a
private, self-contained vault; after you do, the synced portion lives in both places.

**So who can technically reach my content on the hosted app?**

Content in the hosted app lives on our servers, and what other *people* can see is governed
entirely by the audience level on each note (<a href="#7-controlling-who-sees-what">§7</a>) — "Only
me" content is not visible to teammates or their AI agents. Every folder's data is isolated from
every other folder's, enforced on every single query.

---

## 12. How your data gets in

There are five routes in. All of them require you to do something deliberate — nothing is ingested
passively.

**1 — You add it directly.** Upload a file, paste text, or drop a link in **Add sources**. The most
direct path, and the one with the most control: you can pin the destination subfolder and attach
instructions.

**2 — An AI agent adds it for you.** With Pomegranate connected to Claude (or another MCP client),
the assistant can file something into your folder — but only when you **ask it to, explicitly**. It
needs a clear instruction along the lines of "add this to Pomegranate." It does not watch your
conversation and file things on its own initiative; an ordinary chat doesn't end up in your folder
as a side effect.

**3 — A connected third-party app.** Gmail, Slack, Drive, Notion, GitHub, Jira, Teams, Fathom.
These connect through **[Composio](https://composio.dev)**, a platform that specializes in
custodying OAuth connections to third-party apps. Practically, this means Pomegranate never
registers its own OAuth client with each provider and never holds your live access tokens — you
authorize on the app's own consent screen, Composio holds the connection, and Pomegranate works
through a reference to it. Pulls are either one-off or on a schedule you set
(<a href="#6-automating-what-comes-in">§6</a>).

**4 — The Chrome extension.** Save a selection, a whole page, or an image into your folder from
wherever you are, and ask or review the current page against your team's context without leaving
the tab. It connects with a token issued from the web app.

The extension is currently unlisted: the install link only works for accounts Pomegranate has
enlisted, so ask to be added before installing — otherwise the link appears to do nothing.

**5 — WhatsApp.** Save the Pomegranate number — **+1 510 697 6636** — in your contacts, then
message it **directly, one-to-one** from the phone number linked to your account, and whatever you send — text, a voice note, an image — is handled the same
way as anything else. Link your number first under **Setup → Your profile**, or the bot won't know
who you are.

> **Not yet supported:** adding the Pomegranate number to a **group chat**. Group messages are
> currently declined with an "unsupported" reply rather than ingested. One-to-one only for now.

---

## 13. Removing your data

**How do I delete one specific thing?**

Open the Library, find the node, and delete it — you'll be asked to confirm. This removes that one
statement from the graph, so it stops being used to answer questions.

Note the difference from *superseding*: writing a correction archives the old version but keeps it
readable in history (<a href="#2-the-mental-model">§2</a>). Deleting removes it. If your goal is
"this must not be here anymore," delete it; if your goal is "this is no longer true," just write
the correction.

**How do I remove a whole subfolder's worth?**

Deleting a subfolder permanently removes its nodes, candidates, edges, and wiki pages — see
<a href="#4-organizing-renaming-archiving-deleting">§4</a>. Archiving, by contrast, hides it while
keeping everything.

**How do I remove everything?**

Delete the folder. That removes every graph node, candidate, review, source, MCP connection token,
audit row, and uploaded file belonging to it. It's logged immediately before it runs, you're signed
out of the folder right after, and it cannot be undone.

**What about the things attached to my account rather than to a folder?**

Those are revoked separately and are worth doing as their own pass: disconnect third-party apps
under **Setup → Integrations → Connected apps**, and revoke connector URLs and connection tokens
under **Setup → Integrations**. Disconnecting an app stops future pulls but does not retroactively
remove documents it already brought in — delete those separately if you want them gone.
