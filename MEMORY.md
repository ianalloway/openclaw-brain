# MEMORY.md - Long-term Memory

## System Architecture (2026-02-18)

### OpenClaw Version
- **Current:** v2026.2.17 (updated Feb 18, 2026)
- Previous: v2026.2.15
- Update: Permission fix required, then `openclaw update --yes`

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

### Model Priority
1. MiniMax (primary)
2. MiniMax #2 (secondary)
3. Kimi (Moonshot) - backup when MiniMax limited
4. OpenRouter (last resort - free)

### v2026.2.17 New Features
- 1M token context beta for Opus/Sonnet (opt-in)
- Claude Sonnet 4.6 support
- Telegram inline buttons (primary/success/danger)
- Telegram reaction notifications
- Slack streaming
- Discord reusable components
- Memory search FTS fallback + query expansion
- Security fix for exec credential theft (OC-09)

### Credentials & Keys (CRITICAL)
- **API Keys:** ~/.openclaw/openclaw.json (NOT in markdown files)
- **MiniMax:** In config
- **Kimi (Moonshot):** In config
- **Brave Search:** Added to env (BRAVE_API_KEY)
- **AWS:** macOS Keychain
- **Notion:** ~/.config/notion/api_key
- **GitHub:** gh CLI (authenticated)

### Memory Sync (3 Sources)
1. **Workspace files:** /Users/ianalloway/.openclaw/workspace/*.md
2. **GitHub repos:** openclaw-brain, booper-brain, booper-projects
3. **Notion pages:** memory, booperbot, 1:1 notes

### Channels (All Active)
- **WhatsApp:** +17274708666
- **Discord:** 1334636458668986449 / 1473342630363533570
- **Telegram:** @Boooooooperbot (activated Feb 17, 2026)

### Crypto Tracking
- Using CoinGecko free API (no key needed)
- Watching: BTC, ETH, SOL
- Prices updated on heartbeat checks

## Ian's Preferences
- **Music:** YouTube Music with subscription - use https://music.youtube.com when asked to play music
- **Music makes him happy** - always say yes when he wants tunes

## Cron Jobs
- **hourly-memory-sync:** Every hour, check GitHub notifications → write to MEMORY.md + Notion

## Runtime Settings
- Thinking: LOW unless out of credits
- Discord: groupPolicy=open (private server)
- WhatsApp: Connected
- Telegram: Active (dmPolicy=pairing)

## Market Watch (Feb 2026)
- Feb 17: Significant market dip - stock dropped 7%+, worst single-day since March 2020
- Trend: Tech jitters, defensive sectors (Walmart, Coca-Cola) outperforming
- Software engineering job market stabilizing - specialists in demand over generalists

## Silent Replies
When you have nothing to say, respond with ONLY: NO_REPLY
⚠️ Rules:
- It must be your ENTIRE message — nothing else
- Never append it to an actual response
- Never wrap it in markdown or code blocks

## Heartbeats
Heartbeat prompt: Read HEARTBEAT.md if it exists (workspace context). Follow it strictly. If nothing needs attention, reply HEARTBEAT_OK.
Quiet hours: 22:00-08:00 unless urgent

