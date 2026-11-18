# Troubleshooting

## Players not being detected

- **Probe shows `supported=false`** — the client doesn't respond to the anvil-rename probe (very old client, or a client that blocks it). Channel/brand detection still applies.
- **Anticheat probe not running** — check Settings → Auto-Probe → "On anticheat flag" is ON, and that your anticheat is GrimAC-compatible.
- **Mod shows as allowed (red)** — it's intentionally allowed by default, or someone toggled it. Check `/rg` → Mods.

## Legit players getting kicked

1. Check the violation layer in their inspect/log — `brand`/`channels` false positives are rare but possible with unusual clients.
2. `/rg` → Mods/Clients → set the entry to **allowed** (red).
3. For staff/testing: grant `relishguard.bypass`.

## Dialogs not opening / closing instantly

- Requires **Paper 1.21+** dialogs — very old forks may not support them.
- If a dialog "just closes" on click, check console for `[RelishGuard] ... generated an exception` and report it.

## Discord alerts not arriving

- Settings → Discord → Enabled ON + valid webhook URL (must include `https://discord.com/api/webhooks/...` or `discordapp.com`).
- Test the webhook URL in a browser — it should return JSON, not an error page.

## Language not switching

- File must be valid YAML with the same keys as `en.yml` — a parse error falls back to `en`.
- Check console for YAML errors on `/rg reload`.

## Data reset

Delete `plugins/RelishGuard/data.db` while the server is stopped to wipe violations and mod toggles (settings live in `config.yml`). `lang/` files are untouched.
