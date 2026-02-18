# TOOLS.md - Model Inventory & Connections

_Your AI system architecture — what models you use, how they connect, and what you spend._

## Music Preferences
- **YouTube Music** - Ian's subscription, open via browser at https://music.youtube.com
## Model Priority

| Priority | Model | Purpose | Cost |
|----------|-------|---------|------|
| 1 | MiniMax 2.5 | Primary - all tasks | $10/mo |
| 2 | MiniMax 2.5 (#2) | Secondary when primary hits limit | $10/mo |
| 3 | Kimi (Moonshot) | Backup when MiniMax limited | Free/trial |
| 4 | OpenRouter | Last resort | Free tier |

**CRITICAL:** Always use MiniMax first. If rate limited → MiniMax #2 → Kimi → OpenRouter. **NEVER STOP. ALWAYS ROTATE.**

## Research - ALWAYS USE PERPLEXITY
- Use **Perplexity** for ALL web searches and research
- It's better than regular search
- Default to Perplexity for any research task

## Model Rotation Strategy

| Task Type | Primary | Fallback |
|-----------|---------|----------|
| General reasoning | MiniMax 2.5 | Kimi → OpenRouter |
| Coding | MiniMax 2.5 | Kimi → OpenRouter |
| Web search / Research | Perplexity | MiniMax |
| Job applications | MiniMax 2.5 | Kimi → OpenRouter |
| Background / heartbeat | MiniMax 2.5 | Kimi → OpenRouter |

## Subscriptions & Access

- **MiniMax:** Primary model ($10/month)
- **OpenRouter:** Fallback (free tier)
- **Philosophy:** Try MiniMax first, then free

## Instructions

- Always check skills for updates and new capabilities
- Use free tools where possible
- MiniMax → OpenRouter as fallback chain

---

## MCP & Connections

| Server/Tool | Purpose | Connected To | Data Flow |
|-------------|---------|--------------|-----------|
| Notion | Memory & notes | API key: ~/.config/notion/api_key | Read/write pages |
| GitHub | Code & config sync | gh CLI | Push/pull repos |

## Notion API Usage

**Setup:**
```bash
npm install -g @notionhq/client
export NOTION_API_KEY="ntn_..."
```

**Pages:**
- **memory** (id: 30837181-e092-80dd-9e4a-f0ea0e51090a): general memory
- **booperbot** (id: 30837181-e092-80f3-8acf-cfd93ee9ed28): personal journal
- **1:1 notes** (id: 30837181-e092-80ba-a385-d853352c34c3): what Ian should know

**Tool:** Use `notion` skill - read skill file at /opt/homebrew/lib/node_modules/openclaw/skills/notion/SKILL.md

## Budget

- **Monthly spend:** ~$10
- **Philosophy:** MiniMax first, then free

---

_Update this as we learn more about your AI usage._
