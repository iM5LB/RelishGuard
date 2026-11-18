# Discord Alerts

RelishGuard can post detections and punishments to a Discord channel via webhook.

## Setup

1. Discord → Channel settings → **Integrations → Webhooks → New Webhook** → Copy URL.
2. `/rg` → **Settings → Discord**:
   - **Discord Enabled** — toggle on
   - **Webhook URL** — paste the URL, Save
   - **Server Name** — shown in alerts; leave empty to use the server's actual name

All fields save instantly to `data.db`.

## What gets sent

- Detection alerts (mod/client, player, brand, layer)
- Punishment notices (kick/ban with reason)

## Bypass interaction

Players with `relishguard.bypass` still get violations **recorded** but produce **no** Discord alert and no punishment.

## Kick footer

Every kick message ends with a Discord invite link. It lives in `lang/en.yml` under `kick.discord-url` — set it to your support server or empty string to hide.
