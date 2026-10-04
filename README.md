## 💧 Add Your Solana Token to a Liquidity Pool — Raydium 2025 Tutorial
A complete, step-by-step guide to making your custom Solana token tradable by adding it to a Raydium liquidity pool.

This tutorial builds on the previous Solana Token Tutorial (non–Token-2022 version).
If you haven’t yet created your token, complete that guide first before proceeding.

All steps are verified on Mainnet-Beta (Raydium does not support Devnet).

## 🧩 Step-by-Step Tutorial
## ⚙️ 1️⃣ What You’ll Learn
By the end of this tutorial, you’ll know how to:
Understand what a liquidity pool and AMM (Automated Market Maker) are
Mint your token on mainnet-beta
Add a Raydium liquidity pool pairing your token with SOL
View your new market on Dexscreener and Jupiter
Give your token its first real market value

## 💡 2️⃣ What You’ll Need
Before starting, make sure you have:
✅ Phantom Wallet (set to Mainnet-Beta)
✅ SOL in your wallet (~0.05 SOL or about $7 for all fees)
✅ Your mint address for the token you created earlier
✅ Optional: your token logo and metadata hosted on Storacha

## 🪙 3️⃣ Mint Your Token on Mainnet-Beta
If your existing token was created on Devnet, it won’t appear on Raydium.
You’ll need to mint a real token on mainnet first.
```bash
solana config set --url https://api.mainnet-beta.solana.com
```
Create or use a clean mainnet wallet:
```bash
solana-keygen new --outfile ~/.config/solana/mainnet.json
solana config set --keypair ~/.config/solana/mainnet.json
```
Fund it with a small amount of SOL from an exchange.














