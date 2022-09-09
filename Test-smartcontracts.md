A Short and Sweet Guide for Testing Your Smart Contracts Effectively:
 

Tools you should know/know where to find if you don't :)
(The link to each of these is in the comment)

- Surya by ConsenSys to make sense of the smart contracts you are writing your tests for, saves a lot of time if the SCs are complex and not 
written by you.
-All the chai matchers to test your cases.
-Additional chai matchers provided by Hardhat for more complex matching.
-Hardhat network helpers to manipulate time, blocks, accounts, balances, take snapshots, manipulate storage and much more on the local network right 
from your test code.
 

Unit Test Flow:
1. Test the cases when the smart contract's function is used as it is supposed to.
2. Trigger all the require/assert statements
3. Trigger all the modifiers
4. Target the edge cases
 

Never Forget To:
-Trigger every require/assert statement and modifier with all the possible paths.
-Test the 'internal' visibility quantifiers by:
-Removing 'internal'
-Writing a test for a passing function call
-Restoring 'internal'
-Updating the test to assert a failing function call

-Check for the boundary condition parameters and boundary condition +/- 1
For example, for uint, check with 0, 1, uint_max, uint_max-1
-Test all the possible ways the code can flow(full coverage)
-Cover all the conditional operators and their combinations, for ex. 'if (a && b)' will have 4 tests
