# Testing changelog

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
