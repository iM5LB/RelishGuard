# Commands

Base command: `/relishguard` (alias `/rg`)

| Command | Permission | Description |
|---------|-----------|-------------|
| `/rg` | `relishguard.gui` | Open the staff dashboard dialog |
| `/rg help` | — | Show command help |
| `/rg inspect <player>` | `relishguard.inspect` | Inspect a player — brand, channels, mods, violations, actions |
| `/rg settings` | `relishguard.gui` | Open the Settings dialog directly |
| `/rg check <player>` | `relishguard.check` | Run a live rename probe on a player |
| `/rg reload` | `relishguard.admin` | Reload language files and runtime settings |

## Inspect actions

Inside the inspect dialog you can also:

- **Run Live Probe** — immediate rename probe with results
- **Kick Player** / **Ban Player** — prompts for a reason
- **Ban IP** — bans the player's current IP
- **Violation Log** — paginated recorded violations for that player

All manual punishments record a violation entry (`manual-ban`, `manual-ip-ban`, `manual-kick-by` layers) so they show up in logs.
