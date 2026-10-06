# Email Assistant

Read what matters. Write what you mean. Keep the reply short.

Find an old message, catch up on a conversation, turn rough notes into a clear email, or send a reply with the right attachments. Email Assistant helps with each step through the mail tools already available to your assistant.

- **Read and find:** search correspondence, summarize threads, and pull out requests and deadlines.
- **Write and reply:** draft, shorten, or translate emails while keeping the facts and your intended tone.
- **Send and attach:** check recipients, include the right files, and keep replies in the original conversation.
- **Organize:** label, archive, or otherwise handle a selected set of emails when you ask.
- **Follow up:** identify unanswered requests and create reminders or scheduled sends when you request them and suitable tools are available.

Writing starts with the point. A quick reply stays quick; a detailed request keeps the information the recipient needs. Greetings and sign-offs follow the conversation rather than a fixed template.

## Try it

```text
Use $email-assistant to summarize this thread and tell me what needs a reply.
```

```text
Use $email-assistant to turn these notes into a short email. Keep the dates and amounts.
```

```text
Use $email-assistant to reply in the same thread and attach these two files.
```

## Setup

Place the `email-assistant` folder in your assistant's skill directory. The skill uses the standard `SKILL.md` format; optional display metadata is included for Codex. Invoke it as `$email-assistant`, or let a host that supports automatic skill selection choose it for an email task.

Drafting works without a mailbox connection. Searching, sending, organizing, reminders, and scheduled sends depend on the authorized tools available in your environment. This skill supplies instructions, not an email account, mail server, or background service.

## 中文

**邮件助手：读邮件、抓重点、写回复、带附件发送；简短清楚，不绕弯子。**

可以帮你查找往来邮件、概括一段对话、列出需要回复的问题和截止日期，也能把零散想法写成邮件、翻译或改短已有草稿。需要发送时，核对收件人、链接和附件；继续原话题时，接着原邮件回复。

你也可以要求它整理指定邮件，或设置提醒和定时发送。这些操作需要相应的邮箱或日程工具。只让它读信或写草稿时，不会自动发信、转发或清理邮箱。

## Privacy

The package contains general instructions only. It includes no real correspondence, contacts, account details, or personal attachments. Private mail stays within the task and the tools you authorize.

## License

Source available under **PolyForm Noncommercial 1.0.0**. Noncommercial use is permitted under the license; commercial use requires separate written permission from the copyright holder. This is not an OSI-approved open-source license. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
