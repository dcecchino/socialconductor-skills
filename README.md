# SocialConductor Skills for Claude

Control your [SocialConductor.AI](https://www.socialconductor.ai) comment automation bots directly from Claude — no browser needed.

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

```bash
claude plugin marketplace add https://github.com/dcecchino/socialconductor-skills
claude plugin install socialconductor-plugin@socialconductor-skills
```

---

## Getting Started

1. **Sign up** at [socialconductor.ai](https://www.socialconductor.ai)
2. **Get your API key(s)** from your account settings page on each platform
3. **Set your environment variables:**

```bash
export SC_FB_API_KEY=your_facebook_key        # Facebook / Instagram
export SC_YT_API_KEY=your_youtube_key         # YouTube
export SC_TIKTOK_API_KEY=your_tiktok_key      # TikTok
```

You only need the keys for the platforms you use.

4. **Connect your accounts** — say the connect command for each platform:

```
connect my facebook page
connect my youtube channel
connect my tiktok account
```

New accounts get a **7-day free trial** with up to 30 AI replies per day.

---

## Example Commands

```
check my tiktok bot
pause my facebook bot
show youtube leads
reply to tiktok comment abc123 saying Great video!
block @spammer123
show stale youtube videos
turn on viral intelligence
```

---

## Support

- 📧 support@socialconductor.ai
- 🌐 [socialconductor.ai](https://www.socialconductor.ai)
