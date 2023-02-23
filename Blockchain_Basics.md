A blockchain is typically a bunch of computers (nodes) connected to each other. All of these computers contain the same information (e.g. a ledger of transactions). To "hack" this information, you will need to "hack" most of these computers at the same time. 

There are many blockchains in the world. The Bitcoin Blockchain is the first and oldest one. It records all transactions of the bitcoin cryptocurrency. Anyone can run a node of this blockchain. All you need is a computer with enough storage space and a strong Internet connection..

**A block is added to the block list if:

The block is the last one (previous index + 1);
The previous block is correct (previous hash == block.previousHash).
The hash is correct (calculated block hash == block.hash);
The difficulty level of the proof-of-work challenge is correct (difficulty at blockchain index n < block difficulty);
All transactions inside the block are valid;
The sum of output transactions are equal the sum of input transactions + 50 coins representing the reward for the block miner;
Check if there is a double spending in that block
There is only 1 fee transaction and 1 reward transaction.

**A transaction inside a block is valid if:**

The transaction hash is correct (calculated transaction hash == transaction.hash);
The signature of all input transactions are correct (transaction data signature can be verified with the public key of the address);
The sum of input transactions are greater than output transactions, it needs to leave some room for the transaction fee;
The transaction isn't already in the blockchain.
All input transactions are unspent in the blockchain.


Links
https://cryptomaniaks.com/guides/blockchain-for-dummies-ultimate-blockchain-101-guide

https://blog.coincodecap.com/blockchain-technology-and-crypto-vocabulary?utm_source=linkedin&utm_medium=social&utm_campaign=ReviveOldPost

https://alamhilaal.blogspot.com/2020/11/byzantine-general-blockchain.html
