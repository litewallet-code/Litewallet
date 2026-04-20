# What is MWEB?

> 📖 This is a summary. The full guide, interactive examples, and FAQ are on the website.  
> **Read the canonical version at [litewallet.dev/guides/mweb](https://litewallet.dev/guides/mweb)**

---

MWEB stands for **MimbleWimble Extension Block**. It's the optional privacy layer that activated on Litecoin in May 2022, adding confidential transactions — hidden amounts and unlinked addresses — as a per-transaction choice.

## The short version

- **What it does:** Hides transaction amounts and sender/receiver addresses for MWEB transactions
- **When it activated:** May 20, 2022, at block 2,257,920
- **How to use it:** Opt-in per transaction. You choose MWEB when sending from a compatible wallet.
- **Not a separate coin:** The LTC moving through MWEB is the same LTC as the rest of the Litecoin chain.
- **The same 84 million supply cap** applies to both the standard ledger and MWEB combined.

## How it works

MWEB adds a second "lane" to the Litecoin chain running alongside the main ledger:

1. **Pedersen commitments** hide transaction amounts while proving inputs equal outputs
2. **One-time addresses** unlink senders and receivers — no address is reused on-chain
3. **Transaction aggregation** merges multiple transactions into one block-level blob
4. **Kernels** — small public proofs that each transaction was valid

An observer can see that an MWEB transaction happened, but cannot see how much was sent or which addresses were involved.

## Peg-in and peg-out

MWEB is a separate block from the standard Litecoin ledger. Moving LTC between the two:

- **Peg-in** — Standard ledger → MWEB (visible on the standard ledger)
- **Peg-out** — MWEB → Standard ledger (visible on the standard ledger)

What happens **inside** MWEB between peg-in and peg-out is confidential.

For maximum privacy:
- Delay between peg-in and peg-out
- Peg out to a different address than you pegged in from
- Split or combine amounts across multiple pegs

## MimbleWimble origins

MimbleWimble is a cryptocurrency protocol first described in a July 2016 anonymous whitepaper under the pseudonym "Tom Elvis Jedusor" (French for "Tom Marvolo Riddle," a Harry Potter reference).

Two standalone cryptocurrencies implemented MimbleWimble as their base protocol — Grin and Beam, both launched in January 2019. Litecoin took a different approach: MimbleWimble as an **optional extension** rather than the entire chain.

## Wallets supporting MWEB

As of 2026, MWEB is supported in:

- **LiteWallet** — Windows, macOS, Linux, iOS, Android (every platform)
- **Cake Wallet** — macOS, Linux, iOS, Android (no Windows)
- **Litecoin Core** — Recent versions, desktop only

Most multi-coin wallets (Exodus, Trust Wallet, Atomic, Coinbase Wallet) do not support MWEB and treat Litecoin as a standard-ledger-only asset.

## Limitations

MWEB makes transactions **inside** the extension block confidential. It does **not** hide peg-in and peg-out events, which remain visible on the standard Litecoin ledger.

MWEB is a meaningful privacy upgrade — not perfect anonymity. For strong privacy, combine MWEB with good operational practices (delays, address separation, amount fragmentation).

---

## Read more

- **Full guide with examples:** [litewallet.dev/guides/mweb](https://litewallet.dev/guides/mweb)
- **How to use MWEB:** [litewallet.dev/guides/how-to-use-mweb](https://litewallet.dev/guides/how-to-use-mweb)
- **MWEB in LiteWallet:** [litewallet.dev/features/mweb](https://litewallet.dev/features/mweb)
- **FAQ:** [litewallet.dev/faq](https://litewallet.dev/faq)
