# LiteWallet FAQ

> 📖 Full FAQ with 20+ questions at [litewallet.dev/faq](https://litewallet.dev/faq)

---

## General

### Is LiteWallet free?

Yes. LiteWallet is free to download and use on every platform. You only pay standard Litecoin network fees (typically under $0.01) when sending transactions. There are no subscription fees, no transaction fees charged by LiteWallet, and no accounts.

### Is LiteWallet open source?

Yes. The source code is available on GitHub under the MIT License.

### Is LiteWallet custodial?

No. LiteWallet is **non-custodial**. Your private keys are stored locally on your device and never uploaded to any server. No one — including LiteWallet — can access your funds. This also means no one can recover your wallet for you if you lose your recovery phrase.

### What platforms does LiteWallet support?

All five major platforms: **Windows, macOS, Linux, iOS, and Android**. The wallet identity (keys, balance, transaction history) works identically across platforms — restore the same recovery phrase on any device to access the same wallet.

## Security

### Where are my private keys stored?

Locally on your device, encrypted and protected by your device's security features (Face ID, Touch ID, Secure Enclave on iOS/macOS, Android Keystore). Keys are never transmitted over the network.

### What is the 12-word recovery phrase?

It's a human-readable cryptographic seed that generates all your wallet's keys. Anyone with the phrase can fully restore your wallet on any compatible device. This is why you must store it securely and never share it.

### Does LiteWallet support hardware wallets?

Yes. LiteWallet supports Ledger and Trezor hardware wallets. When paired, your private keys stay on the hardware device — LiteWallet acts as the interface, but signing happens on the secure hardware.

## MWEB

### What is MWEB?

MWEB (MimbleWimble Extension Block) is Litecoin's optional privacy layer. Transactions inside MWEB have confidential amounts and unlinked addresses. It activated on Litecoin in May 2022.

Read more: [What is MWEB?](./guides/what-is-mweb.md)

### Do MWEB transactions cost more than standard Litecoin transactions?

Comparable. MWEB transactions carry standard Litecoin network fees, similar to non-MWEB transactions. Peg-in and peg-out each count as on-chain transactions with standard fees.

### How fast are MWEB transactions?

Same as standard Litecoin — confirmations follow the 2.5-minute block time. Your MWEB balance updates as soon as the transaction confirms.

### Can I send MWEB directly to an exchange?

Most exchanges accept only standard Litecoin addresses. To deposit to an exchange, peg out from MWEB to a standard Litecoin address first, then send to the exchange.

## Technical

### What's LiteWallet's relationship to Litecoin Core?

LiteWallet is an SPV (Simplified Payment Verification) wallet. It doesn't run a full Litecoin node — instead it connects to trusted nodes to verify transactions cryptographically without storing the entire blockchain. This keeps the wallet lightweight and fast.

### Does LiteWallet support Tor?

Yes. You can route LiteWallet's network connections through Tor for additional network-level privacy. See **Settings → Advanced → Tor**.

### What's the latest version?

See the [Changelog](./changelog.md) or [litewallet.dev/changelog](https://litewallet.dev/changelog).

## Support

### How do I get help?

- **Support guides:** [litewallet.dev/support/troubleshoot](https://litewallet.dev/support/troubleshoot)
- **FAQ:** [litewallet.dev/faq](https://litewallet.dev/faq)
- **Community:** [Discord](https://discord.gg/litecoin) or [X/Twitter](https://x.com/LiteWallet)

### Who can I contact about a security issue?

See [security disclosure process](./security.md).

### Will LiteWallet ask for my recovery phrase?

**Never.** LiteWallet support will never ask for your recovery phrase, private keys, or password. Anyone asking for these is attempting to steal from you. Report suspected phishing to the official channels above.

---

## Read more

- **Full FAQ:** [litewallet.dev/faq](https://litewallet.dev/faq)
- **Guides:** [litewallet.dev/guides](https://litewallet.dev/guides)
- **Download:** [litewallet.dev/download](https://litewallet.dev/download)
