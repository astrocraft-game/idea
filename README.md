# astrocraft

This folder contains the astrocraft design documentation in mdBook format.

At the highest level, the game is about an ascended human mind in a **Mind Disk** rebuilding physical industry against **Dark Flux**. The design is organized around four major scopes, each with two operational layers, forming a nested drill-down hierarchy:

```
S2 Sector → S1 Star → O1 Orbit → O2 Station / P2 Planet
    → P1 Region → E1 Cell → E2 Quantum
```

Navigation is entity-driven: click an entity → "Enter" to go deeper, back button to go up.

The detailed design lives in [`idea/book/src/`](./book/src). Start with [`idea/book/src/SUMMARY.md`](./book/src/SUMMARY.md).

## Building with mdBook

This folder includes a `book/book.toml` and `book/src/SUMMARY.md`, so it is ready for mdBook layout.

Typical commands:

```bash
cd idea/book
mdbook build
```

Or for local preview:

```bash
cd idea/book
mdbook serve --open
```
