# Dada Udyogini — clickable prototype

A tap-through prototype of the three Dada Udyogini apps — **Buyer, Seller and
Admin** — in one self-contained HTML file. Open it on any phone, tablet or
laptop. Nothing to install, no sign-in, no backend.

**Live:** https://ramanbyte.github.io/DadaUDYOGINI/

## What it is

54 screens, 256 tap targets. The screens are not drawings: they are screenshots
of the **real apps running** in their demo build (mock data, no server), and the
tap targets sit exactly where the app's own buttons sit.

- Tap a button and it navigates where the app navigates. The bottom nav bar
  works on every screen.
- Tap anywhere else and every tap target flashes, so nobody has to hunt for
  what is clickable.
- The URL carries the screen (`…#buyer/checkout`), so a single screen can be
  linked to, and Back behaves.
- **All screens** opens a thumbnail index of all 54, grouped by app.

| App | Screens |
| --- | --- |
| Buyer | 22 — browse, cart, checkout, orders, returns, wishlist, profile |
| Seller (Artisan) | 16 — dashboard, KYC, listings, orders, earnings |
| Admin | 16 — approvals, catalogue, orders, returns, oversight |

## What it is not

It is a prototype, not the product. It cannot type, scroll or compute — tapping
a mapped button jumps to the screen that button leads to, and that is all. A
handful of buttons are deliberately inert rather than guess a destination.

To *drive* the real thing, run the demo build of the apps themselves.

## Files

| File | |
| --- | --- |
| `prototype.html` | The prototype. Everything is inlined — screens included. 2.7 MB. |
| `index.html` | Redirects the site root to `prototype.html`. |
| `.nojekyll` | Stops GitHub Pages running its Jekyll pass over the site. |

Generated from the app source by `tools/wireframe/` in the main repository —
`capture.js` drives the running demo build and records every screen and every
tappable, and `build_prototype.py` assembles this file. Re-running them
regenerates the prototype from whatever the apps look like that day.
