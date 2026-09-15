# Typical new-user access email

This is the structure used by the user-admin skill after an account, workspace, and connector have been provisioned. Values in braces are replaced with the recipient's actual details; they are not random placeholders in a sent email.

**Subject:** Your Pomegranate access

```text
Hi,

You're set up on Pomegranate.

Get started with Claude or ChatGPT
Copy and paste the prompt below into a new conversation in Claude or ChatGPT. Your AI assistant will guide you through setup, help you choose useful ways to use Pomegranate, and help you import your first data with your approval.

--- COPY FROM HERE ---
Start my Pomegranate onboarding. Fetch and follow this getting-started skill:
https://timegenius0.github.io/pomegranate-onboarding/v1/getting-started.md

Email: {recipient email}
Phone: {registered WhatsApp phone, if present}
MCP link: {recipient's provisioned connector URL}
--- END OF PROMPT ---

Prefer to get set up yourself?
Follow the instructions below instead:

1. Sign in to the app
Go to https://app.pomegranate.expert and log in with this email ({recipient email}) via the normal sign-in flow.

Your workspace "{workspace name}" ({workspace id}) is already created and ready to use.

2. Connect Pomegranate to Claude.ai
In claude.ai, go to Settings -> Connectors -> Add custom connector, and paste this link:

{recipient's provisioned connector URL}

You won't need to select an authentication method or fill in any auth fields -- just paste the link and add it.

3. Ingesting and querying data from Claude
Once the connector is added, just talk to Claude normally in claude.ai:
- To add something: ask Claude to save or ingest it, e.g. "Add this doc to Pomegranate" or paste in notes/text and say "ingest this." It gets routed to the right folder automatically.
- To ask a question: just ask, e.g. "What does Pomegranate say about X?" -- Claude will answer from your workspace's current content and cite the specific notes it used.
- You can also ask Claude to list your folders, pull up recent changes, or check a draft against what's already tracked before you ship it.

Let me know if you run into any trouble getting in.

-- Pomegranate-user-admin Agent, on behalf of Bilel
```

If no WhatsApp phone is registered, omit the `Phone:` line rather than inventing one.
