# Changelog — `toxi-realtime`

Per-crate history extracted from the monolith changelog
([meshackbahati/toxi](https://github.com/meshackbahati/toxi/blob/main/CHANGELOG.md)),
which remains the full documentation hub.

## Unreleased

- **toxi-realtime** (`3.2.0`): room join and create use one lookup and
  one name allocation through the entry API.

## Unreleased

- **toxi-realtime** (`3.2.0`): `Message` payloads are reference-counted
  (`Arc<String>`, `Arc<Value>`, `Arc<Vec<u8>>`), so fan-out clones
  pointers instead of duplicating payloads. Constructors keep their
  shapes; pattern matches observe `Arc` payloads.

## 3.1.5

- **toxi-realtime** (`3.1.3`): fan-out snapshots connection handles before
  delivery instead of sending under the registry lock; room broadcast no
  longer orders locks opposite to disconnect handling.

## 3.1.4

- **toxi-realtime**: bumped to `3.1.2` (no API changes, version sync).
