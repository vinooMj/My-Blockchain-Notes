Coinbase recently released their Smart Wallet and is, I think, the best self-custodial embedded wallet solution out there! 🔑 Here is how it works..

(1) Upon sign up, the user will be prompted for biometrics and a passkey will be created.

(2) Coinbase then deploys a smart contract that pins (hardcodes) that passkey's public key as the authorized key for transactions.

(3) When the user wants to transact, the dApp will create a transaction and prompt the user for its biometrics.

(4) The biometrics will decrypt the passkey from the iCloud Keychain which is shared across devices.

(5) Upon decryption, the passkey then signs over an ERC-4337 compliant message (UserOperation) that contains the transaction details to execute, such as transferring 10 USDC to wallet 0xa901..bc.

(6) The UserOperation message then gets validated and packaged into a transaction in a private alternative mempool.

(7) The dApp can decide to sponsor the gas fees through paymaster to reduce friction from the experience.

(8) The smart contract validates the UserOperation format (calldata), nonce replays, and the signature.

(9) Signature validation includes unwrapping the signature data, determining if the signature is a classic Ethereum signature (secp256k1), or a WebAuthn signature (secp256r1), and verifying the signature accordingly against the authorized signing public key from step (2).

(10) Upon successful validation and verification of the message, the smart contract executes the transaction with the received information (calldata).

This means that:
• The user is the sole owner of the smart contract wallet.
• So long as the user doesn't wipe its passkey from their iCloud Keychain & Google Password Manager backup, they can access it.
• iCloud Keychain and Google Password Manager both have multiple levels of recovery accessible.
• You're not relying on any other intermediaries than Apple and Google to trust.
• There is no API key that puts the web3 app developer in the position of a custodian.
• There is no complex sharding of key shares from multi-party computation.
• You'd need at least 1 smart contract deployed by chain by user - it's downside for L1s or expensive L2s but required for gas sponsorship and transaction batching anyway.
• Users would have to delegate full temporary trust to the dApp with session keys if they do not want to constantly approve onchain actions with biometrics.
• Users trust Coinbase to deploy the smart contract with no backdoor (easy to verify the bytecode against the open source version).

Overall, pretty good choices made by Coinbase to make self-custody more usable and approchable in the embedded wallet space!
