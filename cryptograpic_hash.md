Essential Properties of Cryptographic Hash Functions :

👉🏻 Preimage Resistance: Retrieving the original input value given a hash output should be computationally infeasible. This property is 
crucial for
ensuring the security of passwords and other sensitive data.

👉🏻 Second Preimage Resistance: It should be computationally infeasible to find any second input with the same hash output as 
any specified input, i.e., given x and h, it should be difficult to find y ≠ x such that h(x) = h(y).

👉🏻 Collision Resistance: It should be computationally difficult to find two distinct inputs that hash to the same output. 
This means it should be hard to find any two different inputs, a and b, such that H(a) = H(b).

👉🏻 Avalanche Effect: A slight change in the input should produce such a drastic change in the output that the new hash value 
appears uncorrelated with the old hash value.

👉🏻 Fixed Output Length: No matter how large or small the input is, the output length of the hash function remains the same.

👉🏻 Deterministic: The output (hash value) is always the same for a given input. This means that any changes to the input 
would produce a different output.
