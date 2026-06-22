# Sorlyn Browser

Sorlyn is an early, experimental web browser built on the Firefox open-source
codebase. It focuses on privacy-first defaults, a clean and maintainable
open-source architecture, and a distinct identity that is separate from Mozilla
and Firefox.

> **Project status: early / pre-alpha.**
> Sorlyn is currently in the project-scaffolding stage. There is no installable
> build yet, and the components described below are planned rather than
> implemented. This repository establishes the project structure, documentation,
> and licensing groundwork only.

## What Sorlyn is

- A Firefox-based browser fork with its own branding, identity, and roadmap.
- Privacy-focused by default, with the intent to document every changed default.
- Open source, licensed under the Mozilla Public License 2.0 (MPL-2.0) unless
  otherwise noted.

Sorlyn aims to be small, reviewable, and maintainable. Changes are intended to
be minimal and auditable so that anyone can understand how Sorlyn differs from
upstream Firefox.

## Relationship to Mozilla and Firefox

Sorlyn is an independent project. **Sorlyn is not affiliated with, sponsored by,
or endorsed by Mozilla.**

Sorlyn is built on the Firefox source code, which Mozilla publishes under the
Mozilla Public License 2.0. "Firefox" and "Mozilla" — including their associated
names and logos — are trademarks of the Mozilla Foundation. Those trademarks
belong to Mozilla and are not part of Sorlyn's branding.

Sorlyn uses its own branding, identity, and roadmap, and does not represent the
views of Mozilla. For details, see [`TRADEMARKS.md`](./TRADEMARKS.md) and
[`NOTICE`](./NOTICE).

## Planned components

### Sorlyn Shield

Sorlyn Shield is planned as a native protection and ad-blocking layer integrated
into the browser. The initial goal is network-level content blocking with
simple filter-list support, a local allowlist, and a per-site disable option.
Sorlyn Shield is not yet implemented. See
[`docs/SORLYN_SHIELD.md`](./docs/SORLYN_SHIELD.md).

### Sorlyn Sync

Sorlyn Sync is planned as an optional, encrypted, privacy-first synchronization
system, potentially self-hostable. It is intended to be strictly opt-in and is
not yet implemented. See [`docs/SORLYN_SYNC.md`](./docs/SORLYN_SYNC.md).

## Repository layout

```
.
├── sorlyn/              Sorlyn-specific project code and assets (planned)
│   ├── branding/        Sorlyn branding and visual identity
│   ├── shield/          Sorlyn Shield protection / ad-blocking layer
│   └── sync/            Sorlyn Sync optional private sync
├── docs/                Project documentation
│   ├── ROADMAP.md       Phased development plan
│   ├── ARCHITECTURE.md  High-level architecture and structure
│   ├── SORLYN_SHIELD.md Design notes for Sorlyn Shield
│   ├── SORLYN_SYNC.md   Design notes for Sorlyn Sync
│   └── BRANDING.md      Branding approach and guidelines
├── LICENSE              Mozilla Public License 2.0
├── NOTICE               Attribution and third-party notices
├── TRADEMARKS.md        Trademark policy and Mozilla/Firefox attribution
└── README.md            This file
```

The `sorlyn/` directory holds Sorlyn-specific work and is intentionally kept
separate from upstream Firefox source. Firefox internals are not modified or
renamed at this stage.

## Documentation

- [`docs/ROADMAP.md`](./docs/ROADMAP.md) — phased development plan.
- [`docs/ARCHITECTURE.md`](./docs/ARCHITECTURE.md) — how the project is
  structured and how Sorlyn-specific code relates to upstream.
- [`docs/SORLYN_SHIELD.md`](./docs/SORLYN_SHIELD.md) — Sorlyn Shield design
  notes.
- [`docs/SORLYN_SYNC.md`](./docs/SORLYN_SYNC.md) — Sorlyn Sync design notes.
- [`docs/BRANDING.md`](./docs/BRANDING.md) — branding approach and guidelines.

## License

Sorlyn is licensed under the Mozilla Public License 2.0 (MPL-2.0) unless
otherwise noted. See [`LICENSE`](./LICENSE) for the full text and
[`NOTICE`](./NOTICE) for attribution information.
