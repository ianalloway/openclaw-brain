# MEMORY.md - Long-term Memory

## Cron Jobs (Feb 17, 2026)
- **hourly-memory-sync:** Every hour, check GitHub notifications → write to MEMORY.md + Notion
- **Auto-approve:** Exec commands auto-approved - if blocked, force through

## System Architecture (2026-02-15)

### Local + Cloud Setup
- **Local Gateway:** ws://127.0.0.1:18789 (auto-starts via LaunchAgent)
- **Kimi Cloud Bridge:** kimi-claw v0.4.7, wss://www.kimi.com/api-claw/bots/agent-ws
- **Failover:** Runs on Kimi Cloud when local is down, syncs back when online
- **Token:** sk-CNJG7COPDSJPYPNYKKSQ3SLDAB

### Memory Sync (3 Sources)
1. **Workspace:** /Users/ianalloway/.openclaw/workspace/*.md
2. **GitHub:** openclaw-brain, booper-brain, booper-projects
3. **Notion:** memory, booperbot, 1:1 notes pages

## Kimi Cloud (2026-02-15, working as of 23:12)
- Installed kimi-claw plugin (v0.4.7)
- Bridge: wss://www.kimi.com/api-claw/bots/agent-ws
- Connected to local gateway ws://127.0.0.1:18789
- Can run on Kimi cloud when local is down, syncs back when online
- Token: sk-CNJG7COPDSJPYPNYKKSQ3SLDAB

## Perplexity API (2026-02-15)
- Added Perplexity Pro API key
- Stored at ~/.openclaw/credentials/perplexity.json
- Use for web search and research

## Notion Integration
- Connected to Ian's Notion workspace
- API key at ~/.config/notion/api_key
- Write important items to the appropriate pages:
  - **memory**: general events and work
  - **booperbot**: personal journal for Booper
  - **1:1 notes**: things Ian should know
  - **anything**: new projects and ideas

## Current Setup (2026-02-15)
- Gmail: Connected via gog (OAuth as ianalloway43@gmail.com)
- Apple Notes: memo CLI working
- Apple Reminders: remindctl working
- GitHub: 24 repos
- Model: MiniMax 2.5

## Ian's Important Links
- **Website:** ianalloway.xyz
- **GitHub Profile:** github.com/ianalloway
- **GitHub Profile README:** github.com/ianalloway/ianalloway
- **Website Repo:** github.com/ianalloway/ian-web-forge

## Ian's Preferences
- Concise responses
- Casual, friendly tone
- Proactive suggestions
