# Sorlyn Architecture

This document describes the high-level structure of the Sorlyn project and how
Sorlyn-specific code is intended to relate to the upstream Firefox codebase. It
is a living document and will grow as the project develops.

## Goals

- **Separation:** Keep Sorlyn-specific code and assets clearly separated from
  upstream Firefox source, so that the differences from upstream are easy to
  find, review, and maintain.
- **Auditability:** Make every deviation from upstream small and explainable.
- **Maintainability:** Reduce the cost of tracking upstream Firefox changes over
  time by keeping the Sorlyn surface area minimal.

## Foundation: Firefox / Gecko

Sorlyn is planned to be based on the Firefox open-source codebase, which is built
on the Gecko engine and is published by Mozilla under MPL-2.0. The Firefox
upstream source has not been imported yet; at this stage, Firefox internals are
**not** modified or renamed. Once imported, the upstream source is intended to be
treated as a foundation that Sorlyn builds on top of, rather than something to
fork and edit broadly.

## Project structure

The Sorlyn-specific parts of the repository are organized as follows:

```
sorlyn/
  branding/   Sorlyn branding and visual identity (names, assets, config)
  shield/     Sorlyn Shield: native protection / ad-blocking layer
  sync/       Sorlyn Sync: optional, encrypted, privacy-first sync

docs/
  ROADMAP.md        Phased development plan
  ARCHITECTURE.md   This document
  SORLYN_SHIELD.md  Sorlyn Shield design notes
  SORLYN_SYNC.md    Sorlyn Sync design notes
  BRANDING.md       Branding approach and guidelines
```

Keeping Sorlyn-specific work under `sorlyn/` makes it possible to answer the
question "what does Sorlyn change?" by looking in one place, supplemented by a
documented list of any changes that must live inside upstream files (for
example, branding strings).

## Components

### Sorlyn Shield

A native protection and ad-blocking layer. The intended starting point is
network-level blocking with simple filter-list support, a local allowlist, and a
per-site disable option. See [`SORLYN_SHIELD.md`](./SORLYN_SHIELD.md). Not yet
implemented.

### Sorlyn Sync

An optional, encrypted, privacy-first synchronization system, potentially
self-hostable and strictly opt-in. See [`SORLYN_SYNC.md`](./SORLYN_SYNC.md). Not
yet implemented.

### Branding

Sorlyn's name, identity, and visual direction, plus the documented approach for
replacing visible product naming carefully and auditably. See
[`BRANDING.md`](./BRANDING.md).

## Relationship to upstream

Where possible, Sorlyn intends to prefer configuration, additive modules, and
documented default changes over edits to upstream source. Any change that must
be made inside upstream files will be documented so that it can be re-applied and
reviewed when tracking newer Firefox releases.

## Status

This architecture is a starting point. As components are prototyped (see
[`ROADMAP.md`](./ROADMAP.md)), this document will be updated to reflect concrete
decisions rather than intentions.
