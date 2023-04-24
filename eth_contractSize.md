It's quite imperative for you as a 
Smart Contract Developer to always be within the Smart Contract Bytecode size limit.

Wait, What's Bytecode?
𝙎𝙞𝙢𝙥𝙡𝙮 𝙥𝙪𝙩 - 𝙃𝙪𝙢𝙖𝙣𝙨 𝙪𝙣𝙙𝙚𝙧𝙨𝙩𝙖𝙣𝙙 𝙎𝙤𝙡𝙞𝙙𝙞𝙩𝙮, 𝙗𝙪𝙩 𝙀𝙑𝙈 𝙪𝙣𝙙𝙚𝙧𝙨𝙩𝙖𝙣𝙙𝙨 𝘽𝙮𝙩𝙚𝙘𝙤𝙙𝙚.

Bytecode is the low-level language that our solidity smart contracts get translated to.
It represents a long sequence of machine codes or opcodes, pieces of instructions, that must be executed by the EVM to get the desired outputs.

What's the Size Limit? 
Every blockchain has a limit on the max size of the contract that can be deployed.

In Ethereum, after the implementation of EIP170, the maximum bytecode size is 24.576 kilobytes.

𝙒𝙝𝙖𝙩 𝙙𝙤𝙚𝙨 𝙩𝙝𝙞𝙨 𝙢𝙚𝙖𝙣 𝙛𝙤𝙧 𝙮𝙤𝙪 𝙖𝙨 𝙖 𝙎𝙤𝙡𝙞𝙙𝙞𝙩𝙮 𝘿𝙚𝙫𝙚𝙡𝙤𝙥𝙚𝙧?
Well, if your smart contract bytecode exceeds this threshold, you shall not be able to deploy your contract on-chain.

Therefore it's crucial to learn optimization techniques so that smart contracts can stay within the𝟐𝟒.𝟓𝟕𝟔 𝐊𝐁 size limit without breaking intended functionality.

Well, this is easier said than done since we might need large contracts for our intended use-cases.

However, with sufficient knowledge of optimizing contract bytecode size, we can write smart contracts to fit our needs without surpassing the bytecode threshold.

Some of these optimization tricks to keep in mind 
 Start using Libraries: Using a library in a smart contract can help reduce the size of the bytecode because it allows code reusability.

 Use smaller data types: Use smaller data types such as uint8, uint16, and uint32 instead of uint256 whenever possible.

 Shorter error messages should be preferred: Using long error messages in require statements can inflate the bytecode size.

 Use of Custom errors: For solidity versions of 0.8.4 or more, prefer replacing error messages with custom errors. They are ABI-encoded as selectors and therefore help in the optimization.

 Minimize code redundancy: Avoid writing repetitive code and reuse existing code as much as possible.

 Optimize code logic: Optimize the code logic to reduce the number of instructions required to execute the Smart Contract.

 Replacing Modifires with Private Function - 𝘔𝘰𝘳𝘦 𝘰𝘯 𝘵𝘩𝘪𝘴 𝘪𝘯 𝘵𝘩𝘦 𝘯𝘦𝘹𝘵 𝘱𝘰𝘴𝘵. 𝘛𝘩𝘪𝘴 𝘪𝘴 𝘪𝘯𝘵𝘦𝘳𝘦𝘴𝘵𝘪𝘯𝘨.

Tools you may need
We now have access to various tools to monitor their Smart Contract bytecode size during development, like:
 𝙝𝙖𝙧𝙙𝙝𝙖𝙩-𝙘𝙤𝙣𝙩𝙧𝙖𝙘𝙩-𝙨𝙞𝙯𝙚𝙧 provides details and warnings about contract sizes in a hardhat project
 𝙩𝙧𝙪𝙛𝙛𝙡𝙚-𝙘𝙤𝙣𝙩𝙧𝙖𝙘𝙩-𝙨𝙞𝙯𝙚 displays the contract size of all or a selection of your contracts in kilobytes.

Developers can optimize Smart Contract performance and avoid bytecode size limits by reducing Smart Contract bytecode usage and monitoring Smart Contract size during 
development using tools.
