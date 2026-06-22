# Sorlyn Branding

This document describes how Sorlyn approaches branding and identity. It covers
the principles and the intended process. Concrete branding assets and naming
changes are introduced in later phases (see [`ROADMAP.md`](./ROADMAP.md)).

## Why Sorlyn has its own branding

Sorlyn is a distinct project with its own name, identity, and roadmap. A clear,
separate identity:

- Avoids confusion with Firefox and Mozilla.
- Respects Mozilla's trademarks (see [`../TRADEMARKS.md`](../TRADEMARKS.md)).
- Gives Sorlyn a stable identity to build on.

**Sorlyn is not affiliated with, sponsored by, or endorsed by Mozilla.** Firefox
and Mozilla names and logos are trademarks of the Mozilla Foundation and are not
used as part of Sorlyn's branding.

## Principles

- **Distinct identity.** Sorlyn uses its own name and visual direction rather
  than Firefox or Mozilla branding.
- **Careful replacement.** Visible product naming is replaced deliberately, not
  in bulk. Each change should be understandable on its own.
- **Minimal and auditable.** Branding changes are kept small so reviewers can
  see exactly what changed and why.
- **No premature changes.** At this stage, Firefox internals are not renamed or
  modified. Branding work begins in Phase 1.

## Scope of branding work

When branding work begins, it is expected to cover, at minimum:

- The product name shown to users.
- Visible naming in the user interface and about pages.
- Application metadata where a product name is presented to the user.

The `sorlyn/branding/` directory is reserved for Sorlyn branding assets and
configuration as they are created.

## Process

The intended process for replacing visible product naming:

1. Identify where Firefox branding appears to users.
2. Replace it with Sorlyn branding in small, reviewable changes.
3. Record what changed, so the set of branding modifications stays auditable and
   can be re-applied when tracking upstream updates.
4. Avoid touching unrelated code in the same change.

## Status

Planning only. No branding assets or naming changes have been introduced yet.
This document will be updated with concrete guidelines (naming, colors,
logos, usage rules) once branding is defined in Phase 1.
