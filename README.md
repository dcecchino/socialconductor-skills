# SocialConductor Skills for Claude

Control your [SocialConductor.AI](https://socialconductor.ai) comment automation bots directly from Claude — no browser needed.

## What is SocialConductor?

SocialConductor is an AI-powered comment automation SaaS for TikTok, YouTube, and Facebook/Instagram creators and businesses. The AI reads each comment, understands your video context, and posts intelligent replies automatically — 24/7.

## Supported Platforms

| Platform | Dashboard |
|----------|-----------|
| 👥 Facebook / Instagram | [podium.socialconductor.ai](https://podium.socialconductor.ai) |
| 📺 YouTube | [studio.socialconductor.ai](https://studio.socialconductor.ai) |
| 🎵 TikTok | [violin.socialconductor.ai](https://violin.socialconductor.ai) |

---

## Install

`claude plugin marketplace add https://github.com/dcecchino/socialconductor-skills`
`claude plugin install socialconductor-plugin@socialconductor-skills`

---

## Getting Started

1. **Sign up** at [socialconductor.ai](https://socialconductor.ai)
2. **Get your API key(s)** from your account settings page on each platform
3. **Set your environment variables:**

`export SC_FB_API_KEY=your_facebook_key        # Facebook / Instagram`
`export SC_YT_API_KEY=your_youtube_key         # YouTube`
`export SC_TIKTOK_API_KEY=your_tiktok_key      # TikTok`

You only need the keys for the platforms you use.

4. **Connect your accounts** — say the connect command for each platform:

`connect my facebook page`
`connect my youtube channel`
`connect my tiktok account`

New accounts get a **7-day free trial** with up to 30 AI replies per day.

---

## OpenClaw Enhancements

We've expanded our capabilities with new OpenClaw features, giving you deeper control over your AI responses, detailed analytics, and advanced scheduling directly through the API:

### Drafts & Approvals
* **`GET /api/openclaw/drafts`** — View pending AI replies waiting for review.
* **`POST /api/openclaw/approve_bulk`** — Approve multiple pending replies at once.

### Analytics
* **`GET /api/openclaw/analytics`** — Access daily stats and broader trend data.
* **`GET /api/openclaw/insights`** — Review core performance metrics for your accounts.

### AI Teaching
* **`GET /api/openclaw/examples`** — View your current "star" and "bad" example lists.
* **`POST /api/openclaw/teach`** — Add new teaching examples to train the AI on your preferred tone and style.

### Advanced Features
* **`GET /api/openclaw/friends`** — Access your friend and subscription lists.
* **`POST /api/openclaw/vacation`** — Configure and manage the vacation scheduler.
* **`GET /api/openclaw/viral_vault`** — Explore your top-performing, most viral comments.

---

## Example Commands

You can use natural language to interact with your bots and the new OpenClaw features:

`check my tiktok bot`
`pause my facebook bot`
`show youtube leads`
`reply to tiktok comment abc123 saying Great video!`
`block @spammer123`
`show stale youtube videos`
`turn on viral intelligence`

# New OpenClaw Commands:
`show my pending drafts`
`approve all pending drafts`
`show my daily analytics`
`add this comment to teaching examples`
`turn on vacation mode`
`open the viral vault`

---

## Support

- 📧 support@socialconductor.ai
- 🌐 [socialconductor.ai](https://socialconductor.ai)
