# Languages

All player- and staff-facing text lives in `plugins/RelishGuard/lang/*.yml` — kick messages, chat replies, dialog titles, buttons, tooltips, prompts, and body lines.

## Adding a language

1. Copy `lang/en.yml` to `lang/<code>.yml` (e.g. `es.yml`, `fr.yml`, `de.yml`).
2. Translate the **values** — keep the keys identical.
3. `/rg` → **Settings → Language** → pick it from the list. Applies instantly, no restart.

The picker scans `lang/*.yml` every time it opens, so dropping in a new file is enough — no reload needed.

## Fallbacks

- Missing **keys** fall back to `en`
- Missing **file** falls back entirely to `en`

## What's in `en.yml`

| Section | Contents |
|---------|----------|
| `kick.*` | Kick message template + Discord invite footer |
| `punish.*` | Broadcast, default/manual reasons, ban/kick labels |
| `reason.*` | Detection reason strings incl. all anticheat offense phrases |
| `info.*` / `check.*` / `help.*` | Command output |
| `dialog.*` | Every dialog title, button, tooltip, input label, body line |

Detection **names** (Wurst, Xaero's, channel namespaces) are data in `DetectionRules`, not lang keys — they stay consistent across languages.

## Placeholders

Values support `{placeholder}` tokens filled by the plugin — `{player}`, `{uuid}`, `{brand}`, `{reason}`, `{mod}`, `{state}`, `{lang}`, `{page}`, `{count}`, `{query}`, etc. Keep them intact when translating.
