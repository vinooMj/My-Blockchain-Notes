
How do they work?
.
The diagram below shows a side-by-side comparison of DNS and ENS.

DNS (Domain Name Service) acts as an 𝐚𝐝𝐝𝐫𝐞𝐬𝐬 𝐛𝐨𝐨𝐤. It translates human-readable domain names (google.com) to machine-readable IP addresses (142.251.46.238).

ENS (Ethereum Name Service) is a naming system based on the 𝐄𝐭𝐡𝐞𝐫𝐞𝐮𝐦 𝐛𝐥𝐨𝐜𝐤𝐜𝐡𝐚𝐢𝐧. It translates human-readable a domain name (abc.eth) to a blockchain address (0x9876…).

DNS operates based on 3 levels of DNS servers:
Root Name Server
TLD (Top Level Domain) Name Server
Authoritative Name Server
For example, ‘www.google.com’ is recursively resolved to 142.251.46.238.

ENS operates based on 𝐭𝐰𝐨 𝐭𝐲𝐩𝐞𝐬 𝐨𝐟 𝐬𝐦𝐚𝐫𝐭 𝐜𝐨𝐧𝐭𝐫𝐚𝐜𝐭𝐬:
𝐑𝐞𝐠𝐢𝐬𝐭𝐫𝐲 - It specifies the owner and resolver addresses for each domain name. 
For example, when we type ‘abc.eth’ in crypto wallet MetaMask, MetaMask asks the registry what the owner address for ‘abc.eth’ is. The registry returns the owner 
address 0x1234.

𝐑𝐞𝐬𝐨𝐥𝐯𝐞𝐫 - It returns the actual Ethereum blockchain address. 
For example, the resolver for ‘eth’ domain name is at address 0x1234 and calling the smart contract at 0x1234 returns the actual address 0x9876 for ‘abc.eth’.

Just like we can buy domain names on GoDaddy, we can buy ENS domain names at https://app.ens.domains/ with ETH.
