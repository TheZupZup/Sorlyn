# Sorlyn Shield

Sorlyn Shield is the planned native protection and ad-blocking layer for the
Sorlyn browser. This document captures the design intent. **Sorlyn Shield is not
yet implemented**; nothing here should be read as a description of current
behavior.

## Goals

- Provide built-in content blocking as a first-class, native part of the
  browser rather than relying solely on add-ons.
- Default to privacy-respecting behavior while remaining transparent and
  controllable.
- Stay small and understandable, especially in the early prototype.

## Planned scope (initial prototype)

The first prototype is intentionally limited:

- **Network-level blocking.** Block requests to known advertising and tracking
  endpoints at the network layer.
- **Simple filter-list support.** Load and apply basic filter lists. The initial
  focus is on a straightforward, well-understood subset rather than full
  compatibility with every filter syntax.
- **Local allowlist.** Let users maintain a local list of domains or sites that
  should never be blocked.
- **Per-site disable option.** Let users turn Shield off for an individual site
  when it interferes with functionality.

## Non-goals (for now)

- Full parity with established, mature blocking engines.
- Cosmetic / element-hiding rules beyond what is needed for the prototype.
- Remote or cloud-based configuration. Shield's configuration is intended to be
  local by default.

## Design principles

- **Transparency.** It should be clear what is blocked and why, and easy to
  inspect or override.
- **User control.** Allowlisting and per-site disabling are core features, not
  afterthoughts.
- **Local-first.** Filter lists and user preferences should work without
  requiring an account or external service.
- **Minimal footprint.** Keep the implementation auditable and maintainable; it
  should be possible to reason about Shield's behavior from a small amount of
  code.

## Open questions

These will be resolved during the prototype (see Phase 3 of
[`ROADMAP.md`](./ROADMAP.md)):

- Which filter-list format(s) to support first, and how strictly.
- How and when filter lists are updated, and whether updates are manual or
  automatic by default.
- How Shield interacts with Firefox's existing content-blocking facilities.
- How allowlist and per-site state are stored and surfaced in the UI.

## Status

Planning only. Implementation will begin as a prototype during Phase 3 and will
be documented here as decisions are made.
