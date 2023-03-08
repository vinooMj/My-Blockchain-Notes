A Guide to Automated Market Makers (AMMs) 💱

🟢 Automated market maker (AMM) is a protocol used by decentralized exchanges (DEXs) like Uniswap, Sushiswap or Pancakeswap. 

Instead of relying on traditional financial intermediaries, AMMs use automated smart contracts to pair crypto buyers with sellers.

AMMs use a mathematical formula to determine the price of an asset based on its supply and demand.

Unlike traditional exchanges(Binance, KuCoin, CoinBase), which are based on the order-book model, AMM-based exchanges have liquidity pools of different pairs of assets. 

One of the most common types of AMMs is the constant product market maker model, which uses a simple mathematical formula (x * y = k) to determine the price of an 
asset based on the ratio of the two assets in a liquidity pool.

For example if a liquidity pool contains equal amounts of ETH and DAI, then the price of ETH in DAI will be determined by the formula ETH * DAI = k, where k is a 
constant.

These pools are created by Liquidity Providers (LPs), which get a certain percentage of the trading fee for providing liquidity to the pool. 

Upon providing Liquidity to the pool, they get LP tokens which represent their share in the pool, which can be given back to the pool to get their liquidity back.

In the example of ETH-DAI, to create a liquidity pool we need to add same worth of both of these tokens e.g 1 ETH = 1k DAI so we can create a pool of 2 ETH = 4k DAI


Now we have trading liquidity pool, for us to get eth we have to provide the pool with DAI, and to get DAI we need to provide the pool with USDC.

Here the Constant Product Market Maker Formula comes into place.

If we trade ETH for DAI, the amount DAI is now less than ETH in the Pool, the value of ETH increases.

Because x(ETH) * y(DAI) = K(Total Value of Both)

Any assets supply which will decrease in the pool, will increase it’s price to make sure the value of K remains the same.

This creates opportunity for arbitrage across different Decentralized Exchanges and Liquidity Pools, buying assets on a lower price from one DEX and selling to 
another DEX on a higher price.

Arbitrage results in an temporary loss for LPs which is called Impermanent Loss. for E.g

If the price of ETH increases to 1 ETH for 1,500 DAI, the LP's share of ETH in the pool will be worth more than their initial investment, but their share of DAI 
will be worth less. 

If the LP withdraws their liquidity at this point, they will receive fewer assets than they initially provided.

This temporary loss would become permanent if the LPs decide to withdraw their assets. 

All of this was explained if the swap variants is a constant product swap, there are more out there such as:

↪ Constant-sum swaps: Maintain a constant sum of the two assets in the liquidity pool.

↪ Hybrid swap: A combination of constant-product and constant-sum swaps.
