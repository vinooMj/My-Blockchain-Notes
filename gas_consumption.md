Top 4 Solidity Gas Optimization Techniques :-


1. Use Uint256 instead of Uint8 :-

A smart contract's gas consumption can be higher if developers use items that are less than 32 bytes in size because the Ethereum Virtual Machine can only handle 
32 bytes at a time. In order to increase the element's size to the necessary size, the EVM has to perform additional operations.

contract A { uint8 a = 0; }

The cost in the above example is 22,150 + 2,000 gas, compared with 7,050 gas when using a type higher than 32 bytes.

contract A { uint a = 0; // or uint256 }

Only when you’re working with storage values is it advantageous to utilize reduced-size parameters because the compiler will compress several elements into one
storage slot, combining numerous reads or writes into a single operation.

Smaller-size unsigned integers, such as uint8, are only more effective when multiple variables can be stored in the same storage space, like in structs. Uint256 uses 
less gas than uint8 in loops and other situations.


2. Use Mappings Instead of Arrays :-

There are two data types to describe lists of data in Solidity, arrays and maps, and their syntax and structure are quite different, allowing each to serve a 
distinct purpose. While arrays are packable and iterable, mappings are less expensive.

It is advised to use mappings to manage lists of data in order to conserve gas. This is beneficial for both memory and storage.

An integer index can be used as a key in a mapping to control an ordered list. Another advantage of mappings is that you can access any value without having to
iterate through an array as would otherwise be necessary.

3. Store Data in Calldata Instead of Memory :-


Instead of copying variables to memory, it is typically more cost-effective to load them immediately from calldata. If all you need to do is read data, you can
conserve gas by saving the data in calldata.

Because the values in calldata cannot be changed while the function is being executed, if the variable needs to be updated when calling a function, use memory
instead.

4.Use the External Visibility Modifier :-


Use the external function visibility for gas optimization because the public visibility modifier is equivalent to using the external and internal visibility 
modifier, meaning both public and external can be called from outside of your contract, which requires more gas.
