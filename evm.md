EVM
Every Ethereum node runs on the EVM to maintain consensus across the blockchain.

Ethereum has its own native cryptocurrency (Ether) that follows almost exactly the same intuitive rules, it also enables a much more powerful function: smart contracts. For this more complex feature, a more sophisticated analogy is required. Instead of a distributed ledger, Ethereum is a distributed state machine. Ethereum's state is a large data structure which holds not only all accounts and balances, but a machine state, which can change from block to block according to a pre-defined set of rules, and which can execute arbitrary machine code. The specific rules of changing state from block to block are defined by the EVM.
This means that the machine code is completely isolated from the network, filesystem or any processes of the host computer. Every node in the Ethereum network runs an EVM instance which allows them to agree on executing the same instructions. The EVM is Turing complete, which refers to a system capable of performing any logical step of a computational function. JavaScript, the programming language which powers the worldwide web, widely uses Turing completeness.
Ethereum Virtual Machines have been successfully implemented in various programming languages including C++, Java, JavaScript, Python, Ruby, and many others.
Smart contract languages like Solidity cannot be executed by the EVM directly. Instead, they are compiled to low-level machine instructions (called opcodes).

EVM uses a set of instructions (called opcodes) to execute specific tasks. At the time of writing, there are 140 unique opcodes.

Security

The EVM is a security oriented virtual machine, designed to permit untrusted code to be executed by a global network of computers. To do so securely, it imposes the following restrictions:
Every computational step taken in a program's execution must be paid for up front, thereby preventing Denial-of-Service attacks.
Programs may only interact with each other by transmitting a single arbitrary-length byte array; they do not have access to each other's state.
Program execution is sandboxed; an EVM program may access and modify its own internal state and may trigger the execution of other EVM programs, but nothing else.
Program execution is fully deterministic and produces identical state transitions for any conforming implementation beginning in an identical state.



https://moralis.io/evm-explained-what-is-ethereum-virtual-machine/
https://www.bitrates.com/guides/ethereum/what-is-the-unstoppable-world-computer
https://www.coding-bootcamps.com/blog/how-ethereum-virtual-machine-works.html

Core:
https://github.com/ethereum/go-ethereum/tree/master/core/vm
GitHub - pirapira/awesome-ethereum-virtual-machine: Ethereum Virtua…
