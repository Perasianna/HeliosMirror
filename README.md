# HeliosMirror

Built for Base

HeliosMirror is a Base-focused repository that uses OnchainKit wallet UX alongside Viem RPC reads to reflect (“mirror”) the current Base network state in a simple browser interface.

It is intentionally scoped to infrastructure validation: chainId, latest block height, and native balance reads—plus clear Basescan references for deployment and verification.

## Networks

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

## What the App Does

Primary file: app/heliosMirror.ts

Runtime steps:
- Initializes OnchainKitProvider against the selected Base chain
- Presents wallet connection UI through OnchainKit
- Reads Base state using Viem:
  - RPC chainId
  - latest block number
  - native ETH balance for a provided address
- Keeps explorer context visible via Basescan URLs

## Repository Layout

app/  
- heliosMirror.ts  
  React component wiring wallet UX + Base JSON-RPC reads.

Common supporting files:
- package.json
- .env

## Libraries

OnchainKit  
https://github.com/coinbase/onchainkit  

Viem  
EVM client for Base JSON-RPC reads

## Installation and Running

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies using your preferred package manager and run using a standard React/Vite or Next.js dev server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL
- 
## Author

GitHub: https://github.com/Perasianna

Public contact (email): droplet_nuns0g@icloud.com 

Public contact (X): https://x.com/nurhafizatuliza

## License

MIT License

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0x57b2e395bb3cf38f45b972636c8eb5bc7bf1eaba

Deployment and verification:
- https://sepolia.basescan.org/address/0x57b2e395bb3cf38f45b972636c8eb5bc7bf1eaba
- https://sepolia.basescan.org/0x57b2e395bb3cf38f45b972636c8eb5bc7bf1eaba/0#code  


These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
