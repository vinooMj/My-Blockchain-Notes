1. ACCOUNT TYPES:

- External accounts: controlled by public-private key pairs, address determined from the public key.

- Contract accounts: controlled by the code stored with the account, address determined at the creation time.

2. TRANSACTIONS

Messages sent from one account to another one

It can include:
- Binary data (payload)
- Ether

If the target account contains code, that code is executed. The payload is provided as input data.

If the target account is not set, a new contract is created.

3. GAS

A transaction is charged with gas. 

First, a gas price is set by the creator, at gas_price * gas cost.

If some gas is left after the execution, it's refunded.

If the gas is used up at any point, an exception is triggered, and all the modifications are reverted.

4. STORAGE

It's a key-value store that maps 256-bit words to 256-bit words 

Each account has persistent storage between function calls & transactions.

It's not possible to enumerate storage from within a contract, it's costly to read, and even more to initialize and modify it.

5. MEMORY

Contract's space instance for each message call

Memory can be addressed at byte level:
- Reads are limited to 256 bits
- Writes can be 8 bits/256 bits

Memory is expanded on access by a 256-bit, and the gas cost must be paid at expansion time (it scales quadratically)

6. STACK

The EVM is a stack machine:  all computations are performed on a data area (the stack).

Max size of 1024 elements with 256-bits words 

Possible actions:
- copy one of the topmost 16 elements to the top of the stack
- swap the topmost element with one of the 16 below

7. STACK COMPLEX OPERATIONS

Other ops take the topmost 2 elements from the stack and push the result onto it

Stack elements can be moved to storage/memory to get deeper access

It's not possible to just access arbitrary elements in the stack without first removing the top

8. INSTRUCTION SET

All instructions operate on 256-bit words, or on memory slices. 

Arithmetic, bit, logical, comparison operations are present.

Conditional/unconditional jumps are possible
 
Contracts can access relevant properties of the current block (number, timestamp,...)

9. MESSAGE CALLS

Similarly to transactions, they have:
- source
- target
- data
- payload
- Ether
- gas
- return data

Transaction:a top-level msg call that can create further message calls

Contracts can call other contracts or send Ether to non-contract accounts with msg calls

10. DELEGATECALL

A a msg call variant,BUT:
- target address code executed on calling the contract context
- msg.sender/msg.value don't change values

A contract can dynamically load code from a different address at runtime

Storage, address, balance refer to the calling contract

11. LOGS

Data can be stored in a specially indexed data structure that maps all the way up to the block level 

Contracts cannot access log data after creation, but they can be efficiently accessed from outside the blockchain

This feature is used by Solidity to implement events

12. CREATE CALLS

Contracts can create other contracts using a special opcode.

Differences between create calls and normal message calls:
- the payload data is executed
- the result is stored as code
- the caller/creator receives the address of the new contract on the stack

13. SELF DESTRUCT

Operation on contract's address to remove code from the blockchain

- the Ether is sent to a designated target 
- storage and code are removed from the state 

Removing the contract is dangerous: if someone sends Ether to removed contracts, the Ether is lost.

14. DEACTIVATE 

If you want to deactivate your contracts, you should instead disable them by changing some internal state which causes all functions 
to revert. This makes it impossible to use the contract, as it returns Ether immediately.

15. PRECOMPILED CONTRACTS

Contract addresses with ranges 1-8 are special.

They can be called like any other contract, but their behavior and gas cost is not defined by EVM code stored at that address but implemented 
in the EVM execution environment itself.
