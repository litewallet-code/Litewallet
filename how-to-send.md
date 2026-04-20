# How to send Litecoin from LiteWallet

> 📖 Full step-by-step guide with screenshots at [litewallet.dev/guides/how-to-send](https://litewallet.dev/guides/how-to-send)

---

Sending Litecoin from LiteWallet takes under a minute once you understand the basic flow. This guide walks through a standard send and notes the important checks to do along the way.

## Before you start

Have ready:
- The recipient's **Litecoin address** (or MWEB address, if sending privately)
- The **amount** you want to send
- Enough LTC in your wallet to cover the amount **plus the network fee**

## Sending a standard Litecoin transaction

### Step 1: Open the Send screen

Tap **Send** (or press Send from the main wallet view).

### Step 2: Enter the recipient address

You can:
- **Paste** the address from your clipboard
- **Scan a QR code** using your device camera
- **Type** the address manually (not recommended — one wrong character sends to the wrong destination)

Litecoin addresses start with `L`, `M`, or `ltc1` (for SegWit). MWEB addresses are longer and start with `ltcmweb`.

**Always verify the address matches what the recipient gave you.** Copy-paste malware can silently replace addresses in your clipboard with an attacker's address.

### Step 3: Enter the amount

Type the amount in LTC. LiteWallet shows:
- The equivalent in your chosen fiat currency
- The current network fee estimate
- Your remaining balance after the transaction

### Step 4: Review and confirm

LiteWallet shows a confirmation screen with:
- Recipient address (the full address, not truncated)
- Amount in LTC
- Network fee
- Total deducted from your balance

Read this screen carefully. **Transactions on Litecoin are irreversible.** Once broadcast, there is no "undo."

### Step 5: Authorize

Depending on your security settings:
- **PIN** — Enter your wallet PIN
- **Biometric** — Use Face ID, Touch ID, or fingerprint
- **Hardware wallet** — Connect and confirm on the device

LiteWallet signs the transaction locally and broadcasts it to the Litecoin network.

### Step 6: Wait for confirmation

The recipient sees the transaction as "unconfirmed" immediately. It typically takes 2–3 minutes for the first confirmation.

- **0 confirmations** — Transaction broadcast, visible on block explorers
- **1 confirmation** — Mined into a block, secure enough for most purposes
- **6 confirmations** — ~15 minutes, recommended for large amounts or exchange deposits

## Sending privately via MWEB

To send a confidential transaction:

1. Make sure you have a MWEB balance (peg-in first if you don't — see [How to use MWEB](https://litewallet.dev/guides/how-to-use-mweb))
2. Tap **Send** and choose **MWEB** as the source
3. Enter a MWEB address (starts with `ltcmweb`)
4. The transaction amount and addresses will be confidential on-chain

**Note:** The recipient must also be able to receive MWEB. Most exchanges accept only standard Litecoin addresses — for those, peg out to a standard address first.

## Fees

LiteWallet estimates fees automatically based on current network conditions. Typical Litecoin network fees are under $0.01 — drastically lower than Bitcoin.

For most users, the default fee is correct. Advanced users can adjust the fee in **Settings → Advanced**.

## Common issues

**"Insufficient balance" but I have enough LTC**  
The amount includes the fee. If your balance is exactly the send amount, there's nothing left for the fee. Reduce the send amount slightly or receive more LTC.

**"Invalid address"**  
Check that the full address was pasted correctly. Missing characters at the beginning or end will fail validation.

**Transaction pending too long**  
If confirmations are slow (over 30 minutes), network congestion may be unusually high. The transaction will eventually confirm. For stuck transactions, see [Troubleshooting](https://litewallet.dev/support/troubleshoot).

## Safety tips

- **Test with a small amount first** if sending to a new address
- **Double-check the first and last 4 characters** of the address before confirming
- **Never share your recovery phrase** — no one legitimate will ever ask for it
- **Be wary of unexpected payment requests** — scam patterns include urgency, threats, or impersonation

---

## Read more

- **Full send guide:** [litewallet.dev/guides/how-to-send](https://litewallet.dev/guides/how-to-send)
- **How to receive:** [litewallet.dev/guides/how-to-receive](https://litewallet.dev/guides/how-to-receive)
- **How to use MWEB:** [litewallet.dev/guides/how-to-use-mweb](https://litewallet.dev/guides/how-to-use-mweb)
- **What is MWEB?** [what-is-mweb.md](./what-is-mweb.md)
- **Security:** [security.md](./security.md)
- **Back to README:** [README.md](./README.md)
