# promo-blocker.github.io

> Public website for Promo Blocker, served by GitHub Pages at https://promo-blocker.github.io. Hosts the privacy policy for Promoted Post Hider for Reddit.

## Pages

| URL | File | Purpose |
| --- | --- | --- |
| https://promo-blocker.github.io/ | `index.html` | Landing page |
| https://promo-blocker.github.io/privacy/ | `privacy/index.html` | Privacy policy linked from the Chrome Web Store listing |

## How it is built

Plain HTML and one stylesheet. No build step, no scripts, no third-party assets. `.nojekyll` tells GitHub Pages to serve the files as-is.

## Editing

1. Change the HTML or `styles.css`.
2. Open the file in a browser to check it.
3. Open a pull request. Pages redeploys from `main` after merge.

The privacy policy wording must stay in sync with the extension's behavior. If the extension ever gains a permission or collects anything, update the policy and the effective date in the same change.

## Development

See [CONTRIBUTING guidelines in CLAUDE.md](CLAUDE.md) for the development workflow: every change starts as a GitHub issue, lands via a reviewed pull request, and updates the [CHANGELOG](CHANGELOG.md).

## License

MIT
