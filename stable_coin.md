What is a 𝐬𝐭𝐚𝐛𝐥𝐞𝐜𝐨𝐢𝐧?
Is it going to change the payment flow? 

The diagram below shows how fiat-backed stablecoin USDC is created and destroyed.

𝐅𝐢𝐚𝐭 → 𝐒𝐭𝐚𝐛𝐥𝐞𝐜𝐨𝐢𝐧
Step 0 - A ERC-20 smart contract is deployed on the blockchain, with stablecoin token detail.

Step 1 - Bob transfers $100 from his fiat wallet to the custodian (a bank or a trust company) who maintains the fiat reserve for the stablecoin issuer, 
in exchange for 100 USDC.

Step 2 - The custodian confirms the transaction and asks the stablecoin issuer to mint and transfer stablecoins.

Steps 3 and 4 - The stablecoin issuer mints new tokens and transfers them to Bob’s crypto wallet. It is called “𝐬𝐭𝐚𝐛𝐥𝐞” because it is 1:1 pegged to USD.

Steps 5 and 6 - A 3rd-party auditor audits the reserves in the custodian and the tokens in the smart contract. It makes sure the tokens are fully backed 
by fiat money or short-term bills. In USDC’s case, the reserve contains 22.4% cash and 77.6% T-bills (low risk) as per the audit report.

𝐒𝐭𝐚𝐛𝐥𝐞𝐜𝐨𝐢𝐧 → 𝐅𝐢𝐚𝐭
Steps 1 and 2 - Bob transfers 100 USDC to the issuer in exchange for $100. The issuer burns 100 USDC by calling the smart contract.

Steps 3 and 4 - The issuer confirms the transaction and asks the custodian to transfer $100 to Bob’s fiat wallet.

How does stablecoin change the payments? 
Bob can easily transfer the 100 USDC to his friend’s crypto wallet via blockchain transaction. There is no need to go through the banking systems or 
payment gateways/processors. Then Bob’s friend can exchange the USDC tokens for his local currency via an exchange.
