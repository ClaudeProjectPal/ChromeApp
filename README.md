# Claude Project Pal 🤝

**Bulk upload zip files into Claude.ai project knowledge. Stop adding files one at a time.**

By [Daniel Boutros](https://buymeacoffee.com/soularcade) @ Soul Arcade

---

## The Problem

Claude.ai's project knowledge is powerful — but loading it is painful. The interface makes you upload files one at a time. No bulk upload. No folder support.

## The Fix

Drop a zip. Walk away.

Claude Project Pal extracts every text file from your zip and uploads them directly to your Claude project using Claude.ai's own API — authenticated by your existing session. No API keys. No new accounts.

## Install

[**→ Install from the Chrome Web Store**](https://chrome.google.com/webstore/detail/claude-project-pal)

Or load unpacked in developer mode:
1. Download this repo as a zip and extract it
2. Go to `chrome://extensions`
3. Enable Developer mode
4. Click "Load unpacked" → select the folder

## Supported File Types

`.md` · `.txt` · `.py` · `.json` · `.csv` · `.html` · `.yaml` · `.yml` · `.xml` · `.rst`

## How It Works

1. Navigate to a Claude.ai project page
2. Click the extension icon
3. Drop your zip file onto the panel
4. Hit Upload — done

The extension reads your `lastActiveOrg` cookie and project ID from the URL, then POSTs each file as JSON to Claude.ai's internal docs API. Your session cookie handles authentication automatically.

## Version Monitoring

The extension checks `version.json` in this repo on every popup open. If Claude.ai changes their API in a way that breaks uploads, update this file to alert all users immediately:

```json
{
  "version": "2.1.0",
  "api_broken": true,
  "api_broken_msg": "Claude.ai changed their API on [date] — update required"
}
```

## Privacy

No data collected. No tracking. No analytics. Files go from your browser directly to Claude.ai — nowhere else. Full privacy policy at [ClaudeProjectPal.github.io/ClaudeProjectPal/privacy](https://claudeprojectpal.github.io/ChromeApp/privacy.html).

## Support

Found a bug? [Open an issue](https://github.com/ClaudeProjectPal/ChromeApp/issues)

Find this useful? [Buy Daniel a coffee ☕](https://buymeacoffee.com/soularcade)

---

*Not affiliated with or endorsed by Anthropic.*
