# Quick Start

## 1. Open the dashboard

```
/rg
```

Players with `relishguard.gui` (ops by default) get the **RelishGuard** dialog: Players, Clients, Mods, and Settings.

## 2. Review the mod lists

- **Clients** — hacked clients (Wurst, Meteor, etc.). Enforced by default.
- **Mods** — individual mods (xray, freecam, QoL…). Each entry shows **green = enforced** or **red = allowed**.

Everything legitimate is already allowed by default (maps like Xaero's/JourneyMap, camera mods, inventory QoL, libraries are ignored entirely). Flip anything you disagree with — toggles save instantly to `data.db`.

## 3. Check a player

```
/rg inspect <player>
```

Shows brand, channels, detected mods, live probe results, and a **Violation Log** of everything recorded. From there you can **Run Live Probe**, **Kick**, **Ban**, or **Ban IP** manually.

## 4. Tune enforcement

`/rg` → **Settings**:

- **Auto-Punish** — on/off plus `KICK`, `BAN`, or `BAN-IP`
- **Auto-Probe** — probe on join and/or on anticheat flag
- **Discord** — webhook alerts
- **Language** — pick any `lang/*.yml` file

## 5. Permissions

Ops bypass automatically (`relishguard.bypass` defaults to `op`). For non-op staff who should bypass punishment but still be inspected:

```
/lp user <name> permission set relishguard.bypass true
```
