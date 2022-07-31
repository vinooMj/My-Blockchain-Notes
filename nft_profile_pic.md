Reddit and Twitter announced support for 𝐍𝐅𝐓 𝐩𝐫𝐨𝐟𝐢𝐥𝐞 𝐩𝐢𝐜𝐭𝐮𝐫𝐞𝐬.
What are the differences between NFT (Non-Fungible Token) profile pictures and regular profile pictures?

The diagram below shows the differences.

𝐑𝐞𝐠𝐮𝐥𝐚𝐫 𝐩𝐫𝐨𝐟𝐢𝐥𝐞 𝐩𝐢𝐜𝐭𝐮𝐫𝐞𝐬
🔹Step 1: The user needs to upload a profile picture, and this request goes to the user service.
🔹Step 2: The picture is stored in an object store, like Amazon S3. A URL is generated to visit the file.
🔹Step 3: A new entry in the database is created to store the picture’s metadata.

𝐍𝐅𝐓 𝐩𝐫𝐨𝐟𝐢𝐥𝐞 𝐩𝐢𝐜𝐭𝐮𝐫𝐞𝐬
🔹Step 1: To understand the step, we should know what smart contracts are. Smart contracts are programs deployed and stored on blockchains. 
They are self-executing once the pre-determined conditions are met. We call the smart contract function to mint the NFT. 

The mint function inputs include the picture file, name, and description. The mint function returns with the new token ID, metadata URI, and 
the NFT URI on IPFS (InterPlanetary File System). Let’s go through the outputs one by one.

Token ID is a unique ID for the NFT picture. There is a dictionary in the smart contract to store each token ID and its owner’s address. That’s 
why NFT is called “Non-Fungible Token”. Each picture is assigned with a unique ID.

Metadata and the profile pictures are stored on IPFS. IPFS is a peer-to-peer network for storing and sharing data in a distributed filesystem. 
It is an important extension for the blockchains because we cannot store all the data on blockchains. IPFS leverages 𝐂𝐨𝐧𝐭𝐞𝐧𝐭 𝐀𝐝𝐝𝐫𝐞𝐬𝐬𝐢𝐧𝐠 to make sure 
the generated URI is linked to the file content. No one can replace or alter the file content without breaking the link.

The generated metadata URIs are stored in another dictionary in the smart contract. 

🔹Steps 2 and 3: Once the NFT is minted, we need to transfer it to the owner’s address. In blockchains, the address acts as an account number in 
the bank. We control the permissions via the private key stored in wallets like Metamask.

🔹Step 4: We can now authorize the Reddit page to have read-only access to the wallet. The service first goes to the smart contract and then 
retrieves the metadata URI based on token ID. Then it can load up the picture file from IPFS using the image URI in the metadata. So finally 
we can see the cool avatar picture.

You might notice the NFT profile is more complex than the regular solution. But due to the usage of smart contracts, blockchains, and IPFS content 
addressing, we can guarantee the integrity of Intellectual Property. Also, the profile pictures become tradable assets now, or even your personal 
identity. 

Over to you: In content addressing, the generated CID (content identifier) is based on the file content
