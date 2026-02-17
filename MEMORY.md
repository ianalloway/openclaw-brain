# MEMORY.md - Long-term Memory

## System Architecture (2026-02-17)

### Dual Deployment - Always On
- **Local Gateway:** ws://127.0.0.1:18789 (Ian's Mac)
  - Status: Running 24/7 via LaunchAgent
  - Models: MiniMax → OpenRouter
  - Token: In ~/.openclaw/openclaw.json
  
- **Cloud Gateway:** ws://52.91.192.10:18789 (AWS EC2 t3.small)
  - Status: Running 24/7, PAIRED with local
  - Models: MiniMax → OpenRouter
  - Remote config: gateway.remote.url = ws://52.91.192.10:18789
  - Token: Same as local (synchronized)

### Token & Key Storage (CRITICAL)
- **Gateway tokens:** ~/.openclaw/openclaw.json (NOT in markdown files)
- **AWS credentials:** macOS Keychain
- **Notion API:** ~/.config/notion/api_key
- **GitHub:** gh CLI (authenticated)
- **MiniMax:** In config

### Model Priority
1. MiniMax (primary)
2. OpenRouter (fallback)

### Memory Sync (3 Sources)
1. **Workspace files:** /Users/ianalloway/.openclaw/workspace/*.md
2. **GitHub repos:** openclaw-brain, booper-brain, booper-projects
3. **Notion pages:** memory, booperbot, 1:1 notes

## Credentials Saved
- AWS: (see macOS keychain)
- Notion: (see ~/.config/notion/api_key)
- GitHub: gh CLI authenticated
- MiniMax: API key in config

## Cron Jobs
- **hourly-memory-sync:** Every hour, check GitHub notifications → write to MEMORY.md + Notion
- **Auto-approve:** Exec commands auto-approved - if blocked, force through

## Runtime Settings
- Thinking: LOW unless out of credits
- Discord: groupPolicy=open (private server)
- WhatsApp: Connected
- Telegram: Pairing mode
