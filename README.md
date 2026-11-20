# QuickTarget

A World of Warcraft: **Forever** addon for targeting something by name — then marking and pinging it — without ever opening the macro window. Great for rare hunting.

## Install

1. Download **QuickTarget.zip** from the [Releases](../../releases) page (not the green "Code" button).
2. Unzip it into your Forever `Interface\AddOns` folder, so you end up with `Interface\AddOns\QuickTarget\QuickTarget.toc`.
3. Fully restart the game.

## How it works

Type a name into the box and press Enter, then click **Target** (or use the keybind). It runs:

```
/cleartarget
/target <name>
/stopmacro [noexists][dead]
/tm 0
/tm 8
/ping [@target] attack
```

So it targets the mob, puts your chosen raid marker on it, and pings it — and does nothing if the mob isn't found or is dead.

- **Marker** — click the icon next to the box to cycle markers (left = next, right = previous). Default is skull.
- **Ping** — click the ping button to cycle Attack / Warning / Assist / On My Way / Ping / No ping.
- **Several names** — separate them with `;` (e.g. `Rare One; Rare Two`).
- **Keybind** — Options → Keybindings → AddOns → QuickTarget.
- **Make Macro** — creates a real macro called "QuickTarget" you can put on an action bar. It follows whatever is in the box.

## Commands

| Command | What it does |
|---|---|
| `/qt` | Show/hide the window |
| `/qt <name>` | Set the name |
| `/qt mark <0-8>` | Marker (8 = skull, 0 = none) |
| `/qt ping <none\|attack\|warning\|assist\|onmyway\|ping>` | Ping type |
| `/qt macro` | Create/refresh the QuickTarget macro |

## Notes

- Changing the name during combat applies as soon as combat ends (WoW blocks addons from changing targeting buttons in combat).
- `/target` matches partial names, so type enough of the name to avoid grabbing something nearby by mistake.
- Pings are seen by your party/raid; solo, only you see them.
