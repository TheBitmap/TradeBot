# TradeBot
Automated LTC trading bot for crypto currency (Bitfinex)

I am NOT a programmer by any means.  I wanted to develop an automated trading bot to make money based on volatility, not long term trading.
None of my programmer friends would help me, so this is the result of a month of coding on PHP.  

I ran this bot via a console php (on windows with PHP installed, run cmd.exe, then type "php tradebot.php").  Or, you can make a batch
file like I did, to re-run this every so many seconds.  

I will say flat out -- the error checking I developed is complete garbage... it just checks to see if anything was returned... if no data
was returned, it's considered an error.  In a couple checks, if the wrong header was returned, it's considered an error.  

Anyways, I ran this bot, making profitable trades, then BitFinex decided to cease trading operations for any traders in the U.S.A...
so, my bot is now useless.  I may or may not port it to another exchange, however, I've decided to give it away for anyone interested.

I am NOT AT ALL liable if you lose money using this bot.  I've clearly stated that I am NOT a programmer... and you're deciding to use my
bot, so good luck.  I'll update this readme soon enough.... maybe?
-----------------------------------------------------------

This bot was designed to make many small profits as the prices rises and falls.  Some people call this a ping-pong strategy.  The bot will purchase LTC as every level.  By default, it will use .005% of your assets for each trade, and will place trades according to the spread you want to cover... all configurable in the bot.

This bot is currently only set to trade USD to LTC, and to make a few cents each trade.  Before I stopped running the bot, I was making as little as 0.2% profit a day, and as much as 1.5% a day.  The more volatility, the better. You can increase the risk, and likewise the reward in the variable configuration section in tradebot.php

THere are other files I used as "tools", like the read, read2, and show-logs.

In the data folder, it will save logs of the daily total profit, orders that successfully executed, and profit per order.  At the end of each day, it will move the logs into a different folder, then create a new file for the new day.

The risks/downsides are:

1. If the price drops, you will own coins bought at a higher level.  THe bot will hold onto them until it can sell them at a profit
2. If the price sky-rockets, it will not take advantage of a long ride up... it will keep making many small trades, and many small profits.
3. Sometimes, the bot would just kind of hang up.  If this happens, you may miss out on trades.

Bitfinex doesn't allow more than 100 trades per pair... TradeBot will cancell trades that are too low below the current price point.  If the price drops, it will save the trade in a log, then re-institute it when the price rises again.

Good Luck, and fuck you BitFinex, for stopping service to U.S. customers.  Fuck you so hard.

If there is any interest in this at all, I'll add more.  

Lastly, this bot would not have been possible without the API developed by Coinables.  Thank you sir.  You can find the original API project here: https://github.com/coinables/Bitfinex-API-PHP

If you make a bazillion dollars with my bot, maybe a kickback?

BTC: 3FmfWJUef49frwCbGQagKn1aQxNuadpYLJ
LTC: LNYtFZEJJXQMviTYN4ECB4L3WaqTxNsdfK

-TheBitmap
