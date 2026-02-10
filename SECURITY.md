# Security Policy

**Last updated:** February 2025

SHUNYATA ($SHUN) is a community-driven Solana meme token launched fairly through Pump.fun with a focus on transparency, anti-rug mechanisms, and on-chain philanthropy.

**Important:** This project **does not** currently include any custom on-chain programs (smart contracts) deployed by the core team. The token was created and launched via Pump.fun's standard bonding curve mechanism. Therefore, most traditional smart contract security concerns (reentrancy, overflow, access control bugs, etc.) do **not** apply to SHUNYATA itself.

The primary security surfaces are:

- The official multi-signature wallet that receives the philanthropy/DAO portion of transaction fees
- Off-chain components (website, Discord community links, future DAO tooling if any)
- Phishing / impersonation attacks targeting the community
- Supply-chain / dependency risks if any open-source tooling is later added to this repository

## Supported Versions

Because SHUNYATA is a launched token on Solana with immutable token contract (via Pump.fun), **there are no versioned releases of code that can be patched**. Once deployed, Solana token contracts cannot be upgraded unless explicitly designed that way (which Pump.fun tokens are not).

| Component              | Status          | Security Updates Possible? | Notes                                      |
|------------------------|-----------------|-----------------------------|--------------------------------------------|
| Token contract         | Immutable       | No                          | Standard Pump.fun deployment               |
| Multi-sig treasury     | Active          | Partially (signer changes)  | Community-governed multi-sig               |
| Website (GitHub Pages) | Active          | Yes                         | Hosted from this repo                      |
| Future DAO interfaces  | Not yet active  | Yes (when implemented)      | If/when added to this repository           |

## Reporting a Vulnerability

**We take security seriously — even for a meme project.**

Please **do NOT** open public issues or discuss potential vulnerabilities in public channels (Twitter/X, Discord, etc.).

Preferred reporting channels (in order of preference):

1. **Private email**  
   → shunyata.security@proton.me  
   (or another secure email alias you prefer — update this address)

2. **Encrypted message**  
   If you have a PGP key you’d like us to use, please include it in your first message.

3. **GitHub private vulnerability reporting** (recommended once enabled)  
   If this repository enables GitHub's private vulnerability reporting feature, use that.

**What to include in your report:**

- Clear description of the issue
- Step-by-step reproduction (if applicable)
- Screenshots / transaction signatures / Solana explorer links
- Potential impact (financial, reputation, user funds, etc.)
- Any suggested mitigation
- Your contact preference / PGP key (optional)

We will acknowledge receipt within 48 hours and aim to provide an initial assessment within 7 days.

## Scope

**In scope**

- Phishing sites / fake websites / impersonating social accounts using official branding
- Vulnerabilities in the multi-sig wallet configuration (if exploitable via signers or on-chain logic)
- Malicious code / backdoors introduced in this GitHub repository
- XSS / open redirects / content spoofing on https://insanitychain.github.io/SHUNYATA/
- Leaked private keys / signer keys attributable to project communications

**Out of scope**

- Pump.fun platform vulnerabilities (report directly to Pump.fun)
- Solana blockchain / runtime / consensus issues
- Standard MEV / sandwich attacks / front-running (inherent to public blockchains)
- Social engineering of community members
- "Theoretical" governance attacks without concrete exploit path
- Issues already known and accepted (e.g., immutable token metadata, standard SPL token risks)

## Security-related Best Practices (for community & future contributors)

- **Never share your seed phrase or private key** — no legitimate team member or bot will ever ask for it.
- Verify contract addresses and links **only** from pinned messages in official Discord / official website.
- Use hardware wallets for any significant holdings.
- Be extremely cautious of DMs, airdrop links, "verification" requests, etc.
- If building tools / bots / dashboards that interact with SHUNYATA — treat all on-chain data as untrusted.

## Bug Bounty (when applicable)

At this time we do **not** operate a paid bug bounty program due to the project's fair-launch meme nature and lack of custom smart contracts.

If the project evolves to include custom programs, audited interfaces, or significant treasury value under active management, we intend to launch a public bug bounty program (likely through Immunefi, HackenProof or similar).

Thank you for helping keep the SHUNYATA community safe and the void harmonious.

Om Śūnyatā
