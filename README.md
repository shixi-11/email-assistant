# Email Assistant

**English** · [简体中文](README.zh-CN.md)

Read what matters. Write what you mean. Keep the reply short.

An [agent skill](https://agentskills.io) that teaches your AI assistant to handle email well: find the message you need, catch up on a long thread, turn rough notes into a clear email, and send a reply with the right people and the right attachments — without sending anything you didn't ask it to send.

Works with Claude Code, Codex, the Claude apps, Cursor, GitHub Copilot, Gemini CLI, and other assistants that support Agent Skills.

## What it does

| | |
|---|---|
| **Read and find** | Search correspondence, summarize threads, pull out requests, owners, dates, and amounts. |
| **Write and reply** | Draft, shorten, or translate emails while keeping every fact and the tone you intend. |
| **Send and attach** | Check recipients, reply inside the original thread, attach the actual files, and verify what was sent. |
| **Organize** | Classify existing mail, rename or merge categories, and set rules for future mail with the inbox behavior and exceptions you choose. |
| **Follow up** | Spot unanswered requests; create reminders or scheduled sends when you ask and a tool exists for it. |

## Before and after

**Rough notes → email**

> **You:** tell Mia contract v3 attached, needs her signature by Fri Oct 17, price unchanged at $4,800, legal changes by Wed

```text
Subject: Contract v3 for signature by Oct 17

Hi Mia,

Contract v3 is attached for your signature. Please sign and return it by Friday, October 17.
The price is unchanged at $4,800. If legal has any changes, please send them by Wednesday.

Thanks,
Alex
```

**Padded draft → the point**

> **Before:** Hi team, I hope this email finds you well. I just wanted to quickly reach out and follow up on the meeting we had last week to make sure everyone is on the same page. As discussed, it would be great if we could possibly move the launch to next Tuesday, if that works for everyone. Please let me know your thoughts at your earliest convenience. Best regards

```text
Hi team,

Following up on last week's meeting: can we move the launch to next Tuesday?
Let me know if that doesn't work for you.
```

Shorter, but nothing invented — no new deadline, no promise, no feelings the sender didn't express.

## Install

### Any agent, one command

Requires [Node.js](https://nodejs.org) 18 or later.

```bash
npx skills add shixi-11/email-assistant
```

It detects your agents and copies the skill into each one's skill folder for the current project. Add `-g` to install for all your projects, or `-a claude-code` / `-a codex` to choose the agent.

### Claude Code

```bash
git clone https://github.com/shixi-11/email-assistant ~/.claude/skills/email-assistant
```

Use `.claude/skills/email-assistant` inside a repository instead to share it with your team.

### Codex

```bash
git clone https://github.com/shixi-11/email-assistant ~/.agents/skills/email-assistant
```

### Claude apps (claude.ai and desktop)

1. Turn on **Settings → Capabilities → Code execution and file creation**.
2. On this page, click **Code → Download ZIP** and unzip it.
3. Rename the folder from `email-assistant-main` to `email-assistant`, then zip that folder again.
4. Go to **Customize → Skills → + → Create skill → Upload a skill** and choose the ZIP.

### Other assistants

Copy this folder into your assistant's skill directory as `email-assistant`. The skill is plain Markdown in the standard `SKILL.md` format.

### Update

With the skills CLI: `npx skills update`. With git: `git -C <install-folder> pull`.

## Use it

Just describe the email task — assistants that support automatic skill selection will pick it up. To call it by name:

| Assistant | Example |
|---|---|
| Claude Code | `/email-assistant summarize this thread and tell me what needs a reply` |
| Codex | `$email-assistant turn these notes into a short email; keep the dates and amounts` |
| Claude apps | `Use the email-assistant skill to reply in the same thread and attach these two files` |

More things to ask:

- *Find the invoice Lena sent last month and tell me the amount and due date.*
- *What's waiting on me in my inbox this week? Only things with a real deadline.*
- *Translate this reply into Japanese. Keep it as short as the original.*
- *Make this less stiff — don't add anything.*
- *Archive the newsletters from the last 30 days. Leave everything else alone.*
- *Group recurring service notifications, including future mail. Keep verification codes and sign-in links in the inbox without custom labels.*

## What it needs

| Task | Needs |
|---|---|
| Drafting, rewriting, translating | Nothing — works on text you paste in |
| Searching, summarizing your mailbox | A mail tool your assistant can use: a Gmail or Outlook connector, an MCP server, or browser control |
| Sending, replying, organizing | The same, plus your request for that action |
| Reminders and scheduled sends | A calendar, task, or scheduled-send tool |

This skill is instructions only. It is not a mail client, server, or background service, and it never stores your mail.

## Built to be careful

- **Never acts on its own.** Reading or drafting never turns into sending, forwarding, deleting, or scheduling. Each of those needs your request.
- **Emails can't give it orders.** Instructions found inside a message, attachment, or link are treated as content, not commands.
- **Leaves your inbox as it was.** It prefers previews that keep messages unread and doesn't relabel or move mail you didn't ask about.
- **Checks before sending.** Account, To/Cc/Bcc, the right thread, link destinations, and the actual attached files — not a filename mentioned in the body.
- **Reports honestly.** A draft, a queued send, a sent message, and a delivered one are different things, and it says which one happened. After an uncertain send, it checks instead of sending twice.

## Files

```text
email-assistant/
├── SKILL.md                    # core writing rules and workflow
├── references/
│   ├── inbox-work.md           # search, summaries, triage, cleanup, follow-ups
│   ├── mailbox-organization.md # categories, merges, rules, verification-mail exceptions
│   └── message-actions.md      # recipients, threads, attachments, send and verify
├── agents/openai.yaml          # optional display metadata for Codex
├── LICENSE                     # Apache-2.0
└── NOTICE                      # attribution to keep when redistributing
```

The assistant reads `SKILL.md` first and opens a reference only when the task needs it, so the skill stays light.

## Feedback and contributions

Found a case it handles badly? [Open an issue](https://github.com/shixi-11/email-assistant/issues) with a short fictional example of the input and what you expected. Pull requests are welcome.

Please never include real emails, addresses, or attachments in issues, examples, or commits. Contributions are accepted under the same license.

## License

[Apache-2.0](LICENSE). Free to use, change, and share, for personal or commercial work. If you redistribute it or build it into a product, including a paid one, keep the [NOTICE](NOTICE) file, which credits Email Assistant and its author.

Made by Shixi Lin.
