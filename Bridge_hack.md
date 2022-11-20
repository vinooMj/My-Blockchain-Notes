How Bridges are Hacked?

- Fake Events:
Often, a cross-chain bridge will monitor for deposit events on one blockchain to initiate a transfer to the other. If an attacker can generate a deposit event without
making a real deposit or by depositing with a valueless token, then they can withdraw value from the bridge at the other end.

- Message Verification Bug:
Cross-chain bridges perform validation of a deposit or withdrawal before actually performing any transfers. There have been many instances in the past where 
lack of proper validation of signature leads to millions of dollars hacks. Recently BSC chain was attacked because of a similar bug and a total of 576 Million was
withdrawn by hackers..

- Lack of cross-contract access control in blockchain bridges:
It is important to have access control validations on critical functions that execute actions like modifying the owner, transfer of funds and tokens, pausing and
unpausing the contracts, etc.

- Validator Takeover:
Some cross-chain bridges have a set of validators that vote whether or not to approve a particular transfer. If the attacker controls most of these validators, 
they can approve fake and malicious transfers. This is what happened to these validators in the Ronin Network hack, where the attacker took over 5 of the bridge’s 9 
validators.

- Admin Private Key Leak:
If the admin key of the smart contract is leaked, all the funds and operation of the smart contract will be at great risk. Recently, the Harmony bridge was exploited
via the theft of two private keys. The attack resulted in a theft of roughly $100 million in various cryptocurrencies.
