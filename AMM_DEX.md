AUTOMATED MARKET MAKER

Traditional exchanges work on order-book model. Buyers and sellers place their orders.

If you need to buy something at a certain price, there should be a seller willing to sell at that price, and vice versa.

eg: Robinhood, Nasdaq, Bombay Stock Exchange are based on order-book model.

Crypto decentralised exchanges (DEXes) like Uniswap, Sushiswap or Pancakeswap are based on Automated Market Maker or AMM model.

An AMM model has 'Liquidity Pools' of different pairs of assets. eg: ETH-USDC pool. People can buy and sell assets from/to this pool.

Who creates these pools? Liquidity Providers. They get certain percentage of trading fee for doing so. Anyone can contribute to a pool and become a 
liquidity provider.

To create an ETH-USDC liquidity pool, we need to add the same value of both assets. eg: If 1 ETH = 1k USDC, then we can create create a pool of 
10 ETH + 10k USDC.

In reality, this pool is much larger having much higher amount of each asset, but let's take 10 ETH + 10k USDC to understand.

Thus, we see that the value of each asset is same in the pool i.e. 10,000.

To buy ETH with USDC, you can add USDC to the pool, and in return, you'll get some ETH.

But now, since the amount of ETH gets lesser as compared to USDC, its value increases in the pool (>1k). This is because of something called 'Constant 
Product Formula'.

The increased ETH price creates 'arbitrage' opportunity for traders to buy ETH for cheap from somewhere else and sell it at a higher price in the pool. 
Thus, when they sell ETH to the pool, they add ETH and withdraw USDC, hence restoring the balance.

But what is constant product formula?

It says that the product of amount of both assets in the pool should always remain same.

i.e. 10 ETH * 10,000 USDC = 100,000

Hence, the product of ETH and USDC amount should always be 100,000

So initially, if you want to buy 1 ETH, you will reduce it from 10 to 9. Hence, the new USDC amount in pool should be 100,000/9 = 11,111.

i.e. you'll need to pay 11,111 - 10,000 = 1,111 USDC for 1 ETH.

If you want to buy an ETH again, ETH amount becomes 8. Hence, USDC amount in pool should be 100,000/8 = 12,500.

i.e. you'll pay 12,500 - 11,111 = 1,389 USDC for 1 ETH.

Thus, we see that more the supply of an asset decreases in the pool, more its price increases due to the constant product formula.

In reality, the pools are much larger, hence the price impact of buying and selling 1 ETH would be much lesser on the pool.

Also, arbitrage opportunities make sure that the prices are corrected to its fair value.
