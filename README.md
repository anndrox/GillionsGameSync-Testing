# Gillions Game Sync Testing

This is the feed for early builds of Gillions Game Sync, a Dalamud plugin that connects your FINAL FANTASY XIV character to [Gillions](https://gillions.app). Use Stable for everyday play.

## What it shares

Game Sync reads supported data without changing it. That includes inventory, gear and currencies; retainer items and ventures; glamour plates and dye colours; achievements, collectibles and quest progress; and Gil changes for the ledger. You choose each sharing category on Gillions: [gillions.app](https://gillions.app/gillions-sync) for Stable, or the separate Gillions TEST site if you have approved access. You can try the plugin window without pairing.

## Install

In Dalamud, go to **Settings > Experimental > Custom Plugin Repositories**. Add the URL for your channel and save. Then open the plugin installer and install the matching plugin.

### Testing (early builds)

Disable Stable and any development copies first. Install **Gillions Game Sync Testing** and open `/gillionssynctest` in game. Keep your Stable settings and pairing. See the [Testing guide](docs/testing-guide.md#install) if you already use an older Testing feed.

```text
https://raw.githubusercontent.com/anndrox/GillionsGameSync-Testing/main/data/GillionsGameSyncTesting.json
```

### Stable

Install **Gillions Game Sync** and follow the [Stable pairing steps on gillions.app](https://gillions.app/gillions-sync). Disable Testing before turning Stable back on.

```text
https://raw.githubusercontent.com/anndrox/GillionsGameSync/main/data/GillionsGameSync.json
```

## Screenshots

Screenshots of the Testing window and sharing settings will go here.

## Support

Visit [Gillions Help](https://gillions.app/help) for setup and troubleshooting. See the [Testing bug report guide](docs/testing-guide.md#quick-test-and-bug-report) for what to include in a report.

## For developers

See the [developer docs](docs/README.md) for Testing notes and release records. [MIT licence](LICENSE).
