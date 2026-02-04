# Permissionless Portfolio Margin 





import { Callout } from 'fumadocs-ui/components/callout';

<Callout type="info">
  **Status:** Coming soon
</Callout>

## What is Permissionless Portfolio Margin?

Portfolio margin lets you use assets like ETH, wstETH, or any supported ERC20 token as collateral for perps trading. Your spot holdings and perp positions are unified into a single account with one health ratio.

<img alt="Portfolio Margin" src={__img0} />

***

## Technical Details

Portfolio margin is built on [RIP-1: Modular Sub-accounts](/docs/risex/rips/rip-1) and integrates with Morpho Lite for permissionless lending markets. For the full technical specification including architecture, health calculations, and liquidation mechanics, see [RIP-2: Permissionless Portfolio Margin](/docs/risex/rips/rip-2).

<img alt="PPM Architecture" src={__img1} placeholder="blur" />

***

## Key Features

### Leverage Any ERC-20

Use any token as collateral for perps trading. As long as there's a Morpho market for it on RISE, you can leverage it.

### Permissionless Collateral Listing

New collateral types can be added without governance approval or whitelisting. Anyone can create a Morpho market, and once it meets liquidity thresholds, it becomes available for portfolio margin. The market decides what's valuable collateral.

### Secure by Design

Risk is isolated between RISEx and Morpho through composability. The portfolio margin system coordinates between protocols without modifying either one; each maintains its own security model and liquidation logic.
