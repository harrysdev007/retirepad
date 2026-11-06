# RETIREPAD

React frontend with a local Vite API for the official Pump SDK.

## Run locally

npm install
npm run dev -- --port 5188

Optional server variable: SOLANA_RPC_URL. Defaults to the public Solana mainnet RPC.

The local API reads supported quote assets from Pump mainnet, enriches labels through Dexscreener, and prepares and simulates creation transactions for wallet signing. No private wallet keys are stored. A publicly hosted metadata URI is currently required; automatic media upload is not implemented.

Token creation, fee rates and holder rewards remain subject to the live Pump program rules. The proposed RETIREPAD weekly rewards, buybacks and fixed starting market cap are not implemented. Submitted transactions are stored locally; the launched-token index is not connected yet.

Build: npm run build

The API middleware currently runs with the local Vite server. Production hosting requires a separate backend deployment; a static dist upload alone does not provide these endpoints.
