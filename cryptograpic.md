Cryptography is the practice of securing communication in an adversarial environment.

Stated differently, cryptographic techniques are used to ensure that your information remains verifiable and private from snoops.

2The foundation of just about everything in blockchain is "Asymmetric Cryptography" (which, as you can imagine, is different from "Symmetric Cryptography")

Symmetric: Hide *and* reveal info using the same tool.

Asymmetric: Hide with one tool, reveal with another tool

3The "tool" to hide/reveal info is actually just data and it is called a "key." In Asymmetric Cryptography there are two keys:

Earth globe asia-australiaKey Public Key: Share with everyone

See-no-evil monkeyKey Private Key: Do NOT share with anyone (don't save in a desktop file named "Secret Private Key.txt")

4What do keys look like? Lots of letters and numbers like this: M3owIBv84KW68lzpGaRR...

There's a lot of math behind keys usually involving Fancy Prime numbers. It's not important to understand this math (whew!) so we'll just call it "Fancy Pants Math" Smiling face with sunglassesJeansAbacus from here on.

5Asymmetric Cryptography is also called "Public Key Cryptography."

An important concept here is that the Public Key is derived mathematically from the Private Key. 

The Private Key is generated using a large random number (important so that your Private Key is unique).

6, Let's talk Keycap digit one Encryption with Alice and Bob

Since Bob shares his Earth globe asia-australiaKey Public Key with everyone, Alice can use it to hide ("Encrypt") the info she wants only him to see.

And since Bob hides his See-no-evil monkeyKey Private Key, only he can see ("Decrypt") the encrypted info from Alice.

7 aybe you have questions:

White heavy check mark YES, you can post your Earth globe asia-australiaKey Public Key on a billboard outside your home

No entry sign NO, you cannot use a Earth globe asia-australiaKey Public Key to Decrypt info

White heavy check mark YES, if your See-no-evil monkeyKey Private Key is lost it is impossible to Decrypt info Encrypted with your Earth globe asia-australiaKey Public Key 

8Now, let's discuss Keycap digit two Hashing.

It is a common requirement in software to know if some piece of information (file, photo, message etc.) has been modified. You could check every byte and compare with the original, but this is slow and inefficient.

There's a better way...

9,Using Hashing, we can instantly tell if some info has changed (even a single byte).

Hashing uses Fancy Pants Math Smiling face with sunglassesJeansAbacus to take info of any size and make it a small, fixed size called a "hash."

Keycap number sign 1 = Before
Keycap number sign 2 = After

If #1 and #2 don't match, the info has changed!

10, Moving along to Keycap digit three Signing

While Encryption is about hiding information, Signing is about ensuring that a visible message is:

Blue circle Authentic, and
Blue circle Unmodified

The use of keys for Signing is the reverse order of Encryption.

11ere's how Signing works:

Step 1: Bob Signs his message for Alice with his See-no-evil monkeyKey Private Key

Step 2: Alice receives the message and uses Bob's Earth globe asia-australiaKey Public Key to verify the message signature

If the message was fake or modified, Step 2 would fail.

12, SHA-256 is a hash algorithm. For trust, it must fulfill two conditions:

1) No way to use the hash to get back the original data (i.e. hashing is one-way). White heavy check mark

2) Collision resistant — different input data should not result in the same hash. White heavy check mark

Both conditions met = Trust
