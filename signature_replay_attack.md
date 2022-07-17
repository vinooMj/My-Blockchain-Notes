Signature Reply Attack in SmartContracts (Let's break it down):

It is the scenario in which the same signature is used to execute multiple functions or transactions within the Smart Contract. 

So what is the signature? What is the advantage of executing multiple functions with a single signature?

Consider the example of a multi-sig wallet which needs more than one private key, which is more than one person to authorize transactions. 

Let's you are trying to withdraw 10 ETH from the wallet and you need one more signature to authorize that transaction. Let's say I am the one doing that. 

The transaction goes through, you receive your 10 ETH and now all these signatures are publicly available. 

Now you can use these same signatures to execute another transaction of 10 ETH. And keep doing so until the funds in the Wallet are completely drained.

So how do you get around this? 

Making sure that signatures are unique for each transaction is a mitigation for this attack. 

That's about Signature Reply Attacks. I feel all the Web3 founders should be familiar with some of the common smart contract attack vectors.  
