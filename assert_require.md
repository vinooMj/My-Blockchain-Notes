This post is about an imperative change in Solidity's assert() statement that most Smart Contract developers are perhaps still unaware of.

Additionally, it seems quite a few Solidity articles around this topic are outdated, and most of them aren’t updated yet.

𝙒𝙝𝙖𝙩 𝘿𝙤 𝙬𝙚 𝙠𝙣𝙤𝙬 𝙨𝙤 𝙛𝙖𝙧?
One of the major differences that you might have known between assert() and require() statements in solidity is that:
▶️ If assert() statements fail, they consume all of the Gas provided in a transaction
▶️ If require() statements fail, they refund the remaining gas back to the caller

𝙒𝙝𝙖𝙩 𝘾𝙝𝙖𝙣𝙜𝙚𝙙?
Well, since solidity version 0.8.0, this difference is no more true.

Because after the launch of solidity 0.8.0, the behavior of assert() statements has changed.

After solidity 0.8.0, the 𝐚𝐬𝐬𝐞𝐫𝐭() 𝐬𝐭𝐚𝐭𝐞𝐦𝐞𝐧𝐭 𝐝𝐨𝐞𝐬𝐧'𝐭 𝐜𝐨𝐧𝐬𝐮𝐦𝐞 𝐚𝐥𝐥 𝐠𝐚𝐬 𝐢𝐧 𝐚 𝐭𝐫𝐚𝐧𝐬𝐚𝐜𝐭𝐢𝐨𝐧. It now 𝐫𝐞𝐭𝐮𝐫𝐧𝐬 𝐭𝐡𝐞 𝐫𝐞𝐦𝐚𝐢𝐧𝐢𝐧𝐠 𝐠𝐚𝐬 𝐛𝐚𝐜𝐤 𝐭𝐨 𝐭𝐡𝐞 𝐬𝐞𝐧𝐝𝐞𝐫.
---
Let's dive into the details and understand Why?
To begin with, you first need to understand the difference between two specific opcodes in the EVM, i.e., 𝙄𝙉𝙑𝘼𝙇𝙄𝘿 & 𝙍𝙀𝙑𝙀𝙍𝙏.

 𝐈𝐍𝐕𝐀𝐋𝐈𝐃: As per this opcode, the EVM must revert all state changes and consume all the gas sent in a transaction. No gas refunds for the sender of transactions.
𝐑𝐄𝐕𝐄𝐑𝐓: As per this opcode, the EVM must revert all state changes as well but it should also return the remaining gas to the sender.

Now, in previous versions of Solidity, the assert() function used the INVALID opcode, which consumed all remaining gas in a transaction upon execution.

This behavior lead to issues like limiting the gas refunds for users and complicating debugging due to the lack of information provided by the INVALID opcode.

However, since Solidity version 0.8.0, the assert() function now uses the REVERT opcode, which does not consume all gas in a transaction but actually returns any remaining gas to the transaction's sender.

With this change, the REVERT opcode now allows for better gas management, providing users with greater control over their gas usage.

This change has made it possible for developers to design more complex and gas-efficient smart contracts, which can lead to cost savings for both developers and users.

In the image below, see how the assert() statement takes all gas with solidity version 0.6.11 but refunds back gas with version 0.8.17.

---
Note for Solidity Devs 📝
It's imperative for you as a smart contract developer to keep up with the latest changes in the language, as solidity evolves quite rapidly.
