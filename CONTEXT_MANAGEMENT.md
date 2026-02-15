# CONTEXT_MANAGEMENT.md - Token Audit & Efficiency

## TOKEN AUDIT

| File/Directory | Est. Tokens | Loads When |
|----------------|-------------|------------|
| AGENTS.md | ~3,000 | Every session |
| SOUL.md | ~750 | Every session |
| USER.md | ~500 | Every session |
| HEARTBEAT.md | ~650 | Heartbeat only |
| TOOLS.md | ~400 | When needed |
| IDENTITY.md | ~150 | Every session |
| memory/2026-02-15.md | ~550 | Main session |
| memory/2026-02-13.md | ~500 | When read |
| memory/2026-02-12.md | ~300 | When read |

**Total baseline (fresh session):** ~5,500 tokens

## CONTEXT PROFILES

| Agent Type | Required Files | Optional Files | Max Budget |
|------------|---------------|----------------|------------|
| Main session | SOUL, USER, IDENTITY, AGENTS | Memory (today) | 50% of context |
| Heartbeat | HEARTBEAT, AGENTS | — | 20% of context |
| Sub-agent | AGENTS only | — | 30% of context |

## CONVERSATION WINDOWING

- **Keep last:** 10 message pairs raw
- **Summarize:** Older turns into compressed block
- **Trigger:** When history exceeds 15,000 tokens

## BUDGET GUARDRAILS

| Threshold | Action |
|-----------|--------|
| 50% context used | Warning (log only) |
| 75% context used | Auto-summarize oldest messages |
| 90% context used | Hard stop - clear old sessions |

## SESSION HYGIENE

- Clear sessions older than 7 days
- Archive important context to memory/*.md before clearing
- Check session size during heartbeats

## EFFICIENCY RULES

- Load only what's needed per session type
- Don't load all memory files — just today + yesterday
- Skills load on-demand only

---

Review this context architecture. What's wrong or missing? This becomes how your AI manages its own cognitive load.
