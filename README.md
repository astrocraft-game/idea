# astrocraft

This folder contains the astrocraft design documentation in mdBook format.

At the highest level, the game is about an ascended human mind in a **Mind Disk** rebuilding physical industry against **Dark Flux**. The design is organized around three major scopes, each with two operational layers:

- planetary
- space station
- interplanetary frontier

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
