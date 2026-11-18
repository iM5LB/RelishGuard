# Permissions

Defined in `plugin.yml`:

| Node | Default | Description |
|------|---------|-------------|
| `relishguard.admin` | `op` | Full admin — parent of gui/inspect/check |
| `relishguard.gui` | `op` | Open the `/rg` dashboard |
| `relishguard.inspect` | `op` | `/rg inspect <player>` |
| `relishguard.check` | `op` | `/rg check <player>` live probe |
| `relishguard.bypass` | `op` | **Exempt from punishment & Discord** — detections still recorded |

## Bypass behavior

Players with `relishguard.bypass`:

- ✅ Violations still recorded (visible in inspect + violation log)
- ❌ No kick / ban / ban-ip
- ❌ No Discord alert
- ❌ No punishment console commands

Because it defaults to `op`, server ops are exempt automatically. For non-op trusted players (e.g. staff accounts, testers):

```
/lp user <name> permission set relishguard.bypass true
```

To make a specific player **not** bypass despite being op:

```
/lp user <name> permission set relishguard.bypass false
```
