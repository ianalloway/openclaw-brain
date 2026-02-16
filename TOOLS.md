# TOOLS.md - Model Inventory & Connections

_Your AI system architecture — what models you use, how they connect, and what you spend._

## Model Inventory

| Model/Tool | Purpose | Subscription/Access | Monthly Cost |
|------------|---------|---------------------|--------------|
| MiniMax 2.5 | Primary reasoning, coding, general tasks | API key | $10 |
| OpenAI GPT-4o | Fallback for reasoning/tasks | API key (new) | Pay per use |
| Kimi kf | Cloud tasks, heavy compute, fallback when local down | API key | ~$10 |
| Kimi Cloud | Spawn agents / run when local gateway is down | Installed | — |
| Perplexity | Web search and research | API key (Pro) | — |
| Claude | Fallback / specific tasks | API key | $20 |
| OpenRouter | Secondary fallback | API key | Free tier |

## Model Rotation Strategy

| Task Type | Primary | Fallback |
|-----------|---------|----------|
| General reasoning | MiniMax 2.5 | OpenAI → Kimi → Claude |
| Coding | MiniMax 2.5 | OpenAI → Kimi → Claude |
| Web search / Research | Perplexity | Kimi → MiniMax |
| Job applications | MiniMax 2.5 | Kimi → Claude |
| Background / heartbeat | MiniMax 2.5 | OpenRouter |

## Subscriptions & Access

- **MiniMax:** Primary model ($10/month)
- **Claude:** Secondary ($20/month)
- **OpenRouter:** Fallback
- **Philosophy:** Try free first, upgrade when needed

## AI Domain Coverage (from Muscles)

| Domain | Current Use | Needs Help With |
|--------|-------------|-----------------|
| Creative | None yet | Image, video, audio |
| Coding/Engineering | Yes | All of it |
| Writing | — | All (copy, research, marketing, email) |
| Design | — | All (UI/UX, logos, presentations) |
| Communication | — | All (email, chat, calendar, support) |
| Business | — | All (PM, CRM, accounting) |
| Data | — | Spreadsheets, analytics, trading |
| Productivity | — | All |
| Media | — | All (voice, transcription, translation) |

## Instructions

- Always check skills for updates and new capabilities
- Use free tools where possible
- MiniMax → Claude → OpenRouter as fallback chain

---

## MCP & Connections

| Server/Tool | Purpose | Connected To | Data Flow |
|-------------|---------|--------------|-----------|
| (To be mapped) | | | |

## Budget

- **Monthly spend:** ~$30
- **Philosophy:** Free first, then paid

---

_Update this as we learn more about your AI usage._
