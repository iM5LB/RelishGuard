# RelishGuard

![RelishGuard](https://github.com/iM5LB/RelishGuard/raw/master/docs/assets/RelishGuardBanner.png)


Official documentation for **RelishGuard** — client integrity and prohibited-mod detection for Paper 1.21+ servers.

RelishGuard is a premium plugin — **14-day free trial, no key needed**. [Get a license key on Relish Plugins](https://relishes.studio/?buy=relish-guard).

## What is RelishGuard?

RelishGuard detects hacked clients and prohibited mods **during the join handshake** — before a cheater reaches spawn. It identifies the exact client or mod by name, enforces per-signature rules you control, and keeps legitimate QoL and map mods working.

- **Caught before spawn** — brand checks, channel inspection, and a stealth translation-key probe (MC-265322) fire during login
- **Know exactly what they run** — every detection names the client or mod (Wurst, Meteor, Vape, xray packs, autoclickers), not just "suspicious player"
- **Protect your legit players** — per-mod toggles mean Jade, Xaero's, JourneyMap, Litematica, and other QoL mods stay allowed while banned clients get kicked
- **Let anticheats feed it** — flagged players automatically trigger the full probe pipeline when GrimAC (or your anticheat) fires
- **Run everything from `/rg`** — a native Paper dialog dashboard for inspecting players, flipping mod toggles, reviewing violations, and changing settings
- **Keep your data** — settings in `config.yml`, violation history and toggles in SQLite (`data.db`), all text in `lang/*.yml`
- **Alert your staff** — Discord webhook notifications for every detection and punishment
- **Works everywhere** — Paper, Purpur, and Paper forks including Folia

> **Honest limits:** purely client-side modules with zero protocol footprint can't be name-detected — no plugin can do that. GrimAC behavioral flags and Paper anti-xray cover those cases.

## Quick Links

| Guide | Description |
|-------|-------------|
| [Installation](Installation.md) | Install and verify |
| [Quick Start](QuickStart.md) | First setup in minutes |
| [Detection](Detection.md) | How detection works and what it covers |
| [Staff Dashboard](Dashboard.md) | The `/rg` dialog UI |
| [Configuration](Configuration.md) | Settings, mod toggles, and data storage |
| [Commands](Commands.md) | Full command list |
| [Permissions](Permissions.md) | Nodes and bypass |
| [Languages](Languages.md) | Adding translations |
| [Discord Alerts](Discord.md) | Webhook setup |
| [Troubleshooting](Troubleshooting.md) | Common fixes |

## Requirements

| Component | Requirement |
|-----------|-------------|
| Minecraft | 1.21+ |
| Server | Paper, Purpur, or Paper-based forks (Folia supported) |
| Java | 21+ |
| Dependencies | PacketEvents (required) |
| Soft dependencies | GrimAC or another anticheat, Discord webhook (optional) |

## Getting Help

- Store: [relishes.studio](https://relishes.studio/)
- Discord: [Support server](https://discord.gg/j8BNhh2xNw)
- Issues: [github.com/iM5LB/RelishGuard/issues](https://github.com/iM5LB/RelishGuard/issues)
- Donate: [creators.sa/m5lb](https://creators.sa/m5lb)

## Next Steps

1. [Install RelishGuard](Installation.md)
2. [Quick Start](QuickStart.md) — open `/rg` and review the Mods list
3. Tune [Configuration](Configuration.md) and set permissions
