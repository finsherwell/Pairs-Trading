# Pairs-Trading

Pairs trading is a strategy that involves finding two historically correlated assets (usually stocks), identifying when their prices diverge, then placing opposite trades on then with the expectation that their price relationship will revert to the mean. Throughout this README file, I will include some examples which might not be accurate. These examples are purely for my own benefit - to help me remember concepts with ease, and make it easy to return to theory.

## Correlation
**Technical Definition:** Correlation is a statistical measure of how two assets move in relation to each other. A high correlation usually means that they move together.

**Example:** Coca-Cola (KO) and Pepsi (PEP) are two beverage giants. They operate in the same industry and are affected by similar market forces (e.g. soda consumption trends), their stock prices tend to move in a similar direction over time - they are positively correlated.

## Identifying a Pair
**Technical Concept:** Traders look for two assets with strong historical correlation - they move together over time.

**Example:** Imagine McDonald's (MCD) and Yum! Brands (YUM) - both operate fast-food chains around the globe. Over time, their performance often moves similarly due to consumer trends and factors affecting the macroeconomy.

## Mean Reversion
**Technical Concept:** Mean reversion is the theory that prices (or price relationships) tend to move back towards their historical average over time.

**Example:** Imagine there are two gas stations opposite each other on the same street. They usually have similar prices, but one day one of the gas stations raise its price by 50 pence. Over the next few days, they usually adjust to return to parity, because customers will move to the cheaper station.

## Strategy Setup
**Strategy Step:**
1. Identify a price divergence between the two correlated assets.
2. Short the asset that has outperformed (is overpriced relative to the other).
3. Go long on the underperforming asset (is underpriced).
4. When prices converge again, close both positions for a profit.

**Example:**
If KO and PEP normally trade at similar price ratios, and KO suddenly rises 10% while PEP only rises 2%, you might:
- Short KO (expect it to come down).
- Buy PEP (expect it to catch up).
- When they return to their normal relationship, you exit both trades.

## Market Neutrality
**Technical Concept:** Pairs trading is considered market-neutral because you're hedging - you both have a long and short position, so you are less exposed to the overall market direction.

**Example:** If the stock market crashes, both KO and PEP might go down - but if KO falls more, you still profit because your trade was based on their relative move, not the markets overall trend.

## Risks in Pair Trading
**Main Risks:**
- Breakdown in correlation: The two assets no longer move together (e.g. one changes its business model).
- Divergence doesn't revert: The price difference may increase instead of decreasing.
- Execution risk: You mistime the entry or exit.

**Example:** If KO introduces a revolutionary new product and PEP struggles with declining sales, their stocks may diverge permanently - and your trade will suffer.

## Tools Used
The following tools will be used throughout this project:
- Statistical Analysis: Correlation coefficients, z-scores, cointegration tests.
- Charting Tools: Price ratio charts, spread charts, correlation matrices.
- Algorithms: Machine learning and/or quantitative models will be used to find and manage pairs.

## Automated or Algorithmic Pairs Trading
**Quantitative Approach:** Institutional traders often run algorithms to scan thousands of pairs in real time, testing correlation, volatility and mean reversion strength.
I will only be scanning a few pairs, but using a wide range of quantitative techniques and machine learning models to help accurately detect pairs.

## Best Conditions for Relative Value Trading
**Technical Concept:** Pairs trading performs best in stable market conditions, where correlations are preserved and mean reversion is more likely. High-volatility or highly directional markets may distory relative pricing.
Ideal Conditions Include:
- Sideways or range-bound markets.
- Assets with clear, long-term business similarities.
- Periods with low systemic shocks (e.g. outside of major financial crises or unpredictable news events).

**Example:** In a calm economic period with no major interest rate changes or geopolitical shocks, the relationship between companies like American Airlines (AAL) and Delta (DAL) - which face similar costs and demand trends - may behave predictably, making them better suited for pairs trading.

## Other Concepts
### Z-Score:
Technical Definition: A z-score measures how many standard deviations an asset's current price (or price ratio) is from its mean. It helps determine how "extreme" the current divergence is.

*Use in Pairs Trading:*
- A high absolute z-score (e.g. above 2 or below -2) suggests a potential trading signal.
- When z-score reverts towards 0, the trade can be exited.

### Cointegration Tests:
Technical Definition: Cointegration is a statistical property where two non-stationary time series have a stable, long-term relationship. Unlike correlation, cointegration implies that the spread between the two series is mean-reverting.

*Example:*
Suppose McDonald's (MCD) and Wendy's (WEN) stock prices trend upwards over time. Even if their prices don't appear closely correlated day-to-day, a cointegration test might show that their price difference is stable and mean-reverting - making them a good candidate for pair trading.

### Price Ratio:
Technical Concept: The price ratio is the quotient of the prices of the two assets in a pair, typically calculated as:
```
Price Ratio = Price of Asset A / Price of Asset B
```

*Used in Pairs Trading:*
- Used to track the relative performance of the two assets.
- Mean and standard deviation of the ratio help define entry and exit thresholds.

*Example:*
If KO trades at £60 and PEP at £55, the price ratio is 1.09. If over the past year the ratio has averaged 1.05, this may suggest KO is temporarily overpriced and could be shorted while going long on PEP.
