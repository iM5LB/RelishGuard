# Changelog

## 1.0.0

Initial release.

### Detection

- Client brand blacklist checks on join
- Plugin-message channel inspection with namespace matching
- Stealth anvil-rename translation-key probe (MC-265322) — runs on join, on demand, and on anticheat flags
- Inventory click-burst heuristic
- Per-mod enforcement toggles; legit QoL/map/camera mods allowed by default; shared libraries ignored entirely
- `relishguard.bypass` permission — records detections, skips punishment/Discord (default: op)

### Metrics

- Optional anonymous usage statistics via bStats (`metrics.enabled`, default `true`)

### Staff dashboard

- Paper Dialog UI: Players grid, Clients, Mods (search + pagination), Settings
- Inspect view: brand, channels, detected mods, live probe, violation log, kick/ban/ban-ip actions
- Settings: debug, auto-punish (kick/ban/ban-ip), auto-probe (join + anticheat flag), Discord webhook, language picker
- All dialog text localized via `lang/*.yml`

### Storage & integrations

- `config.yml` holds the license key and all runtime settings (Settings dialog writes back to it); SQLite `data.db` stores violations and mod toggles
- Discord webhook alerts
- PacketEvents packet layer; GrimAC anticheat bridge; Folia-compatible schedulers
