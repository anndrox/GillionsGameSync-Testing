# Testing changelog

## 0.0.95.0 — travel refusal back-off (experimental prerelease)

- A travel upload refused by Gillions waits 5 minutes before trying again,
  instead of retrying every 15 seconds. A character change, login or travel
  setting change retries at once.
- Everything else is unchanged. The update from 0.0.94 preserves configuration
  (checked with the real serializer). No physical in-game testing.

Source: anndrox/GillionsGameSync `2630eaa0da547ba3612be3b78a870bba819cbafc`.
Release record: [releases/0.0.95.json](releases/0.0.95.json).

## 0.0.94.0 — grouped inventory uploads (experimental prerelease)

- During heavy gathering or crafting, inventory uploads are grouped: at most
  one per 10 seconds, and a change is held for at most about 10 seconds. That
  is about 41% fewer during activity.
- An isolated change still uploads after 1.5 seconds, and Sync now still
  uploads immediately.
- Everything else is unchanged. The update from 0.0.93 preserves configuration
  (checked with the real serializer). No physical in-game testing.

Source: anndrox/GillionsGameSync `f1866ecefbdc56b87f2aca29b567b9c95996a57b`.
Release record: [releases/0.0.94.json](releases/0.0.94.json).

## 0.0.93.0 — quieter Retainer uploads (experimental prerelease)

- Retainer data is sent when it changes, or when venture results are waiting,
  plus a 5-minute "still current" refresh, instead of every 30 seconds. An
  unchanged hour now sends 12 times instead of about 120.
- Sync now still sends everything immediately.
- Everything else is unchanged. The update from 0.0.92 preserves configuration
  (checked with the real serializer). No physical in-game testing.

Source: anndrox/GillionsGameSync `032544a132aa2bc20fa3cc1f0fab17bb3e3d40ab`.
Release record: [releases/0.0.93.json](releases/0.0.93.json).

## 0.0.92.0 — Gillions refusals named (experimental prerelease)

- A refusal from Gillions is never shown as "Gillions unavailable". The
  connection says one of:
  - Character not linked on Gillions;
  - Paired to a different character;
  - Reconnect required;
  - Refused by Gillions.
- A one-time in-game chat notice explains how to fix the character problems.
- Finishing a reconnect started from Settings returns to Settings instead of
  opening a second window.
- Everything else is unchanged. The update from 0.0.91 preserves configuration
  (checked with the real serializer). No physical in-game testing.

Source: anndrox/GillionsGameSync `ac5920e6b72ec7d016fe2680bd54f890485176da`.
Release record: [releases/0.0.92.json](releases/0.0.92.json).

## 0.0.91.0 — regression audit and accurate status (experimental prerelease)

- Each feature row says what is actually wrong:
  - an unsupported game version;
  - Off, or Off on Gillions;
  - Not available on Gillions;
  - waiting for data;
  - temporarily unavailable;
  - ready.

  Party Finder no longer always says Ready. Market no longer reports every case
  as temporarily unavailable. A Gillions refusal of the FATE source no longer
  says "Update required".
- Only a request to Gillions can mark it unavailable. Refused authorization or
  client versions are shown as such.
- Item links no longer pass through the Party Finder admission when PF links
  are off.
- Fewer full configuration saves, a backoff on failed saves, and no per-frame
  retries during loading screens.
- Retainer gear, coverage and gil are attributed only to a stably active
  retainer.
- Private uploads take turns, and FATE checks no longer churn outside
  supported areas.
- Includes the native observation integrity work (unavailable data is
  withheld, never sent as empty).
- Native compatibility, consent, permissions, pairing, settings and payloads
  are unchanged. The update from 0.0.90 preserves configuration (checked with
  the real serializer).
- No physical in-game testing for this version.

Source: anndrox/GillionsGameSync `020cce9e6aaaa68f4225a370d3a52da62a363a8c`.
Release record: [releases/0.0.91.json](releases/0.0.91.json).

## 0.0.90.0 — 7.57 hotfix compatibility (experimental prerelease)

- Supports game 2026.10.16.0000.0000 with Dalamud 15.0.3.9 (ClientStructs
  7.57.0.9414) through one per-collector compatibility table; unlisted runtimes
  fail closed and one collector's support never enables another.
- Hunt Progress is physically accepted on this runtime. Submarine reads are
  source qualified but not physically tested. FATE collection, Hunt-routing
  location and private uploads await Gillions TEST admission of the new runtime
  and reference data; they stay unavailable until then.
- Includes collectible readiness: Collectibles are withheld while native sources
  are unavailable instead of being reported as complete-empty.
- Consent, permissions, pairing, settings and payloads are unchanged; the update
  from 0.0.88 preserves configuration (actual-serializer check).

Source: anndrox/GillionsGameSync `1aeafe68190e052d72129fa7a68a4a9a1cc5a0d9`.
Release record: [releases/0.0.90.json](releases/0.0.90.json).

## 0.0.88.0 — experimental prerelease

- Establishes this dedicated public Testing distribution and normal Dalamud feed.
- Reuses the maintained Testing stream and accepted shared Public 1.0.31.3
  sizing, resizing, positioning, input, reconnect and Hunt-status corrections.
- Separates saved Testing window IDs without changing Public geometry or settings.
- Restricts all authenticated Testing requests to the existing secure TEST service;
  old production-bound Testing pairing is retained but inactive.
- Preserves existing collection, retention, permission and read-only boundaries.

This release is offline-first. Public distribution does not grant TEST network
or account access. TEST FATE exact-version admission does not currently include
0.0.88.0; that contribution remains unavailable/fail-closed. Production Testing
admission is not enabled. Never enable Public and Testing together.

Source/package, manifest, upgrade and independent-review checks passed. Physical
FFXIV installation/update and corrected shared-UI acceptance remain owner checks.
Existing controller and live FC submarine validation limitations remain.

See [installation and safe switching](README.md) and the immutable
[release record](releases/0.0.88.json). Historical Testing releases remain in the
[original source repository](https://github.com/anndrox/GillionsGameSync/releases).
