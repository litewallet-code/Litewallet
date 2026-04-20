# How to back up your LiteWallet

> 📖 Full step-by-step guide with screenshots at [litewallet.dev/guides/how-to-backup](https://litewallet.dev/guides/how-to-backup)

---

**This is the single most important step in self-custody.** If you lose access to your device without a backup, the LTC in your wallet is permanently unrecoverable. LiteWallet is non-custodial — no one, including us, can restore your funds.

## What you're backing up

When you create a LiteWallet wallet, the app generates a **12-word recovery phrase** (also called a seed phrase or mnemonic). This phrase is:

- The master key to your wallet
- Human-readable (English words from the BIP-39 standard)
- The only thing needed to restore your wallet on any compatible device
- **Never uploaded anywhere** — LiteWallet stores it only on your device

## The backup process

### Step 1: Open the recovery phrase view

On first setup, LiteWallet shows your 12-word phrase automatically. If you skipped it, you can view it later:

- **Settings** → **Security** → **View Recovery Phrase**
- Enter your device PIN to confirm

### Step 2: Write it down on paper

Use pen and paper. Not a computer. Not a screenshot. Not a photo. Not a cloud note.

- Each word in order, numbered 1 to 12
- Write clearly
- Use a pen that won't fade (not pencil, not erasable ink)
- Include a small label so you remember which wallet it belongs to

### Step 3: Verify what you wrote

Read your written copy back while comparing to the app. Confirm every word matches exactly. One wrong letter can make the backup useless.

### Step 4: Store it safely

Choose a location that is:

- **Physically secure** — fireproof safe, safety deposit box, or equivalent
- **Private** — where no guests, cleaners, or family can accidentally find it
- **Known only to you** — and optionally one trusted person (spouse, lawyer) who can access it if something happens to you
- **Not with your device** — defeats the purpose if both are destroyed together

### Step 5: Consider a second copy

Many users keep two copies in two separate secure locations. A house fire or flood can destroy both your device AND your single paper backup. Redundancy helps.

Metal backup products (engraved steel plates) offer protection against fire and water damage that paper doesn't. Consider one for significant holdings.

## What NOT to do

- **Don't type it into any website, email, or messaging app** — not even to yourself
- **Don't take a photo** — phones get stolen, cloud backups get hacked
- **Don't store it digitally in a "notes" app** — even encrypted ones
- **Don't share it with anyone claiming to be "support"** — LiteWallet support will NEVER ask for your recovery phrase
- **Don't split it into halves stored in different places** — the phrase has no meaningful protection when split like that; you just create two points of failure

## Testing your backup

Before relying on your backup, test it:

1. Install LiteWallet on a second device (or a test device)
2. Choose **Restore Wallet**
3. Enter your 12 words in order
4. Confirm the wallet shows your same addresses

If it works, your backup is verified. Erase the test installation afterward.

## If you lose your device

1. Install LiteWallet on a new device
2. Choose **Restore Wallet** on setup
3. Enter your 12-word recovery phrase
4. Your balance and transaction history appear automatically

This works because the phrase is a cryptographic seed — the same phrase always generates the same keys, and the same keys control the same LTC on the Litecoin blockchain.

## If you lose your recovery phrase

If you no longer have the recovery phrase AND you still have access to the original device, **immediately transfer your LTC to a new wallet with a fresh, properly backed-up recovery phrase.** If the device fails before you can do this, the funds are permanently unrecoverable.

---

## Read more

- **Full guide with screenshots:** [litewallet.dev/guides/how-to-backup](https://litewallet.dev/guides/how-to-backup)
- **Security model:** [litewallet.dev/security](https://litewallet.dev/security)
- **Recovering a wallet:** [litewallet.dev/recover](https://litewallet.dev/recover)
- **FAQ:** [litewallet.dev/faq](https://litewallet.dev/faq)
