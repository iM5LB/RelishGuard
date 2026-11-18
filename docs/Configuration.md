# Configuration

RelishGuard's `config.yml` holds the license key and every runtime setting. Changes made in the in-game **Settings** dialog are written straight back to `config.yml`.

## `config.yml`

| Key | Default | Description |
|-----|---------|-------------|
| `license-key` | `""` | License key — paid keys start with `RL-`, trials with `TRL-` |
| `install-id` | auto | Device fingerprint for trial/license tracking — generated once, do not edit |
| `language` | `en` | Active `lang/*.yml` file |
| `debug` | `false` | Verbose `[RG]` console logs |
| `metrics.enabled` | `true` | Anonymous bStats usage statistics |
| `auto-probe-on-join` | `true` | Run rename probe on every join |
| `on-anticheat-flag` | `true` | Run rename probe when anticheat flags |
| `auto-punish` | `true` | Punish on enforced detections |
| `punishment-type` | `kick` | `kick` / `ban` / `ban-ip` |
| `discord.enabled` | `false` | Discord webhook alerts |
| `discord.webhook-url` | `""` | Webhook URL |
| `discord.server-name` | `""` | Name in alerts — empty uses the server name |

Blank values fall back to the built-in default.

## Data storage — `plugins/RelishGuard/data.db`

SQLite database created on first boot:

| Table | Contents |
|-------|----------|
| `violations` | Every recorded detection: player, mod, layer, brand, timestamp |
| `mod_toggles` | Per-mod enforcement overrides (enabled/disabled) |

## Runtime settings

Editable in the **Settings** dialog or directly in `config.yml`; dialog changes save to `config.yml` immediately and apply live.

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| `debug` | bool | `false` | Verbose `[RG]` console logs |
| `metrics.enabled` | bool | `true` | Anonymous bStats usage statistics |
| `auto-punish` | bool | `true` | Punish on enforced detections |
| `punishment-type` | string | `kick` | `kick` / `ban` / `ban-ip` for auto-punishments |
| `auto-probe-on-join` | bool | `true` | Run rename probe on every join |
| `on-anticheat-flag` | bool | `true` | Run rename probe when anticheat flags |
| `discord.enabled` | bool | `false` | Discord webhook alerts |
| `discord.webhook-url` | string | `""` | Webhook URL |
| `discord.server-name` | string | server name | Name shown in alerts |
| `language` | string | `en` | Active `lang/*.yml` file |

## Mod toggles

Each registry entry (clients + mods) has an `enabled` flag in `mod_toggles`. A row only exists after you flip a toggle — entries without a row use the Java default (hacked clients enforced, legit mods allowed).

## Language files — `lang/*.yml`

All text. See [Languages](Languages.md).

## Hardcoded internals

Detection rules (probe keys, channel lists, brand blacklist, timings, thresholds) are compiled into `DetectionRules` / `RelishConfig` — intentionally not configurable so detection can't be tampered with via files.
