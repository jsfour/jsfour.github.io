---
layout: post
title: Arbitraging Bitcoin with USDT
image: /assets/images/btc_usdt_poloniex_5-2.png
image_alt: USDT Arbitrage opportunity?
excerpt: On paper setting up an arbitrage using BTC and USDT seems like a good idea. But is it really?
permalink: arbitraging-bitcoin-with-usdt
tags:
  - usdt
  - tether
  - cryptocurrencies
  - arbitrage
  - trading
---

On paper setting up an arbitrage using BTC and USDT seems like a good idea. But is it really?

The other day I wrote about [why there was a price difference between USDT and USD]({% post_url 2017-04-22-untethered %}) and how you could take advantage of this market inefficiency to make a 7% profit.

Today we will explore this idea some more.

Since to take the trade you would need to go from a bank to an exchange to BTC to another exchange, to USDT and then to a bank (at some point) there are 2 risks:
1. The price of Bitcoin on the target exchange (Poloniex) will drop while the money is in transit and erode your profit
2. Tether will not get back their wire capabilities

Let's dissect each of these two risks separately.

![BTC/USDT daily returns on Poloniex]({{ "/assets/images/usdt_btc_daily_returns_1_1_16-4_15_17.png" | absolute_url }}){:.center}

Above is a distribution of the daily returns for on Poloniex BTC/USDT from January 2016 to mid-April 2017. Daily returns are the percentage difference in price between any given day and previous day.

One thing that you may notice is the distribution trails off at -10% but extends all of the way to 20%. This means that on most days of the days the price moves in a negative direction but occasionally there is a big spike.

As I mentioned above, most days are losers. Here are the exact figures:
- 58.5987% of the time the return of the day was less than 0
- 41.4013% of the time the return of the day was greater than or equal to 0

At this point, you may think "if most of the time BTC is losing money how come it's up overall". I thought the same thing at first but then realized that occasionally BTC had a very big ~18% day. In fact 0.4246% of the time the return for the day was above 15%. These "big day" gains offset all of the losses.

The price chart for the same period confirms this.

![BTC/USDT price 1/1/16-4/15/17]({{ "/assets/images/usdt_btc_daily_price_1_1_16-4_15_17.png" | absolute_url }}){:.center}

So let's quickly summarize:
1. 58.5987% of the days BTC has a lower price than the day before
2. 0.4246% of the time BTC has a significant gain

If our arbitrage requires that we hold Bitcoin for a day there is a 58.6% chance that the price will move in down while the money is in transit. The good news is that there is also a small chance that the price will jump considerably.

"But Jimi" you may say "who will be holding BTC for a day? It only takes an hour to transfer between wallets." That's a valid argument.

Let's adjust the analysis.

According to [blockchain.info](https://blockchain.info/charts/avg-confirmation-time?timespan=30days&daysAverageString=30) the average block confirmation time is around 100 minutes as of this writing.

Let's resample our daily returns down to 100-minute returns using the last closing price in each period as the price for the period. This resampling breaks last year into periods of 100-minutes and tells us for every period if BTC/USDT increased or decreased in price. From this we can understand the likelihood that the price will drop while we are transmitting the Bitcoin between exchanges.

Here is what that distribution looks like.

![BTC/USDT 100 minute returns 1/1/16-4/15/17]({{ "/assets/images/usdt_btc_100_min_returns_1_1_16-4_15_17.png" | absolute_url }}){:.center}

This looks promising. Here is what I noticed:
- 52.1008% of the 100 minute periods the return was negative
- 47.8992% of the 100 minute periods the return was positive
- The median negative return for the period is -0.347572545288%

So if you were doing this trade you would have a 52% chance that the price would adjust downward on you but typically you could reasonably expect that the price would slide only 0.35%.

Keeping in mind that "past performance does not guarantee future results" and also this analysis only takes into account Poloniex's historical data, this looks like it may work.

Bitcoin, however, is only one-half of the trade. Remember the sequence of the trade would be:
1. USD>BTC
2. BTC transfer to different exchange (in this case [Poloniex](https://www.poloniex.com))
3. BTC>USDT
4. USDT>USD

## How about USDT?
As I mentioned above, one of the risks here is that USDT won't be able to get their outbound wires going again.

I would love to pull some data to understand more about this risk, but I can't since we don't know much about what Tether is doing.

This blind spot is why the trade is too risky.

If Tether isn't able to get their wire capabilities back people would start selling off their Tethers which would force the price down relative to Bitcoin -that's assuming that people will even want unredeemable Tethers. Realistically there is a non-zero chance that, if Tethers are unredeemable nobody would be in the market for them. In this very unfortunate situation, the price would be $0.

*I hope this doesn't happen because I really like what Tether is doing and think the crypto world really needs it.*

The chances of knowing if a trade would be successful are unknowable unless you are sitting in Tether's office. Because of this opacity, if you took the trade you would be risking 100% of your money for a 7% return.

As a comparison, if you were to go to Vegas and put your money on black, you would be risking 100% of your money for a 47.4% effective return --plus Vegas gives comps if you bet a lot.

It's probably best to pass on this arb.

**Disclaimer: The above references an opinion and is for information purposes only. It is not intended to be investment advice. Seek a duly licensed professional for investment advice.**
