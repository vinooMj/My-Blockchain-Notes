Want to share a bingo of 10 how ERC20 tokens nearly broke my projects. The learning curve is steep but breaking the code is the only way
to confidence.

- Mixing tokens with different decimals

There are numerous ERC20 tokens with a variety of decimals. And such a zoo brings an annoying problem with their collective management. 
You have to either develop decimals-ignorant algorithms or make calculations in fixed decimals and convert the result back to the token 
decimals upon payments. Otherwise, there is a risk of confusing the amounts.

- Approval griefing

Never write functions like this: "deposit(address payer, address receiver, uint256 amount) external". If "from" give approval to a
contract with such a function, they will be instantly griefed.

- Deflationary tokens

Tokens that take fees on transfer are hard to correctly support. When you are developing a system, this is one of the concerns to keep 
in mind.

- Burnable tokens and Uniswap

There is a whole category of rebasing tokens (algorithmic stablecoins) that might not only suddenly change in supply but also modify the 
balances of individual users in order to maintain a peg. If such a user happens to be a Uniswap pair, the token
price might get out of control.

- LP tokens misuse

The concept of LP tokens is used to represent a user share in a big pool of assets. There is a limitation though. You won't be able to 
properly record the profit (or PnL) of an individual asset in this pool, only a collective one. This is something that clients tend to 
forget about.

- Forever locked tokens

Unfortunately, there is no token recovery function in the ERC20 standard, so whatever token is sent directly to the token contract gets 
lost forever. I know unfortunate folks who lost $50k this way.

- USDT

There are 2 caveats with USDT.

1. The token requires an allowance to be reset before setting a new one. So you can't just change it from 10 to 5. You have to
do 10 -> 0 -> 5 = 2 transactions. Literally a degraded UX and a possibility of DOS.

2. USDT doesn't return "bool" in functions approve(), transfer(), and transferFrom() which makes it incompatible with ERC20 interfaces.
Solidity reverts if the expected non-empty returndata happens to be empty. That is why you are forced to use low-level calls and
safeTransfer libraries that basically skip the check.

- WETH

2 caveats for WETH as well.

1. WETH withdraw() function that unwraps ether calls transfer() that forwards only 2300 gas to the receiver. The catch is the 2300 gas might not be enough for a proxy contract (especially Diamond) to process the withdrawal, which might result in DOS.
