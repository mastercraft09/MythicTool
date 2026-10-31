# ⚔️ MythicTool

A comprehensive debug, development, and performance toolkit for MythicMobs.

MythicTool is designed for admins and developers who create or manage custom mobs, skills, and content with MythicMobs. It provides a complete set of real-time tools to test skills instantly, profile performance, validate configurations, and quickly understand why a mob or skill is not behaving as expected.

See also the `CHANGELOG.md` for the full list of changes in v2.0.0.

---

## Overview & Compatibility

- **Supported versions:** Minecraft 1.20.6 → 1.21.x
- **Supported platforms:** Paper, Purpur (and Paper forks)
- **Required dependency:** MythicMobs
- **Optional dependencies:** WorldGuard, LuckPerms

---

## Main Features

- **Skill & Mob debugging** — Understand exactly why a skill or mob fails.
- **Instant testing** — Trigger skills instantly without recreating complex in-game conditions.
- **Performance profiling** — Monitor slow skills, event spam, and per-tick mob cost with live TPS/MSPT.
- **Configuration validation** — Scan MythicMobs files for typos, missing skills, circular references, and official abbreviations (lvl, dmg, dur).
- **Live inspection** — Inspect active mobs, spawners, and their AI in real time.
- **Event boss bars** — Automatic countdowns, warnings, and custom actions for raids/dungeons/world bosses.
- **World management** — PvP/PvE toggles, combat logs, AFK tracking.
- **Fully customizable GUI** — `/mt gui` menu defined entirely in `config.yml`.

---

## Installation

1. Ensure MythicMobs is installed.
2. (Optional) Install WorldGuard and/or LuckPerms for advanced features.
3. Place `MythicTool-v2.0.0.jar` into the `plugins/` folder.
4. Restart the server to generate configuration files.
5. Assign permissions (see table below) or rely on OP defaults.

---

## Commands & Subcommands

**Main command:** `/mt`  
**Aliases:** `/mythictool`, `/mtool`

### Diagnostics & Basic Utilities

| Command | Description |
|---|---|
| `/mt help` | Shows all available subcommands. |
| `/mt status` | Displays active tools (Dev Mode, Hitbox, Brain Viewer, etc.). |
| `/mt hitbox` | Toggle mob hitbox visualization via particles. |
| `/mt monitor` | Toggle live skill monitor feed in chat. |
| `/mt inspect` | Inspect the mob you're looking at (HP, phase, target, AI, variables). |
| `/mt why [mob]` | Analyze why a mob isn't attacking or why a skill isn't firing. |
| `/mt validate` | Scan MythicMobs configs for errors. |
| `/mt validateall` | Full scan of all registered MythicMobs files. |

---

### Dev Mode — `/mt devmode [player]`

Advanced developer mode with configurable benefits:

| Option | Effect |
|---|---|
| `immortal` | Invulnerability while active. |
| `fly` | Automatically enables flight. |
| `night-vision` | Grants night vision. |
| `infinite-saturation` | Hunger bar always full. |
| `log-skills-in-chat` | Logs nearby mob skills in chat. |
| `no-mob-damage` | Mobs cannot damage you. |
| `tools.*` | Auto-enable skill monitor, hitbox, brain viewer, validator. |

**v2.0.0:** The `bypass-cooldowns` option was removed along with the entire cooldown system.

---

### Skill Tester — `/mt skill`

| Syntax | Description |
|---|---|
| `/mt skill` | List all available skills (clickable). |
| `/mt skill <skill>` | Execute the skill on yourself. |
| `/mt skill <skill> player <name>` | Execute the skill on another player. |
| `/mt skill <skill> loop <ticks>` | Repeat the skill every N ticks. |
| `/mt skill <skill> loop stop` | Stop your active skill loop. |
| `/mt skill <skill> repeat <times> <ticks>` | Repeat the skill a set number of times. |

**v2.0.0:** Cooldowns are no longer applied — skills always fire instantly.

---

### Performance Profiler — `/mt profiler`

| Subcommand | Effect |
|---|---|
| `start` | Start the profiler. |
| `stop` | Stop
