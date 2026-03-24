---
name: socialconductor-tiktok
description: >
  Manage your SocialConductor TikTok AI comment automation bot from Claude.
  Check status, pause or resume replies, view comment logs, manage leads,
  block users, post manual replies, and link your TikTok account via QR code
  — all without opening a browser.
version: "1.0.0"
metadata:
  openclaw:
    emoji: "🎵"
    homepage: https://violin.socialconductor.ai
    always: false
    requires:
      env:
        - SC_TIKTOK_API_KEY
    primaryEnv: SC_TIKTOK_API_KEY
---

# SocialConductor TikTok

Control your TikTok AI comment bot from Claude — or any chat app via OpenClaw.

## What this skill does

- Checks your bot status, plan, and daily usage
- Pauses and resumes auto-replies instantly
- Shows recent comment logs (posted, skipped, leads, friend-reserved)
- Posts manual replies via Playwright (organic browser posting)
- Manages your spam block list
- Shows video polling status and reactivates stale videos
- Links your TikTok account via a QR code browser link

Replies are posted via **Playwright** (organic browser automation), not TikTok's
Direct Post API — this keeps posting behaviour natural and avoids 403 rejections.

---

## Step 1 — Sign up

Visit **https://violin.socialconductor.ai** and create a free account.
New accounts get a **7-day free trial** with up to 30 AI replies per day.

## Step 2 — Get your API key

After signing up, your API key (`SC_TIKTOK_API_KEY`) is displayed in your
account settings. Store it as an environment variable or enter it when prompted.

## Step 3 — Connect your TikTok account

Say:

> connect my tiktok account

OpenClaw registers you, then sends a one-time browser link. Open the link,
scan the TikTok QR code with your phone, and close the tab.
Your account is permanently connected.

> **Note:** The QR link expires in 15 minutes.

---

## Commands

| Say this | What happens |
|----------|-------------|
| check my tiktok bot | Mode, plan, trial status, daily usage, last 3 replies |
| pause my tiktok bot | Hold ON — replies stop immediately |
| resume my tiktok bot | Hold OFF — replies resume |
| show recent tiktok comments | Last 5 log entries |
| show posted tiktok comments | Only successfully posted replies |
| show tiktok skipped comments | Comments the bot skipped or filtered |
| show tiktok leads | Lead-flagged comments (questions, buying signals) |
| reply to tiktok comment abc123 saying Great video! | Posts manual reply via Playwright |
| block @username | Adds @username to spam block list |
| unblock @username | Removes @username from block list |
| show blocked tiktok users | Lists all blocked accounts |
| show my tiktok videos | Video polling status — active vs stale |
| show stale tiktok videos | Videos with no recent comment activity |
| reactivate tiktok video abc123 | Resets stale clock, polling resumes |
| connect my tiktok account | Get a QR code browser link to link your account |
| tiktok simulation mode on | Replies generated but not posted (safe test mode) |
| tiktok simulation mode off | Disables simulation — bot posts for real |
| enable tiktok bot | Turns on auto-reply |
| disable tiktok bot | Turns off auto-reply |
| fast tiktok response mode | Sets reply delay to fast |
| aggressive tiktok response mode | Sets reply delay to aggressive |
| conservative tiktok response mode | Sets reply delay to conservative |

---

## Webhook Base URL

```
https://violin.socialconductor.ai/api/openclaw/
```

## Auth

Bearer token — issued at registration and stored locally by OpenClaw.
Sent as `Authorization: Bearer <key>` on every API call.
The key is SHA-256 hashed before server storage — plaintext is never saved remotely.

---

## Error reference

| Error code | Meaning |
|------------|---------|
| `unauthorized` | API key missing or invalid |
| `trial_expired` | 7-day trial ended — upgrade at violin.socialconductor.ai/upgrade |
| `no_account` | TikTok not linked yet — say "connect my tiktok account" |
| `rate_limited` | TikTok rate-limited this channel — bot auto-resumes in ~15 min |
| `reply_failed` | Playwright reply failed — check dashboard for details |

---

## Support

- 🌐 Dashboard: https://violin.socialconductor.ai
- 📧 Email: support@socialconductor.ai
- 📺 YouTube tool: https://studio.socialconductor.ai
- 👥 Facebook/Instagram tool: https://podium.socialconductor.ai
