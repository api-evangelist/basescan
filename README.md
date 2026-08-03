# Basescan

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
