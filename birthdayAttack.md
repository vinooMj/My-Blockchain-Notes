BIRTHDAY ATTACK 

* Cryptographic hash functions transform input data into fixed-size outputs, creating a unique hash value for each input. However, due to
the pigeonhole principle, where there are more pigeons than pigeonholes, collisions can occur.

* The Birthday attack leverages the "birthday paradox" to exploit collisions. This paradox states that in a group of just 23 people, the 
probability of two people sharing the same birthday is 50%. 

* In the context of hash functions, the birthday paradox suggests that with a fixed hash size of, let's say, 128 bits, the number of 
possible hash outputs is 2^128. However, as we generate more and more random inputs, the probability of a collision increases.

* With only √(2^128) ≈ 2^64 randomly generated inputs, there's a 50% chance of a collision occurring. This astonishing result is due to the
square root relationship in the birthday paradox. It means that the number of inputs needed to find a collision is surprisingly low.

* Attackers exploit this statistical probability by generating a large number of random inputs and comparing their hash values. With enough 
inputs, the chances of finding a collision become significant, potentially undermining the integrity of hash functions.

* Is the Birthday attack still dangerous today? 
While the Birthday attack remains a theoretical vulnerability, modern cryptographic hash functions are designed to withstand such attacks.
Algorithms like SHA-256 and AES use larger hash sizes and complex structures, making collisions extremely unlikely.

* Overall, the current state-of-the-art hash functions are considered secure against the Birthday attack. But as technology advances, 
it's crucial to stay updated on the latest research and recommended practices to ensure the continued protection of sensitive data.
