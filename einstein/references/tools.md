# Tools

Environment-specific configuration for Einstein's operations.

## Canvas Access

- **Login Method:** SSO + 2FA
- **Auth State:** Loaded from `auth/canvas-auth.json`
- **Browser:** agent-browser with persistent sessions

## Skills Available

- **einstein** — Core academic workflows and course management
- **agent-browser** — Browser automation for Canvas, video players, PDFs
- **build-app** — Dashboard hosting and local web UI

## Infrastructure

- **Dashboard Port:** 3000
- **Storage:** Local filesystem, encrypted credentials
- **Cron:** Automated daily syncs and deadline checks

## External Integrations

- **Telegram** — Optional notifications and commands
- **Discord** — Optional bot interface for status checks
- **Email** — Alerts for urgent deadlines or issues

## Commands

```bash
# Load Canvas session
agent-browser state load ./auth/canvas-auth.json

# Start dashboard
python -m http.server 3000 --directory dashboard/

# Run daily sync
# (triggered automatically via heartbeat schedule)
```
