# 💧 Add Your Solana Token to a Liquidity Pool — Raydium 2025 Tutorial
A complete, step-by-step guide to making your custom Solana token tradable by adding it to a Raydium liquidity pool.

This tutorial builds on the previous Solana Token Tutorial (non–Token-2022 version).
If you haven’t yet created your token, complete that guide first before proceeding.

All steps are verified on Mainnet-Beta (Raydium does not support Devnet).
# 🧩 Step-by-Step Tutorial

# ⚙️ 1️⃣ What You’ll Learn
By the end of this tutorial, you’ll know how to:

Understand what a liquidity pool and AMM (Automated Market Maker) are
Mint your token on mainnet-beta
Add a Raydium liquidity pool pairing your token with SOL
View your new market on Dexscreener and Jupiter
Give your token its first real market value

# 💡 2️⃣ What You’ll Need
Before starting, make sure you have:

✅ Phantom Wallet (set to Mainnet-Beta)
✅ SOL in your wallet (~0.05 SOL or about $7 for all fees)
✅ Your mint address for the token you created earlier
✅ Optional: your token logo and metadata hosted on Storacha

# 🪙 3️⃣ Mint Your Token on Mainnet-Beta

If your existing token was created on Devnet, it won’t appear on Raydium.
You’ll need to mint a real token on mainnet first.

solana config set --url https://api.mainnet-beta.solana.com

solana-keygen new --outfile ~/.config/solana/mainnet.json
solana config set --keypair ~/.config/solana/mainnet.json






spl-token create-token --program-id TokenzQdBNbLqP5VEhdkAS6EPFLC1PHnBqCXEpPxuEb --enable-metadata --decimals 9

spl-token create-account <MINT_ADDRESS>

spl-token mint <MINT_ADDRESS> 1000000





https://explorer.solana.com/address/<MINT_ADDRESS>?cluster=mainnet







spl-token accounts





Token                                         Balance
------------------------------------------------------------
5G2Jf9jP...xyz (MyToken Token)               1000000


















https://storacha.network/ipfs/<IMAGE_CID>


{
  "name": "MyToken Token",
  "symbol": "MTK",
  "description": "Example token created on Solana.",
  "image": "https://storacha.network/ipfs/<IMAGE_CID>",
  "attributes": [
    { "trait_type": "Type", "value": "Utility" }
  ],
  "properties": {
    "files": [
      {
        "uri": "https://storacha.network/ipfs/<IMAGE_CID>",
        "type": "image/png"
      }
    ]
  }
}






https://storacha.network/ipfs/<NEW_METADATA_CID>






spl-token initialize-metadata <MINT_ADDRESS> "MyToken Token" "MTK" "https://storacha.network/ipfs/<NEW_METADATA_CID>"





spl-token update-metadata <MINT_ADDRESS> "MyToken Token" "MTK" "https://storacha.network/ipfs/<UPDATED_METADATA_CID>"























https://dexscreener.com/solana/<YOUR_TOKEN_MINT>




https://jup.ag/swap/<YOUR_TOKEN_MINT>-So11111111111111111111111111111111111111112





