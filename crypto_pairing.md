What the **** is a Pairing?

To understand what an elliptic curve pairing is, one must see it being calculated in action. The math involved is complex and requires knowledge of multiple concepts in Abstract Algebra. Instead of directly jumping into the calculation, let's use sagemath to work out an end-to-end pairing example. I would urge anyone highly interested in this topic, to try to work out the example in this post with pencil & paper (🚫 warning: you need a zen monk's patience).

Step ➊
Create a finite field Fp and extend it to Fp2 where 2 is the embedding degree of the curve being used.
Step ➋ 
Define an elliptic curve on both Fp extend it to Fp2.
Step ➌
A pairing function takes two points in the curve one from base field and one from extension field and outputs a field element on the extended field.
Step ➍
A pairing function preserves the scalar multiplication and can transfer scalar multiplication to field exponentiation. That is: pairing(a*g1,b*g2) = pairing(b*g1,a*g2) = pairing(g1,g2)^(a*b)
