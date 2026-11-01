# Bbillionaire site

This static page is published with GitHub Pages from `contract/web`. It currently has no smart contract address or ABI configured.

To connect a contract again, add its address and ABI to the page and set the network the contract is deployed on.

## GitHub Pages deployment

The repository includes `.github/workflows/deploy-pages.yml`, which publishes `contract/web` when changes are pushed to `main` or when manually run from GitHub Actions. The repository root `index.html` is a copy of the same page.

No private key, wallet seed phrase, or server-side secret is required. GitHub Pages serves the site over HTTPS.
