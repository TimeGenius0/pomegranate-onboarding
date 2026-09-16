# Typical new-user access email

This is the structure used by the user-admin skill after an account, workspace, and connector have been provisioned. Values in braces are replaced with the recipient's actual details; they are not random placeholders in a sent email.

**Subject:** Your Pomegranate access

```text
Hi,

You're set up on Pomegranate. Your workspace "{workspace name}" is ready.

GET STARTED WITH CLAUDE OR CHATGPT (about 5 minutes)

Step 1 - Connect Pomegranate to your AI assistant
Claude: go to claude.ai -> Settings -> Connectors -> Add custom connector, and paste this link:

{recipient's provisioned connector URL}

There's no authentication method to pick and no fields to fill in: just paste the link and add it.
ChatGPT: add the same link as a custom connector in ChatGPT's settings (this needs a plan that supports custom connectors / developer mode).

Step 2 - Open a new conversation
Start a fresh chat and make sure the Pomegranate connector is switched on for it (in the chat's tools / connectors menu).

Step 3 - Ask your assistant to set you up
Copy the message below into that new conversation:

--- COPY FROM HERE ---
Hi! I've just signed up for Pomegranate and connected its connector. Could you help me set it up? Pomegranate's setup guide is at https://pomegranate.expert/onboarding/v1/getting-started.md - please use it as a reference while you walk me through choosing how I'll add data, suggesting a few folders that would be useful for my work, and importing a first batch with my approval.
My account email is {recipient email}.
My WhatsApp number is {registered WhatsApp phone}.
--- END ---

PREFER THE WEB APP?
Go to https://app.pomegranate.expert and sign in with {recipient email}. Your workspace "{workspace name}" ({workspace id}) is already there.

USING POMEGRANATE FROM CLAUDE OR CHATGPT
Once the connector is added, just talk to your assistant normally:
- To add something: ask it to save or ingest it, e.g. "Add this doc to Pomegranate", or paste in notes and say "ingest this." It gets routed to the right folder automatically.
- To ask a question: just ask, e.g. "What does Pomegranate say about X?" It answers from your workspace's current content and cites the notes it used.
- You can also ask it to list your folders, pull up recent changes, or check a draft against what's already tracked before you ship it.

Let me know if you run into any trouble getting in.

-- Pomegranate-user-admin Agent, on behalf of Bilel
```

If no WhatsApp phone is registered, omit the "My WhatsApp number is…" line rather than inventing one.

The connector link appears only in Step 1, never inside the message users paste. A pasted secret plus "fetch and follow this skill" reads like prompt injection and makes assistants refuse or hedge.
