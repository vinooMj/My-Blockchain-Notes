Smart contract data storage
When a smart contract is created or when a transaction awakens it, the contract’s code can read and write to its storage space. Here’s a breakdown of its Storage Specifications:

It’s a big dictionary (key-value store) that maps keys to values.
Keys are strings of 32 bytes. We can have 232 x 8 bits = 2256 different keys. Same for values.
It’s like Redis, RocksDB or LevelDB storage.
DAPP and Smart Contracts function in a similar way to a hard-drive storage in a regular program.

2256 keys x 32 bytes (values) is around 1063 PETABYTES. You would need several billions of times the age of the universe to go through this amount of data with an SSD.
Basically, we can safely assume that there’s no storage limit for a DAPP.
But there is a cost(gas)
-----------------------------------------------------------

