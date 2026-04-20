# LiteWallet Security

> 📖 Full security page at [litewallet.dev/security](https://litewallet.dev/security)

---

## Security model

LiteWallet is designed around the principle that **you and only you** control your funds. This means:

- Private keys are generated on your device
- Keys never leave your device
- No server, account, or third party can recover your wallet
- No one can freeze, reverse, or block your transactions

This model provides strong guarantees — no intermediary can steal from you or be compelled to give up your funds — but it also puts full responsibility for security on you.

## How keys are protected

### Generation
Keys are generated using cryptographically secure random number generation on your device. The 12-word recovery phrase is derived using BIP-39 (the same standard used by most major wallets).

### Storage
- **iOS / macOS** — Keys stored in the Secure Enclave when available, encrypted with device-level keys
- **Android** — Keys stored in the Android Keystore, hardware-backed where available
- **Windows / macOS / Linux desktop** — Keys stored encrypted in the local app data, protected by your wallet PIN/password

### Transmission
Private keys are **never transmitted** over the network. All transaction signing happens locally on your device. LiteWallet only sends the final signed transaction to the Litecoin network.

## Network privacy

### SPV + header validation
LiteWallet is a light client. It downloads block headers and verifies transactions cryptographically without syncing the full Litecoin blockchain.

### Tor support
LiteWallet can route its network connections through Tor, hiding your IP address from the nodes it connects to. Enable in **Settings → Advanced → Tor**.

### MWEB for on-chain privacy
For confidential transaction amounts and unlinked addresses, use MWEB. See [What is MWEB?](./what-is-mweb.md).

## Open source

LiteWallet's source code is available on GitHub under the MIT License. This means:

- Anyone can audit the code for vulnerabilities
- Builds can be reproduced from source
- The community can verify the wallet does what it claims

## Your responsibilities

Self-custody puts you in charge, which means these things matter:

1. **Back up your recovery phrase** — see [How to back up](./how-to-backup.md)
2. **Protect the recovery phrase** — never digitally, never shared, never in the cloud
3. **Keep your device secure** — enable device-level encryption, use a strong PIN or password
4. **Verify addresses before sending** — copy-paste malware exists
5. **Keep LiteWallet updated** — security fixes go out with new versions
6. **Watch for phishing** — LiteWallet support will NEVER ask for your recovery phrase

## Threats and mitigations

| Threat | Mitigation |
|---|---|
| **Lost device** | Restore from 12-word recovery phrase on any compatible device |
| **Stolen device without PIN** | Device encryption + wallet PIN protects funds |
| **Phishing site pretending to be LiteWallet** | Always download from litewallet.dev directly |
| **Clipboard malware replacing addresses** | Verify full address before confirming send |
| **Social engineering for recovery phrase** | Never share the phrase, regardless of who asks |
| **Physical theft of paper backup** | Store in a secure location, consider metal backup for fire/water resistance |
| **Supply chain attack on binaries** | Verify download checksums against [litewallet.dev/download](https://litewallet.dev/download) |

## Reporting a security vulnerability

Found a security issue in LiteWallet? Please report it responsibly:

1. **Do not** publicly disclose the issue before we've had a chance to address it
2. **Do** report details via the contact methods on [litewallet.dev](https://litewallet.dev)
3. We aim to acknowledge reports within 48 hours
4. Coordinated disclosure timelines typically range from 30–90 days depending on severity

We credit security researchers who report vulnerabilities responsibly, unless they prefer to remain anonymous.

## What LiteWallet cannot protect you from

To be fully transparent about the limitations:

- **Physical compromise of your unlocked device**
- **Observing you type your PIN over your shoulder**
- **Social engineering where you willingly share your recovery phrase**
- **Exchanges or services where you deposit LTC** (LiteWallet's protection ends once you send funds to a custodial service)
- **Smart contract or DeFi risks** if you bridge LTC to other chains

## Auditing

LiteWallet's code is open source and can be audited by anyone. Community review is ongoing. For the current status of any formal audit reports, see [litewallet.dev/security](https://litewallet.dev/security).

---

## Read more

- **Full security page:** [litewallet.dev/security](https://litewallet.dev/security)
- **How to back up:** [how-to-backup.md](./how-to-backup.md)
- **Wallet recovery:** [litewallet.dev/recover](https://litewallet.dev/recover)
- **FAQ:** [faq.md](./faq.md)
- **Back to README:** [README.md](./README.md)
