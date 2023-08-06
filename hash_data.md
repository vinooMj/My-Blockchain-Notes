Making a Hash of it!
We are used to thinking of audibility in terms of reams of files (stacked in physical form at worst and at big data centres at best). If someone submits a file or data used in some crucial calculations or assessments, we typically want to keep a copy of it - in a dedicated folder for “audit purposes”.

In a similar vein, our project champion at a new client asked me yesterday, “all these files we use in the process, for audibility and traceability do you put them on blockchain?”.
“No”, was my short reply.
“Why?”, he asked, in shock.
“Firstly, it is expensive and secondly it would publish private and confidential data of your firm to the whole world.”
He asked further, “then how do you know if someone has altered a file?”
“We make a hash of it!” I said.
Well, I didn’t, that would have been too cheeky! But I meant exactly that, technically speaking.

Hash is a cryptographic fingerprint of an object - a text, number, data object, file, collection of files and so on. It is of a fixed length of user’s choice.

For example, the hash of the text “Answer to life, the universe and everything” is 5fb93cacf0897ff1ed482a17aac3d5c547951c05ca1a305a68eaf96e3ef0b2fd
(If you tried to spot 42 or a pattern corresponding to it, congratulations, you passed the nerd test!)

What’s very important is that the hash of only a slightly modified text like “Answer to life, the universe, and everything” (there is comma after universe) is 259b05ddb6410ca76bcc2bac69305377d4e7ad7e4663b2f18dd4e49d700d9503

It’s not slightly different from the previous one, it is as far from the previous one as any randomly selected hash would be. Same goes for larger data like entire files.

For audibility, you just need to make a hash of the input data and post it on a public blockchain. The auditor can still take the original data from you as the source and quickly check if the hash of the data you gave matches the hash put up by you earlier on the blockchain. If it matches, there is no way you could have modified it since the time you posted it. Trust has been established!

We have clients using it already for the following purposes.
1. Creating carbon credits using given set of inputs about farm practices - the hashes of input data and supporting files are posted on chain.
2. Quality of agri commodities through their journey from farm to factory gate - hashes of quality data and images if any are posted on chain.
3. Emissions of a given ingredient in a food product - calculation models and their inputs are hashed and posted on chain.

Similar logic can be used for posting property deed documents and associated encumbrance certificate etc on chain. Something else we are working on.
