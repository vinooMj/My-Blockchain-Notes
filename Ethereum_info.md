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


Data storage in Ethereum Blockchain
Ethereum implements a trie data structure to manage temporary and permanent data. The three types of trie data structures in the Ethereum Blockchain are State Trie, Storage Trie and Transaction Trie.

A mined and confirmed transaction is recorded in the transaction trie.

Temporary data like the above mentioned local variables and account addresses are stored in the state trie where it changes and gets updated continuously, thereby updating the state of the complete Ethereum Blockchain.

State trie
There is one global state trie in Ethereum that is constantly updated. It contains a key-value pair, where a key is the address of an Ethereum account and value is the Recursive-Length Prefix (RLP) encoded value of nonce, balance, storageRoot, the hash of an account on Ethereum network.
Storage trie
A storage trie is where all of the contract data is stored. Each Ethereum account has its own storage trie. A 256-bit hash of the storage trie’s root node is stored as the storageRoot value in the global state trie.
Transaction trie
The path to a specific transaction in the transaction trie is via (the RLP encoding of) the index of where the transaction sits in the block. Mined blocks are never updated; the position of the transaction in a block is never changed. This means that once you locate a transaction in a block’s transaction trie, you can return to the same path over and over to retrieve the same result.

Geth uses LevelDB because LevelDB is implemented in GO, has key-value pairs and includes modern data storage (i.e. multiple layers on disk, organized in the background)

------------

 EIP-170 which added a smart contract size limit of 24.576 kb.
 
 ------
 validation - check prev hash next hash, check bal, check identity with public key
 validation - Block validation, transaction validation
  Every block receiver validation the transaction then added to blockchain 
  Block validator - create block add header.
  
  -----------------
  EIP - miners voting
  Soft fork(solidity updates) - hard fork (major updates).
  -----------------
  Ethereum transaction sign
  password -> hash -> private key -> address
-------------------------------------------
Ethereum's "The Surge" will aim to improve Ethereum’s throughput from around 15 transactions per second (TPS) to about 100,000 TPS while reducing transaction fees, it added.

--------------------------------
npx create-web3-dapp - dapp creation in cli
