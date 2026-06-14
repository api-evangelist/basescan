# Basescan

Base L2 blockchain explorer with a REST API for querying Base network transactions, token balances, smart contract ABIs, and ERC-20 transfer events.

Basescan is operated by the Etherscan team and serves as the canonical block explorer for the Base L2 network (chain ID 8453). The API is fully compatible with Etherscan API V2, allowing developers to access Base alongside 50+ other EVM chains using a single API key.

**Developer Portal:** https://docs.basescan.org  
**API Reference:** https://docs.etherscan.io/etherscan-v2  
**API Key Registration:** https://basescan.org/myapikey  
**Pricing:** https://etherscan.io/apis?id=8453

## API Capabilities

- **Accounts** — Native token balances (single/multi-address), historical balances, token holdings (ERC-20/721/1155), address metadata and name tags
- **Transactions** — Normal, internal, and token transfer history; transaction status and receipt checks
- **Blocks** — Block details, rewards, uncle blocks, validation history, and network statistics
- **Tokens** — ERC-20/721/1155 supply, holder lists, transfer history, and token metadata
- **Smart Contracts** — ABI retrieval, source code, contract verification (Solidity, Vyper, Stylus, zkSync)
- **Gas** — Gas oracle, current prices, historical daily averages
- **Event Logs** — Filtered log queries by address and topic
- **Ethereum RPC** — Standard `eth_` methods for block data, transaction execution, and gas estimation

## Authentication

All requests require an API key passed as the `apikey` query parameter. Register at [basescan.org/myapikey](https://basescan.org/myapikey). For Etherscan V2 multi-chain requests, include `chainid=8453` to target the Base network.

## Plans

| Plan | Price/mo | Calls/sec | Calls/day |
|------|----------|-----------|-----------|
| Free | $0 | 3 | 100,000 |
| Lite | $49 | 5 | 100,000 |
| Standard | $199 | 10 | 200,000 |
| Advanced | $299 | 20 | 500,000 |
| Professional | $399 | 30 | 1,000,000 |
| Pro Plus | $899 | 30 | 1,500,000 |
| Enterprise | Custom | Unmetered | Unmetered |

## Repository Structure

```
apis.yml               # APIs.json 0.19 provider profile
plans/plans.yml        # Pricing plan details
rate-limits/rate-limits.yml  # Rate limit tiers and error codes
finops/finops.yml      # FinOps guidance and cost drivers
```
