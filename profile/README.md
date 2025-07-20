# Silens – Decentralized AI Model Review & Governance

**Silens** is a community-driven Web3 platform for **auditing and governing AI models**.  
Users can submit AI models, test them with real prompts, and vote to approve, flag, or delist them — all powered by **CARV ID identity**, **on-chain smart contracts**, and deployed on **BNB Smart Chain**.

---

## Why Silens?

> What if AI systems could hallucinate facts — and no one could stop them?  
> What if public trust in AI depended on platforms that users couldn't control?

**Silens** offers a decentralized, transparent, and reputation-based alternative.

### What You Can Do
- Submit and explore AI models
- Review models with real inputs and outputs
- Vote on proposals to approve, flag, or remove unsafe models
- Build reputation through CARV ID to unlock governance roles

---

## Key Features

| Feature | Description |
|--------|-------------|
| **CARV ID Integration** | ERC-7231 identity and reputation NFT |
| **Model Submission** | Metadata + link to playground (e.g. Hugging Face) |
| **Review Engine** | Prompt → Output → Comment → Optional Screenshot |
| **Governance Layer** | On-chain voting to approve, flag, or delist |
| **Reputation & Badges** | Earn points, unlock roles (Trusted Reviewer, Governance Voter) |
| **Built on BNB Chain** | Deployed fully on BSC Testnet for governance execution |

---

## User Flow

1. **Mint CARV ID** (ERC-7231)
2. **Submit AI model** (metadata + link)
3. **Community reviews model** with prompts
4. **System auto-generates proposal**
5. **Governance voters vote** on result
6. **Proposal executed** → model status updated
7. **Reputation score increases**

## Tech Architecture
![image](https://res.cloudinary.com/dbllvvcv5/image/upload/v1722674273/github/uuhrys8ap3intzsmnwzx)
---

## Repo Structure

### `silens-contracts/` – Smart Contracts
- `ModelRegistry.sol`
- `ProposalVoting.sol`
- `ReputationSystem.sol`
- `CARVID.sol`
- Deployed on BNB Testnet (Chain ID: 97)

### `silens-indexer/` – Indexer/API Layer
- Real-time event processing
- IPFS storage & file mapping
- REST/GraphQL APIs via Hono
- PostgreSQL (Railway/Supabase)

### `silens-ui/` – Frontend App
- Model submission & review UI
- Proposal dashboard & governance voting
- Reputation dashboard + role gating

---

## Badge Roles

| Badge | Requirement | Power |
|-------|-------------|-------|
| VERIFIED_REVIEWER | 1 verified platform + CARV ID | Submit reviews |
| TRUSTED_REVIEWER | 30+ points | Elevated status |
| GOVERNANCE_VOTER | 50+ points | Vote on proposals |

---

## Smart Contract Addresses (BSC Testnet)

| Contract | Address |
|---------|---------|
| Silens (Main) | `0xCA18A11ca8e44c9eef603242Ef3cc92EE8BE12C2` |
| Model Registry | `0xEFEE9654334eE89A25021903B01AD840C7494dE2` |
| Reputation System | `0x8C0028B38c492A2F991dD805093C6712344D012F` |
| Proposal Voting | `0x0e6c055996E02b129B8b4d7cCE9210997e408c7E` |
| Identity Registry | `0x5EF386D8aF3b1709C4Ca0404A27E80B2d1206e38` |

[View Contracts on BSCScan](https://testnet.bscscan.com/address/0xCA18A11ca8e44c9eef603242Ef3cc92EE8BE12C2)

---

## API Endpoints (Indexer)

| Endpoint | Description |
|----------|-------------|
| `/models` | List all models |
| `/models/:id` | View model details |
| `/models/:id/reviews` | Get reviews for a model |
| `/users/:address` | Get user profile & points |
| `/proposals` | List proposals |
| `/proposals/:id` | Proposal details |
| `/proposals/:id/votes` | View votes |

---

## Track Alignment (FAIR3 × CARV)

### 🟦 **FAIR3 – Track 1.1: Technological Fairness**
- Promotes algorithmic transparency through community reviews
- Decentralized reputation system for AI oversight
- Verifiable model behavior and public trust mechanisms

### 🟨 **FAIR3 – Track 1.2: Community Infrastructure**
- Core modular system with reusable governance/review logic
- Supports open contribution and role gating
- Community collaboration with minimal barriers

### 🟧 **FAIR3 – Track 1.3: BNB Chain Integration**
- Fully deployed and governed on **BNB Chain**
- Explores fairness and transparency using BSC-native execution
- Uses BSC ecosystem standards for governance & composability

### 🟩 **CARV – Track 2.3: Modular Identity & Reputation**
- Implements **CARV ID (ERC-7231)** for user identity
- All reputation and voting is tied to that NFT
- Unlocks roles and access based on earned trust

### 🟪 **CARV – Track 2.4: AI × Web3 for Real-World Use Cases**
- Aims to make AI governance transparent, democratic, and fair
- Fully open-source and designed for real community use

---

## Live Demo

> Try the platform:  
**[https://silens.up.railway.app](https://silens.up.railway.app)**  
Connect your wallet, mint CARV ID, and test model review + governance live.

---

## Security Highlights

- Role-based access control in contracts
- Quorum-based on-chain proposal voting
- IPFS + data integrity checks
- ⚙Error handling + rate limiting in indexer
- Wallet-controlled interactions only

---

## Vision

> **Silens** is building a future where **AI is verifiable, transparent, and governed by the people**.  
This is just the beginning — join us in making AI fairer.
