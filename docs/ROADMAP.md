# Sorlyn Roadmap

This roadmap describes the planned phases for Sorlyn. It is intentionally
conservative. Each phase should be small, reviewable, and maintainable, and
should land before the next phase begins. Phases may be revised as the project
learns more.

The guiding principles are:

- Keep changes minimal and auditable.
- Document every meaningful deviation from upstream Firefox.
- Prefer correctness and clarity over speed.

## Phase 0 — Project foundation

Establish the project so that work can proceed safely.

- Import the Firefox upstream source.
- Confirm that a vanilla Firefox build works before making changes.
- Set up the Sorlyn project structure (the `sorlyn/` and `docs/` directories).
- Add `README.md`, `NOTICE`, `TRADEMARKS.md`, and the initial documentation set.

At the end of Phase 0, the repository has a clear structure, licensing, and
documentation, without modifying Firefox internals.

## Phase 1 — Branding

Give Sorlyn its own visible identity.

- Define Sorlyn branding (name, identity, and visual direction).
- Replace visible product naming carefully, where Firefox branding would
  otherwise appear.
- Keep changes minimal and auditable, so each branding change is easy to review.

Branding work is described in [`BRANDING.md`](./BRANDING.md). Firefox and Mozilla
trademarks are not used as part of Sorlyn's branding; see
[`../TRADEMARKS.md`](../TRADEMARKS.md).

## Phase 2 — Privacy-focused defaults

Make privacy the default, transparently.

- Apply privacy-focused default settings.
- Document every changed default, including what it does and why it was chosen.

The goal is that a reader can audit exactly how Sorlyn's defaults differ from
upstream Firefox and understand the rationale for each.

## Phase 3 — Sorlyn Shield (prototype)

Prototype the native protection and ad-blocking layer.

- Prototype Sorlyn Shield.
- Start with network-level blocking.
- Add simple filter-list support.
- Provide a local allowlist.
- Provide a per-site disable option.

Design notes live in [`SORLYN_SHIELD.md`](./SORLYN_SHIELD.md). This phase is a
prototype; the emphasis is on a small, understandable implementation rather than
broad coverage.

## Phase 4 — Sorlyn Sync (exploration)

Explore optional synchronization.

- Explore Sorlyn Sync as an opt-in feature.
- Design it to be optional, encrypted, and privacy-first.
- Consider a self-hostable option.

Design notes live in [`SORLYN_SYNC.md`](./SORLYN_SYNC.md). Sync is explicitly
opt-in and is the most exploratory item on the roadmap; it may change
significantly or be deferred.

## Status

All phases beyond the project foundation are planning targets, not commitments
or release dates. Sorlyn is early-stage software and the roadmap will evolve.
