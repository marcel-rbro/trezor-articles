# SLIP39 and its implementation on Trezor wallets

SLIP39, or Shamir's Secret Sharing for Mnemonic Codes, is a cryptographic protocol that splits a cryptocurrency wallet's recovery seed into multiple shares for secure distribution. To restore the wallet, a predefined minimum number of these shares must be combined, enhancing both security and recoverability. It is used in Trezor hardware wallets to provide flexible, customizable, and resilient backup solutions.

> On this page:
> 
> - [How does SLIP39 work?](#how-does-slip39-work)
> - [What are the differences between SLIP39 and BIP39?](#what-are-the-differences-between-slip39-and-bip39)
> - [How to use SLIP39 on Trezor wallets?](#how-to-use-slip39-on-trezor-wallets)
> - [Where can I find more information about SLIP39?](#where-can-i-find-more-information-about-slip39)

## How does SLIP39 work?

The process to create a set of mnemonic words works as follows:

1. A secret value called Master Secret (MS) is encrypted using a passphrase to create an Encrypted Master Secret (EMS).
2. The EMS is then split into a number of shares which are encoded as a set of mnemonic words. Each set of words represents one share.
3. The individual mnemonic words can be stored together. However, you can also store each mnemonic word individually or in sets of words.

To recover a SLIP39 secret, you need a predefined number of shares (known as a threshold) from all the words.

## What are the differences between SLIP39 and BIP39?

BIP39 uses a mnemonic seed phrase of 12 or 24 words to for wallet backup and recovery. However, to recover a wallet protected by BIP39, you need all of the mnemonic words. If you lose a single word, you need to try all of the combinations to guess the lost word. As a result, you need to store all of the words in every backup location.

On the other hand, SLIP39 splits the passphrase multiple words, but a pre-defined amount of words is required to recover the secret. For example, you can select 5 shares, with only 3 required to recover the wallet. This way you can store the shares of words individually or in sets of multiple shares. If someone finds one of the backup locations, they are not able to recover your wallet. Additionally, if one of the locations is destroyed, you are still able to recover the wallet using the remaining locations.

## How to use SLIP39 with Trezor wallets?

Using SLIP39 on Trezor wallets is simple. Follow these steps to get from a brand new Trezor wallet to a secure environment for your coins:

1. Set up your Trezor wallet.

    [![Setup your Trezor wallet video](https://img.youtube.com/vi/HuVH_9hnUu8/0.jpg)](https://www.youtube.com/watch?v=HuVH_9hnUu8)

2. Choose SLIP39 when asked to create a backup of your wallet.
3. Configure the number of shares and threshold.
    - Selecting higher threshold improves security (chances of someone maliciously restoring your wallet), but lowers resilience (chances of losing access to the wallet). A good middle ground is having 5 shares with a threshold of 3.
4. Write down the shares and store them in a secure location or in multiple locations.
5. It is recommended to test your recovery method regularly. Make sure that the medium which holds the shares is not degrading.

## Where can I find more information about SLIP39?

Visit the following pages for more information about SLIP39:

- [Trezor Firmware documentation](https://docs.trezor.io/trezor-firmware/core/misc/slip0039.html)
- [SatoshiLabs SLIPs repository](https://github.com/satoshilabs/slips/blob/master/slip-0039.md)
- [Trezor Learn article about SLIPs and BIPs](https://trezor.io/learn/a/what-are-bips-slips)