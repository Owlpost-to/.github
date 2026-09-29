<p align="center">
  <img src="https://raw.githubusercontent.com/Owlpost-to/.github/main/assets/org-banner.png" alt="Owlpost. Email for apps and agents. Send, receive, and give your agents an inbox, behind one API." width="100%">
</p>

<p align="center">
  <a href="https://owlpost.pages.dev"><img src="https://img.shields.io/badge/SITE-LIVE-F4B63F?style=for-the-badge&labelColor=0E1526" alt="Site: live"></a>
  <img src="https://img.shields.io/badge/API-PLANNED-8A93A6?style=for-the-badge&labelColor=0E1526" alt="API: planned">
  <a href="https://factory0.ventures"><img src="https://img.shields.io/badge/FACTORY%20ZERO-VENTURE-E3E6EC?style=for-the-badge&labelColor=0E1526" alt="A Factory Zero venture"></a>
</p>

<p align="center">
  <sub>
    <a href="https://owlpost.pages.dev">Site</a> &nbsp;·&nbsp;
    <a href="https://owlpost.pages.dev/#pillars">Products</a> &nbsp;·&nbsp;
    <a href="https://owlpost.pages.dev/#pricing">Pricing</a> &nbsp;·&nbsp;
    <a href="https://owlpost.pages.dev/llms.txt">llms.txt</a>
  </sub>
</p>

---

## Email for apps and agents.

One API for every email your product touches. Send it, receive it, or hand an agent its own address.
Same key, same logs, same webhooks.

---

## Two things, and which is which

This matters more than anything else on this page, so it is first.

| | What it is | Status |
| :--- | :--- | :--- |
| **Site** | [owlpost.pages.dev](https://owlpost.pages.dev): the landing page, `llms.txt`, the Open Graph card. | `LIVE` |
| **Owlpost** | The product: sending, inbound parsing, agent inboxes, templates, SDKs, CLI, MCP server. | `PLANNED` |

Nothing below is public yet. There is no package on npm or PyPI, no API key to sign up for, and no
price charged anywhere.

Two labels are used everywhere, and they govern the tense of the sentence around them:

- `LIVE`: deployed and reachable.
- `PLANNED`: designed, not public.

---

## Three products, one key

| Product | What it does | Status |
| :--- | :--- | :--- |
| **Send** | Transactional and marketing email from one SDK, with templates, scheduling and a timeline per message | `PLANNED` |
| **Receive** | Inbound email parsed to JSON (bodies, headers, attachments) and posted to your webhook | `PLANNED` |
| **Agent Inboxes** | Persistent addresses on owlpost.to or your own domain, with threads, search, real-time events and inbound screening | `PLANNED` |

```js
const inbox = await op.inboxes.create({ name: 'support-agent' });
// → support-agent@owlpost.to

op.inboxes.on('message.received', async (msg) => {
  const reply = await agent.run(msg.text);
  await op.messages.reply(msg.id, { text: reply });
});
```

<sub>The API as designed. Not published.</sub>

---

## The plan

| Plan | Emails a month | Agent inboxes | Price |
| :--- | ---: | ---: | ---: |
| Free | 5,000 | 3 | $0 |
| Starter | 50,000 | 10 | $12 |
| Growth | 200,000 | 100 | $49 |
| Scale | 1,000,000 | 1,000 | $249 |

Unlimited domains and contacts on every plan; charged per email sent, never per contact. `PLANNED`:
nothing is charged today.

---

## Repositories

| Repo | What it is |
| :--- | :--- |
| **website** | owlpost.pages.dev: static HTML, no build step, Cloudflare Pages. Private |
| **.github** | This page and the mark |

<p align="center">
  <br>
  <a href="https://owlpost.pages.dev"><b>owlpost.pages.dev</b></a>
  &nbsp;·&nbsp;
  a <a href="https://factory0.ventures">Factory Zero</a> venture
</p>

<p align="center">
  <sub>Email for apps and agents.</sub>
</p>
