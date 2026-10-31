# Bbillionaire dApp

This static wallet interface connects to the contract deployed at `0x685F81de76BdabE79d8Ea5804EeA3c6E711ED514` on Ethereum Mainnet (chain ID 1) and supports the contract's `USDT_ERC20` and `GC_ADDRESS` tokens. It reads account balances, deposit limits, investments, and accrued income; requests a token allowance when needed; and supports deposits and withdrawals. The contract ABI lives in `abi.js`.

## Before publishing

1. Verify the contract address, network, token addresses, and deployed bytecode on [Etherscan](https://etherscan.io/address/0x685F81de76BdabE79d8Ea5804EeA3c6E711ED514).
2. The Solidity source in `../contracts/Bbillionaire.sol` does **not** match the ABI supplied for this interface. Do not publish this interface for transactions until you confirm the deployed bytecode at the address matches the supplied ABI.
3. Review the deposit, approval, referral, and withdrawal behavior on Ethereum Mainnet before inviting users.

## GitHub Pages deployment

The repository includes `.github/workflows/deploy-pages.yml`, which publishes `contract/web` when changes are pushed to `main` or when manually run from GitHub Actions.

1. Push this project to a GitHub repository, keeping the workflow at the repository root and this site in `contract/web`.
2. In the repository, open **Settings → Pages** and set the build/deployment source to **GitHub Actions**.
3. Push to `main`; the workflow deploys the site. Its URL appears in the workflow run and the Pages settings.

No private key, wallet seed phrase, or server-side secret is required. GitHub Pages serves the site over HTTPS, which browser wallet providers require.

The page loads ethers.js from cdnjs. For production, vendor a reviewed build locally or add a verified Subresource Integrity hash for the pinned CDN asset.
