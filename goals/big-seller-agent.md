# Big Seller E-commerce Agent

**Created:** 2026-05-08
**Goal:** Build an AI agent that can manage BigSeller e-commerce operations via browser automation

## Capabilities (Target)

### Interactive / On-demand Queries
- [ ] Show orders from Shopee today that have issues
- [ ] Query SKU sales performance (this week vs last week)
- [ ] Find products with stock below threshold
- [ ] Compare Lazada vs Shopee revenue this month
- [ ] Show all refunded orders

### Conversational Analysis
- [ ] Analyze sales drop — "Why did sales drop this week? Look at trends"
- [ ] Restock recommendations based on velocity
- [ ] Pattern detection in cancelled orders

## Implementation Steps

### Phase 1: Browser Automation Setup
- [x] Copy Brave profile for big-seller agent (port 9226)
- [ ] Fix captcha solving (manual login or captcha service)
- [ ] Verify session persistence (cookies work after restart)

### Phase 2: BigSeller Login
- [ ] Complete login with captcha solving
- [ ] Save session cookies
- [ ] Verify agent can access dashboard

### Phase 3: Core Features
- [ ] Navigate to order management
- [ ] Query today's orders
- [ ] Generate sales report
- [ ] Stock level monitoring

### Phase 4: Advanced
- [ ] Cross-platform revenue comparison
- [ ] Order issue detection
- [ ] Automated daily reports to Telegram

## Tech Stack
- **Browser:** Brave on CDP port 9226 (big-seller profile)
- **Automation:** Playwright via CDP
- **Agent:** OpenClaw big-seller agent
- **Platform:** BigSeller (aggregates Shopee, Lazada, TikTok, etc.)
- **Session:** Agent账号 pinky.dressy@gmail.com

## Blockers
- CAPTCHA on login — needs captcha solving solution or manual session save

## Notes
- BigSeller has image captcha on every login
- No direct API available — browser automation is the only way
- Consider 2Captcha API (~$0.003/captcha) for automated login

---

## Why This Agent? (Original Vision)

Here's what an OpenClaw e-commerce agent could do that cron jobs can't:

### Interactive / On-demand queries:
- "Show me orders from Shopee today that have issues"
- "Which SKU sold the most this week vs last week?"
- "Find products with stock below 10"
- "Compare Lazada vs Shopee revenue this month"
- "Show me all refunded orders"

### Conversational analysis:
- "Why did sales drop this week? Look at trends"
- "Which products should I restock based on velocity?"
- "Is there a pattern in cancelled orders?"

### Decision-making assistance:
- "Should I raise price on PNK047 based on demand?"
- "Which listings need optimization?"
- "What's my profit margin after fees for this order?"

### Real-time actions:
- Update stock levels directly
- Reply to customer messages
- Create product listings
- Process bulk order updates

### What it looks like:
- You chat with the agent like you chat with me
- Agent queries BigSeller API, analyzes data
- Returns insights, recommendations, or takes action
- Remembers your business context over time

---

## Comparison: Cron vs Agent

| Task | Cron (report) | OpenClaw Agent |
|------|---------------|----------------|
| Daily order list | ✅ | ✅ |
| Weekly sales summary | ✅ | ✅ |
| "Why are sales down?" | ❌ | ✅ |
| "Compare 3 products" | ❌ | ✅ |
| "Update stock for SKU X" | ❌ | ✅ |
| Interactive Q&A | ❌ | ✅ |

**You only need the agent if you want to ask questions and get answers, not just receive scheduled reports.**

