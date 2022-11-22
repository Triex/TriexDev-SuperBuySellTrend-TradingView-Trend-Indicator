# TriexDev - SuperBuySellTrend (SBST) TradingView Trend Indicator

[Base Indicator - TradingView script link](https://www.tradingview.com/script/lz0rpQtQ-TriexDev-SuperBuySellTrend/)

[SBST Plus - TradingView script link](https://www.tradingview.com/script/HZFvahUz-TriexDev-SuperBuySellTrend-PLUS/)

---

Dig this indicator? Want to support me doing more free stuff? <a href="https://buymeacoffee.com/Triex">BuyMeACoffee</a>

I am creating a (likely) paid (automatic trading) `Strategy` using this while I optimise the free indicator. Early backtests give great results. 
Currently working on optimising the probability side - but this may take some time as I am mid other projects.

---

Minimal but powerful.

Have been using this for myself, so thought it would be nice to share publicly. Of course no script is correct 100% of the time, but this is one of if not the best in my basic tools.

---

# [Base Indicator](https://github.com/Triex/TriexDev-SuperBuySellTrend-TradingView-Trend-Indicator)

## What is ATR?
The average true range (ATR) is a technical analysis indicator, which measures market volatility by decomposing the entire range of an asset price for that period.

The true range indicator is taken as the greatest of the following:
- current high - the current low;
- the absolute value of the current high - the previous close; 
- and the absolute value of the current low - the previous close. 

The ATR is then a moving average, generally using 10/14 days, of the true ranges.

## What does this indicator do?
Uses the ATR and multipliers to help you predict price volatility, ranges and trend direction.

>The buy and sell signals are generated when the indicator starts 
plotting either on top of the closing price or below the closing price. A buy signal is generated when the ‘Supertrend’ closes above the price and a sell signal is generated when it closes below the closing price.

>It also suggests that the trend is shifting from descending mode to ascending mode. Contrary to this, when a ‘Supertrend’ closes above the price, it generates a sell signal as the colour of the indicator changes into red.

>A ‘Supertrend’ indicator can be used on equities, futures or forex, or even crypto markets and also on daily, weekly and hourly charts as well, but generally, it will be less effective in a sideways-moving market.

_[Thanks to KivancOzbilgic who made the original SuperTrend Indicator this was based off](https://www.tradingview.com/u/KivancOzbilgic/)_

---

## Usage Notes

Two indicators will appear, the default ATR multipliers are already set for what I believe to be perfect for this particular (double indicator) strategy.
If you want to break it yourself (I couldn't find anything that tested more accurately myself), you can do so in the settings once you have added the indicator.

Basic rundown:
- A single Buy/Sell indicator in the dim colour; may be setting a direction change, or just healthy movement.
- When the brighter Buy/Sell indicator appears; it often means that a change in direction (uptrend or downtrend) is confirmed.

---

[![Chart Snapshot](https://www.tradingview.com/x/z2B45Iaf)](https://www.tradingview.com/x/z2B45Iaf)
You can see here, there was a (brighter) green indicator which flipped down then up into a (brighter) red sell indicator which set the downtrend. At the end it looks like it may be starting to break the downtrend - as the price is hitting the trend line. (Would watch for whether it holds above or drops below at that point)

[![Chart Snapshot 2](https://www.tradingview.com/x/qj1xmOoj)](https://www.tradingview.com/x/qj1xmOoj)
Another example, showing how sometimes it can still be correct but take some time to play out - with some arrow indicators.

Typically I would also look at oscillators, RSI and other things to confirm - but here it held above the trend lines nicely, so it appeared to be rather obvious.

It's worth paying attention to the trend lines and where the candles are sitting.
Once you understand/get a feel for the basics of how it works - it can become a very useful tool in your trading arsenal.

[![Chart Snapshot 3](https://www.tradingview.com/x/7ftnNOuT)](https://www.tradingview.com/x/7ftnNOuT)
Also works for traditional markets & commodities etc in the same way / using the same ATR multipliers, however of course crypto generally has bigger moves.

---

_You can use this and other indicators to confirm likeliness of a direction change prior to the brighter/confirmation one appearing - but just going by the 2nd(brighter) indicators, I have found it to be surprisingly accurate._

Tends to work well on virtually all timeframes, but personally prefer to use it on 5min,15min,1hr, 4hr, daily, weekly. Will still work for shorter/other timeframes, but may be more accurate on mid ones.

--- 
---

# [SBST Plus](https://github.com/Triex/TriexDev-SuperBuySellTrend-TradingView-Trend-Indicator/tree/master/sbst-plus) 
_Using the "plus" version is optional, if you only want the buy/sell signals - use the "base" version._

[![Chart Snapshot](https://tradingview.com/x/4fzGlOqI)](https://tradingview.com/x/4fzGlOqI)
_With all the "+" indicators turned on, it may look a little confusing at first glance - but if you switch them on/off you should be able to quickly work out what each one is / means, as well as work out your preferences._

## What are vector candles?
Vector Candles (inspired to add from TradersReality/MT4) are candles that are color coded to indicate higher volumes, and likely flip points / direction changes, or confirmations.

These are based off of PVSRA (Price, Volume, Support, Resistance Analysis)

PVSRA - From MT4 source:

>- Situation "Climax"
>- Bars with volume >= 200% of the average volume of the 10 previous chart TFs, and bars
>- where the product of candle spread x candle volume is >= the highest for the 10 previous
>- chart time TFs.
>- Default Colors:  Bull bars are green and bear bars are red.  
&nbsp;
>- Situation "Volume Rising Above Average"
>- Bars with volume >= 150% of the average volume of the 10 previous chart TFs.
>- Default Colors:  Bull bars are blue and bear are blue-violet.

A blue or purple bar can mean the chart has reached a top or bottom. 
High volume bars during a movement can indicate a big movement is coming - or a top/bottom if bulls/bears are unable to break that point - or the volume direction has flipped.

This can also just be a healthy short term movement in the opposite direction - but at times sets obvious trend shifts.

## Volume Tracking
You can shift-click any candle to get the volume of that candle (in the pair token/stock), if you click and drag - you will see the volume for that range.

## Bollinger Bands
Bollinger Bands can be enabled in the settings via the toggle. 

Bollinger Bands are designed to discover opportunities that give investors a higher probability of properly identifying when an asset is oversold (bottom lines) or overbought (top lines).

>There are three lines that compose Bollinger Bands: A simple moving average (middle band) and an upper and lower band.

>The upper and lower bands are typically 2 standard deviations +/- from a 20-day simple moving average, but they can be modified.

## Up/Down Volume Analysis
Quickly lets you check whether the market is buying or selling. 

Volume Analysis can be enabled via a toggle in the settings, you can also change the colours & opacity of the bars.

Buy volume is above 0 (positive), sell volume is below 0 (-negative) on the chart. 

It will show the Buy + Sell volume for each candle on the timeframe you are viewing.

## MA 50, 200, 800
Moving Averages help to work out the current trend / direction. (eg, often; above 200 = bullish, below 200 = bearish). I tend to watch the 50+200 day MA locations and crossovers as primary trendlines for general use. 

## Psy Levels, Daily Hi/Lo & opens
Psychological & daily levels help to confirm, or find pivot points. 

I personally switch these off sometimes to reduce the amount of lines on the chart, but can be very useful.

---
---

## Dev Notes & Future Ideas
- [ ] Consider adding Bollinger Bands to base indicator
- [X] Set up of SBST Plus
  - [X] Toggle-able Bollinger Bands (default state is off)
  - [X] Added vector candles (using PVSRA) inspired from TradersReality/MT4 (Not simple to add an on/off toggle, so have created a "plus" indicator, that way people can choose whether or not they want the extra features)
  - [X] Added toggle/shift click volume functionality (click to see candle vol, drag to see range) 
  - [X] Toggle-able Buy/sell volume analysis (default state is off)
  - [X] Toggle-able MA 50, 200, 800
  - [X] Toggle-able Psychological Levels, Daily/Weekly Hi/Lo & opens
- [ ] Possible to add easy to read RSI, (or?) Stochastic RSI
- [ ] Buy/Sell triggers based on (user inputable) probability that either 1st or 2nd indicator is correct in its prediction
- [ ] Consider how to implement probability algorithm for when a candle crosses over a trend line in either direction

---

[This Repo is licensed under an MIT LICENSE](./LICENSE)
