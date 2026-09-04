# DA-COMPUTER.github.io

A minimal redirect site. Visitors land here for a couple seconds, then get
sent to the real portfolio at [dacomputercode.dev](https://dacomputercode.dev).

## How it works

- `index.html` redirects via JavaScript after a ~2 second delay, styled as a
  small terminal-style "console" (deep/light purple + white, monospace type)
  while it redirects.
- A `<meta http-equiv="refresh">` tag is included as a fallback for
  crawlers or visitors with JavaScript disabled.
- A visible "Go to the portfolio" link is always available in case the
  redirect doesn't fire.

## Deploying with GitHub Pages

This repo is named `DA-COMPUTER.github.io`, so GitHub Pages will serve it
automatically at `https://da-computer.github.io/` once Pages is enabled:

1. Push this repo to GitHub as `DA-COMPUTER.github.io` (public repo).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
4. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
5. Wait a minute or two, then visit `https://da-computer.github.io/` to
   confirm the redirect works.

## Updating the destination

To point somewhere else later, change the URL in two places in
`index.html`:

- The `<meta http-equiv="refresh" content="2; url=...">` tag
- The `setTimeout(...)` call near the bottom of the file
