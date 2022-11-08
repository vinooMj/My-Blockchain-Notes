a private key is generated using the seed integer (which is obtained from the secret recovery phrase) using the SHA256 hash function
the corresponding public key for the private key is derived from the private key using the ECDSA (Elliptic Curve Signature) algorithm.
from the public key derived, compute a keccak256 hash
from the keccak256 hash, take the last 20 bytes (which is 40 hexadecimals), prefix it with “0x” and this is your Ethereum address

Creating the Default Account
With the public/private key pair created from the seed integer, MetaMask will now be able to create your first account (created by default when you install MetaMask). 
As explained,
your first account is generated from the keccak256 hash.

Internally, MetaMask encrypts your private key using the password that you supplied during the installation stage, and stores it in your browser’s data store. 
It does not store them on the cloud.

Creating Additional Accounts
Here comes the interesting part. How does MetaMask create additional accounts (after the first default account)? Turns out that MetaMask makes use of the private key 
of the first account and hashes it to get the next private key. Using the newly created private key, the same procedure applies (as described earlier) to get the public
key and subsequently the account address. And the next account is always the hash of the previous private key.
