# Sorlyn Sync

Sorlyn Sync is the planned optional synchronization system for the Sorlyn
browser. This document captures the design intent. **Sorlyn Sync is not yet
implemented**, and this is the most exploratory item on the roadmap; details are
likely to change.

## Goals

- Let users optionally synchronize browser data (such as bookmarks, history, or
  preferences) across their own devices.
- Treat privacy as the default and the priority.
- Keep the feature entirely opt-in.

## Principles

- **Optional.** Sync is off by default. The browser is fully usable without it,
  and no data is synchronized unless the user explicitly enables it.
- **Encrypted.** Synchronized data should be protected with end-to-end
  encryption so that the sync service cannot read user content.
- **Privacy-first.** Collect as little as possible. Avoid tying sync to
  unnecessary identifiers or profiling.
- **Possibly self-hostable.** Where practical, allow users to run their own sync
  server rather than depending on a single hosted service.

## Open questions

These will be explored during Phase 4 (see [`ROADMAP.md`](./ROADMAP.md)):

- What data types are in scope for an initial version, and in what order.
- The encryption and key-management model, including how keys are derived,
  stored, and recovered.
- The protocol and storage model, and how a self-hosted option would work.
- Whether to build on existing sync protocols/infrastructure or design a new
  one, and the trade-offs of each.
- How sync interacts with Firefox's existing sync facilities.

## Non-goals (for now)

- A hosted, account-based service as a prerequisite for using Sorlyn.
- Synchronizing data without explicit user opt-in.
- Server-side access to unencrypted user data.

## Status

Exploration only. No implementation exists. This document will be expanded as
the design is investigated; it may also be deferred in favor of earlier
priorities such as Sorlyn Shield.
