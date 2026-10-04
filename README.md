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

## 🧱 Mint tokens
Create your token mint
```bash
spl-token create-token --program-id TokenzQdBNbLqP5VEhdkAS6EPFLC1PHnBqCXEpPxuEb --enable-metadata --decimals 9
```
Create a token account for your wallet
```bash
spl-token create-account <MINT_ADDRESS>
```
Mint your initial supply
```bash
spl-token mint <MINT_ADDRESS> 1000000
```

## 🔍 4️⃣ Verify Your Token on Explorer
Before attaching metadata, let’s make sure your token was created successfully and that your wallet holds the minted supply.
## ✅ Check on Solana Explorer
Visit:
```bash
https://explorer.solana.com/address/<MINT_ADDRESS>?cluster=mainnet
```
You should see your Token Mint Account details, including:

Total supply (e.g., 1,000,000)

Mint authority (your wallet address)

Decimals (9)
Click “Token Accounts” and confirm your wallet address appears there as the owner with your full balance.

## 🧠 Optional CLI Verification
You can also confirm it via Solana CLI:
```bash
spl-token accounts
```
This shows all tokens your wallet holds.

Look for your mint address and verify the correct balance.


Example output:
```bash
Token                                         Balance
------------------------------------------------------------
5G2Jf9jP...xyz (MyToken Token)               1000000
```
✅ That confirms your token exists and is in your wallet.
## 💡 Tip
If you open Phantom and don’t see your token yet:

Click “+” → “Import Token” → paste your mint address.

Or use Solflare, which often displays metadata faster.

## 🧾 5️⃣ Add Metadata (via Storacha)
You’ll now attach your metadata and image to your token using Storacha for decentralized IPFS hosting.











