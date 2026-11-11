# Gillions Game Sync Testing

This is the feed for early builds of Gillions Game Sync, a Dalamud plugin that connects your FINAL FANTASY XIV character to [Gillions](https://gillions.app). Use Stable for everyday play.

## What it shares

Sharing through Game Sync is optional. You can try the plugin window without pairing. Testing pairs only with the Gillions TEST site, for testers with approved access. You choose what to share in Game Sync settings on the TEST site, and you can turn sharing off at any time. Some categories need a compatible game version or only update after you open the relevant window in game.

**On when you pair (you can turn these off):**

- Inventory, gear and currencies
- Retainers and ventures
- Glamour plates and dye colours
- Achievements, collectibles, quests and character progress, including reputation and Shared FATE progress
- Gil ledger
- Hunt progress
- Submarine voyages
- Market listings and recent sales you see

Hunt progress, submarine voyages and market updates each have their own switch in Game Sync settings. The rest stop when you disconnect your device.

**Off until you turn them on:**

- Travel and location
- Live FATEs
- Character appearance (Testing only)
- **Party Finder (optional):** Party Finder listings you see in game, including other players' public listings, are sent to Gillions, which passes them on to xivpf.com.

Testing also has a Beastmaster view that stays on your device and does not upload data.

## Install

In Dalamud, go to **Settings > Experimental > Custom Plugin Repositories**. Add the URL for your channel and save. Then open the plugin installer and install the matching plugin.

### Testing (early builds)

Disable Stable and any development copies first. Install **Gillions Game Sync Testing** and open `/gillionssynctest` in game. Keep your Stable settings and pairing. See the [Testing guide](docs/testing-guide.md#install) if you already use an older Testing feed.

```text
https://raw.githubusercontent.com/anndrox/GillionsGameSync-Testing/main/data/GillionsGameSyncTesting.json
```

### Stable

Install **Gillions Game Sync** and follow the [Stable pairing steps](https://github.com/anndrox/GillionsGameSync#stable). Disable Testing before turning Stable back on.

```text
https://raw.githubusercontent.com/anndrox/GillionsGameSync/main/data/GillionsGameSync.json
```

## Support

Visit [Gillions Help](https://gillions.app/help) for setup and troubleshooting. See the [Testing bug report guide](docs/testing-guide.md#quick-test-and-bug-report) for what to include in a report.

## For developers

See the [developer docs](docs/README.md) for Testing notes and release records. [MIT licence](LICENSE).
