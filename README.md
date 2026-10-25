# Gillions Game Sync Testing

Public, opt-in experimental releases of **Gillions Game Sync Testing**.
This distribution repository contains documentation, the Dalamud custom feed,
checksums and release assets—not a second source-code fork.

[Authoritative source](https://github.com/anndrox/GillionsGameSync) ·
[Testing releases](https://github.com/anndrox/GillionsGameSync-Testing/releases) ·
[Report a bug](https://github.com/anndrox/GillionsGameSync-Testing/issues)

## Install

1. Disable installed Gillions Game Sync Public and any dev copies. Keep its
   configuration, pairing and Stable repository entry; do not reset anything.
2. In Dalamud Settings → Experimental → Custom Plugin Repositories, add:

   `https://raw.githubusercontent.com/anndrox/GillionsGameSync-Testing/main/data/GillionsGameSyncTesting.json`

3. Open the plugin installer, refresh repositories and install **Gillions Game
   Sync Testing**. Confirm channel Testing, version 0.0.96.0 and `/gillionssynctest`.
4. Existing Testing users first disable/uninstall only the old Testing plugin,
   without reset/delete-configuration, then remove its old feed and install from
   the new one. Follow any normal installer reload prompt. Dalamud binds updates
   to the installed-from URL, so a URL change alone is insufficient. Keep Stable
   and all settings; no config copying is needed.

The standard Dalamud installer delivers subsequent Testing updates through this
same feed. No custom updater or manual DLL replacement is required. Historical
Testing releases/old feed remain preserved, but this repository is the new channel.

## One enabled copy; separate settings

Public uses `GillionsGameSync`; Testing uses `GillionsGameSyncTest`. They have
separate configuration/pairing files and commands. Both can remain installed,
but **do not run both simultaneously**: duplicate reads/uploads are possible.
Testing88 has separate saved window IDs, preserving Public geometry. Older
Testing geometry stays retained but is not imported; Testing uses readable
defaults. Simultaneous live operation is not supported.

To return, disable Testing before enabling your installed Public release. You may
remove this feed and uninstall only Testing. Never delete/reset Public configuration.
Normal Testing updates preserve Testing settings/history. Testing configuration
deletion is a separate user choice, not an installation or migration requirement.

## Offline first; TEST access is separate

Public distribution does **not** grant access to the Gillions Site TEST service.
UI and local Hunt Progress can be checked unpaired/offline. No account or upload
permission is required for those checks. Testers with separately approved secure
TEST access may pair Testing using its existing controls and applicable consents.
Do not copy Public credentials or pair this build to production.

If an older Testing configuration still points to production, use **Settings →
Advanced → Testing diagnostics → Use shared TEST for next pairing** before
pairing, and only if you have approved TEST access. Existing production-bound
Testing credentials remain inactive; they are not moved or deleted.

All Testing authenticated requests—including ordinary sync and commands—are
restricted to the existing exact HTTPS TEST service, with redirects disabled.
Historical Testing production pairing/history is preserved but inactive; it is
not moved to TEST. Public pairing is untouched. No new production API admission,
gameplay automation or contribution permission is introduced.

## Testing 0.0.96 contents and limits

Testing 0.0.96.0 waits 5 minutes after a "character not linked" refusal instead
of retrying inventory every 10 seconds, and its one-time chat notice names the
character. Everything else is unchanged from 0.0.95. There is no physical in-game
test. Release record: [releases/0.0.96.json](releases/0.0.96.json).

## Testing 0.0.95 contents and limits

Testing 0.0.95.0 waits 5 minutes after a refused travel upload instead of
retrying every 15 seconds. Everything else is unchanged from 0.0.94. There is no
physical in-game test. Release record: [releases/0.0.95.json](releases/0.0.95.json).

## Testing 0.0.94 contents and limits

Testing 0.0.94.0 groups inventory uploads during heavy gathering or crafting:
at most one per 10 seconds, and a change is held for at most about 10 seconds.
That is about 41% fewer during activity. Everything else is unchanged from
0.0.93. There is no physical in-game test. Release record:
[releases/0.0.94.json](releases/0.0.94.json).

## Testing 0.0.93 contents and limits

Testing 0.0.93.0 sends Retainer data only when it changes, or when venture
results are waiting, plus a 5-minute "still current" refresh. Before, it was
sent every 30 seconds, so this cuts about 85% of Game Sync upload traffic.
Everything else is unchanged from 0.0.92. There is no physical in-game test.
Release record: [releases/0.0.93.json](releases/0.0.93.json).

## Testing 0.0.92 contents and limits

Testing 0.0.92.0 names every Gillions refusal instead of showing "Gillions
unavailable":
- **Character not linked on Gillions:** add the character on the website in
  Preferences, for example from the Lodestone.
- **Paired to a different character:** pair again while playing this character.
- **Reconnect required.**
- **Refused by Gillions.**

A one-time in-game chat notice explains the character problems. Finishing a
reconnect from Settings no longer opens a second window.

Everything else, including native compatibility, consent and pairing, is
unchanged from 0.0.91. There is no physical in-game test of the 0.0.92
corrections. Release record: [releases/0.0.92.json](releases/0.0.92.json).

## Testing 0.0.91 contents and limits

Testing 0.0.91.0 makes each feature's status say what is actually wrong:
- an unsupported game version;
- Off, or Off on Gillions;
- Not available on Gillions;
- waiting for data;
- temporarily unavailable;
- ready.

It also fixes command, sync, save and retainer reliability problems found by a
whole-plugin regression audit, and includes the native observation integrity
work: unavailable inventory, currency, gil and character data are withheld,
never sent as empty.

- **Runtime and native compatibility:** unchanged from 0.0.90 (game
  `2026.10.16.0000.0000`, Dalamud 15.0.3.9).
- **Physical testing:** none for this version. The changes are source-qualified
  and covered by automated tests, including a real-serializer upgrade from
  0.0.90.
- **FATE:** shows "Not available on Gillions" until Gillions TEST admits the
  2026.10.16 source.
- **Private Hunt/submarine uploads:** Gillions currently refuses them for
  2026.10.16 (reference data pending).

Consent, permissions, pairing and settings are unchanged. Release record:
[releases/0.0.91.json](releases/0.0.91.json).

## Testing90 contents and limits

Testing 0.0.90.0 supports the 7.57 hotfix runtime: game `2026.10.16.0000.0000`
with Dalamud 15.0.3.9 (ClientStructs 7.57.0.9414). Every patch-sensitive collector
is checked against its own exact compatibility entry; other runtimes fail closed.

- **Hunt Progress:** physically accepted on this runtime by the owner. Bills,
  target counts and zone changes matched the in-game Hunt log.
- **Submarines:** source qualified, not yet physically tested on this runtime.
- **FATE:** collection waits for Gillions TEST admission of the new source. Until
  then it stays unavailable, and no FATEs are read or contributed.
- **Hunt-routing location:** stays off unless separately consented. Its upload, the
  private Hunt/submarine uploads and their reference data also wait for Site
  admission of the new game version.

Consent, permissions, pairing and settings are unchanged; updating from 0.0.88
preserves them. Source, package and serializer checks are not physical proof for
features that have not been run in the game.

## Initial Testing88 contents and limits

Readable, resizable Main/Settings/Pairing windows, clear reconnect instructions
and honest current-area/unknown Hunt Progress messages share the frozen Public
1.0.31.3 implementation. This separately compiled Testing DLL is not that Public
binary. Existing Testing diagnostics and independently gated features remain.

Current TEST FATE exact-version admission includes86/87, not88: FATE contribution
therefore stays unavailable/fail-closed until separately authorized admission.
Other online features need their existing compatible acknowledgements and consent.
Most community testers should use offline UI testing until granted TEST access.

Automated package, actual-serializer and policy checks do not establish physical
FFXIV acceptance. Initial fresh installation/update, placement/input and shared-UI
runtime acceptance remain owner live checks; controller/live FC submarine limits
remain disclosed. This is an experimental prerelease, not Stable promotion.

## Quick test and bug report

Resize/move Main and Settings; shorten them to check scrolling; close/reopen to
check geometry persistence. Check mouse/keyboard/chat. Inspect `pair` without
submitting a code. Optionally enable local Hunt Progress and inspect its lock and
unknown/current-area wording; do not manufacture kills or enable extra sharing.

Report Testing version, a short safe support summary and cropped screenshots.
Do not post configuration, credentials, pairing codes, raw private exports or
identifying activity logs. Consult the release changelog for known limitations.
