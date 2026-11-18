# Installation

## Requirements

- Minecraft **1.21+**
- **Paper**, **Purpur**, or a Paper-based fork (Folia-compatible)
- **Java 21+**
- **[PacketEvents](https://modrinth.com/plugin/packetevents)** — **required**, install it first

## Steps

1. Install **PacketEvents** and restart the server once so it generates its own files.
2. Drop `RelishGuard.jar` into `plugins/`.
3. Restart the server.
4. On first boot the plugin creates:

   ```
   plugins/RelishGuard/
   ├── config.yml      # license key + install-id + setting defaults
   ├── data.db         # SQLite — violations + mod toggles
   └── lang/
       └── en.yml      # all player/staff-facing text
   ```

   `config.yml` holds the license key, install ID, and all settings — in-game Settings changes write straight back to it.

5. Verify in console: `[RelishGuard] RelishGuard enabled.`

## Optional integrations

| Plugin | Effect |
|--------|--------|
| GrimAC (or compatible anticheat) | Probe runs automatically when a player is flagged |
| Discord webhook | Violation/punishment alerts — configured in Settings → Discord |

## License

RelishGuard is a premium plugin — purchase a license key on [Relish Plugins](https://relishes.studio/?buy=relish-guard).

**Activation:**

1. Paste your key into `license-key` in `plugins/RelishGuard/config.yml` — paid keys start with `RL-`, trial keys with `TRL-`
2. **No key?** The plugin self-requests a 14-day free trial on first boot (one trial per device, enforced server-side)
3. Validation runs on startup and every 30 minutes; invalid, expired, or revoked keys fully disable enforcement
4. License responses are RSA-signed — forged replies are rejected

Current license state is printed in the console on startup (`Mode: Premium Version | License: Active`).
