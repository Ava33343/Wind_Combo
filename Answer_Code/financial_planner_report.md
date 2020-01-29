# Financial Planner Report

## A retirement portfolio for Harold
_**1. The stock market is in an upswing in the past year**_
_**2. Harold is inclined to more weight on stocks**_
_**3. S&P 500 index, SPY, that traces the market is used as the stock component**_
_**4. iShares Core US Aggregate Bond ETF, AGG, by BlackRock is used as the stock component**_
_**5. Data is fetched from IEX Finance over the last 365 days including 252 trading days**_

### A portfolio with stock-to-bond Ratio of 60/40 

In planning for retirement in 30 years, we carried out Monte_Carlo simulation for the next thirty years with 252 trading days in each. Daily returns of stocks and bonds are assumed for follow a normal distribution with means and standard deviatiosn calculated from the historical daily returns over the past year, based on daily closing prices. The initial values are based on the closing price of the previous day, in our case, January 28, 2020. Five hundred simulations are generated to project the returns until retirement.

The assumption here is that the stock and bond market returns over the next 30 years are approximately the same as those over the past year. However, since the market has been rallying over the past couple of years, the simulated portfolio return is likely to overestimate the value inside by the time of retirement. Thereafter, a lower percentile of a confidence interval for the returns are more appropriate in the analysis for a safer retirement. 

Over a thirty-year time frame, according to Figure 1, from the 500 simulations, the cumulative returns on $1 initial investment ranges from $30 to $290 at the time of retirement. Figure 2 shows the frequencies of simulated portfolio returns at the end of 30 years while the probabilty of returns on simulated portfolios are displayed in Figure 3. 

![Figure 1](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_1.png)

![Figure 2](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_2.png)

![Figure 3](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_3.png)

A 90% confidence interval, as suggested by the two vertical red lines, states that 90% of the portfolios would generate returns of between $49.2 and $190.8 on a dollar of initial investment. That is approximately 50 times and 191 times the initial investment, respectively. 

Comparing to cumulative returns by the end of year 20, as illustrated in Figure 4 and Figure 5, 90% of the simulated portfolios generate returns that are between 41.8 and 159.4 folds of the original investment. 

![Figure 4](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_4.png)

![Figure 5](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_5.png)

Differences in the 5th and 95th quantiles between 20 and 30-year simulated returns are 7 and 31, respectively. Differences in the ranges of the middle 90% of simulated returns are 142 and 118, respectively, at the end of 30 years and 20 years. See Table 1 below for details:

Table 1. 90% Confidence Intervals for Simulated Portfolio Returns at the end of 30 and 20 years

Simulated Returns | 30-year | 20-years 
----------------- | ------- | ---------
5th Quantile        |   49.2  |   41.8
95th Quantile         |   190.8 |   159.4

The difference in simulated returns widens with increase in years. The gap between higher percentiles grow. Those can be explained by compounding interests. 

### Retirement Analysis on the 60/40 Stock-to-Bond Portfolio

Based on result of the simulation and current projected annual income from Plaid analysis, we come to the following conclusions:

1. the expected cumulative returns for $1 investment at the end of 30 years at 10th, 50th and 90th percentiles are $58.27, $96.43 and $162.94, respectively.

2. According to results from the Monte Carlo simulation, an initial investment of $20,000 in the portfolio over the next 30 years, i.e. 7,560 trading days, will have a 10% chance that it ends up at or below $1,165,337.58, a 50% chance for valuing at or above $1,928,501.40, and a 90% of chance ending up over $3,258,783.77. In other words, the expected cumulative returns for $1 investment at the end of 30 years at 10th, 50th and 90th percentiles are $58.27, $96.43 and $162.94, respectively. Table 2 provides a comparison. 

Table 2. 10th, 50th and 90th Quantiles for $1 and $20,000 Initial Investment in the 60/40 Stock-to-Bond Portfolio

Initial Investment  | 10th Quantile  | 50th Quantile  | 90th Quantile
------------------- | -------------- | -------------- |  -----------
Investment $1           |   $58.27      |   $96.43      |   $162.94
Investment $20,000              | $1,165,337,58 | $1,928,501.40 | $3,258,783.77

3. At the end of 30 years, there is a 90% chance that the 4% withdrawal of $46,613.50 from the retirement portfolio is greater than the projected annual income of $6,054.80. The annual projected income was calculated from the first monthly income stream based on 2% annual inflation rate.


4. When initial investment is $30,000.00, 1.5 times the original $20,000 contribution:

* 50% more than the original, 90% of the expected returns will provide a 4% withdrawal from the retirement portfolio at or above $69,920.25; 50% of the expected portfolio returns will offer at least $115,710.08 at 4% withdrawal rate; 10% of the chance that the 4% withdrawal will secure over $195,527.03 in the amount.

* At the end of 30 years, there is a 90% chance that the 4% withdrawal of $69,920.25 from the retirement portfolio is greater than the projected annual income of $6,054.80.

* The difference in withdrawal amounts at 4% of the retirement portfolio is $23,306.75 at 10th percentile, $38,570.03 at 50th percentile, and $65,175.68 at 90th percentile. The gaps for differences in withdrawals widen as the percentile increases. Greater initial investment creates more chances for higher returns.

5. When initial contribution is $20,000, A 0.7% withdrawal of $4,531.59 from the retirement portfolio does not meet the projected annual income of $6,054.80 for 99.9% of the time. To the contrary, when initial contribution is $30,000, i.e. 1.5 times the original, at the end of 30 years, there is a 99.9% chance that the 0.7% withdrawal of $6,797.39 from the retirement portfolio is greater than the projected annual income of $6,054.80.

6. Figure 6 traces the median and 90% confidence intervals on cumulative daily returns for the 500 simulations on a daily basis for the next 30 years. Table 3 shows the median, upper and lower bounds of the 90% confidence interals on cumulative returns of the last 5 trading days:

Table 3. Daily Cumulative Returns - Median with Boundaries of 90% Confidence Interval on 60/40 Conservative Portfolio

Day       | CI_90_Lower |  Median    | CI_90_Upper
--------- |-------------|----------- | ------------
Day 7556     | 192.637704  | 96.021101 | 48.734163
Day 7557        | 193.685514  | 96.519774 | 48.708338
Day 7558           | 192.262019  | 96.769035 | 48.923027
Day 7559              | 191.639635  | 96.438293 | 49.166638
Day 7560                 | 190.803836  | 96.425070 | 49.185350

7. Goals for Retirement Budgeting with Inflation:

* At zero inflation, the value in the portfolio needs to be at least $151,370.00 by the end of the next thirty years.At 2% annual inflation rate, the projected annual income by the end of year 30 is expected to be $6,054.80.A cumulative return of 7.57 is required for retirement for a withdrawal rate of 4% from the portfolio.

* At 2% annual inflation rate, the value in the portfolio needs to be at least $274,185.80 by the end of the next thirty years.At 2% annual inflation rate, the projected annual income by the end of year 30 is expected to be $10,967.43.A cumulative return of 13.71 is required for retirement for a withdrawal rate of 4% from the portfolio.

* In Figure 6, Median and 90% Confidence Interval Trajectories on 500 Simulations of Cumulative Daily Portfolio Return Over the Next 30 Years, the horizontal red line represent required cumulative return at the end of year 30 with no inflation. The blue one, on the other hand, suggests the cumulative return necessary for retirement in thirty years at a targeted inflation rate of 2%. 

![Figure 6](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_6.png)

* According to Figure 6, the earliest day of retirement could take place around 2,700 trading days. In other words, after the 11th year, provided that the inflation rate is 0. By that day, only 5% of the portfolio returns accumulates just enough to retire and provide withdrawal of 4% in the amount comparable to current annual income. It is shown as the point where the horizontal red line crosses the light blue curve representing 95th percentile of simulated portfolio returns.

* Based on 2% inflation and similar rationale, a reasonable year of retirement is 17th year for over 50% of the simulated portfolio returns over the required amount for the 4% withdrawal to match projected annual income. Retiring after the 21st year would be ideal because by then there is 95% chance that the portfolio accumulates enough value for retirement.
    
### Early Retirement Challenge 
#### Goal: Retire in the next five years

_**More specifically: The value in the portfolio needs to be at least $167,124.71 by the end of the next five years.At 2% annual inflation rate, the projected annual income by the end of year 5 is expected to be $6,684.99.A cumulative return of 8.36 is required for retirement for a withdrawal rate of 4% from the portfolio**_

Based Figure 7, Median and 90% Confidence Interval Trajectories on 500 Simulations of Cumulative Daily Portfolio Return Over the Next 30 Years, we see that a 60/40 stock/bond portfolio does not return enough for retirement in five years. The required returns based on 2% inflation, as shown by the red horizontal lines, does not cross any of the portfolio returns curve prior to 2900 trading days, which is the 11th year following the initial deposit of $20,000.

![Figure 7](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_7.png)

Therefore, in order to retire early, we need a higher ratio of stocks to bonds and/or a greater amount of initial investment.

#### Strategy 1: A portfolio with more risk - 90% stocks (SPY) and 10% bonds (AGG)

After rerunning 500 monte-carlo simulations for cumulative daily returns on the more aggressive portfolio composed of 90% SPY and 10% AGG over the next five years, we see in Figure 8 that the trajectories are more spread out compared to the original, more conservative 60/40 retirement portfolio. Figure 9 traces the medians and two boundaries for 90% confidence intervals on cumulative daily returns in the five-year window. For the last five trading days, data are displayed in Table 4 below:

![Figure 8](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_8.png)

![Figure 9](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_9.png)

Table 4. Daily Cumulative Returns - Median with Boundaries of 90% Confidence Interval on 90/10 Aggressive Portfolio

Day      |    CI_90_Lower  |       Median     |   CI_90_Upper
---------| --------------- | ---------------- | -------------
Day 1256     | 1.698543          |  2.527966      | 3.923702
Day 1257          | 1.700851           |  2.531704    |  3.934448
Day 1258              | 1.704032           |  2.531314     | 3.933907
Day 1259                  |1.702606            |  2.545247     | 3.909562
Day 1260                        |1.708613           |  2.559520     | 3.920164

The horizontal red and blue lines in Figure 10 describes how long it takes for the portfolio to double and triple the initial investment. Those happen when the horizontal lines cross the curved trajectories that trace the median, 5th quantile and 95th quantile of simulated daily cumulative returns over the next five years. 

![Figure 10](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_10.png)

Since the required cumulative rate of return is 8.36 for retirement in the next five years, for an initial contribution of $20,000, and 13.71 for retirement in 30 years as previously specified, under 2% rate of inflation. According to Figure 8, we need to go more aggressive by doubling the initial investment. Figure 9 tells us that the portfolio returns double by 570 trading days with 5% probability, and a 50% chance of doubling by the 950th trading day. There is a 5% chance that the portfolio triples its value by 1000th trading days from the date of initial investment. As a result, the initial investment needs to be doubled to tripled for an adequate return to retire in five years.

Earliest year of doubling value in the 90/10 stock-to-bond retirement portfolio is year 2. 50% chance for doubling value in the 90/10 stock-to-bond retirement portfolio occurs in year 4. Chance of tripling value in the 90/10 stock-to-bond retirement portfolio is year 4, with a 5% probability.

_**For retirement by the end of the fifth year, we need $40,000 to grow up to $167,124.71 by the end of the 5th year, i.e. in 1,260 trading days.**_

In Figure 11, we see that our target return of $167,121,71 will not be met even by the top 5% of portfolio returns, indicated . by the 95th-quantile trajectory. Therefore, we need to increase initial contribution to reach our five-year retirement goal. 

![Figure 11](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_11.png)

#### Strategy 2: Increase Initial Investment

After raising the initial investment to $60,000, one and a half times the original deposit of $20,000, the dream of retiring in the next five years comes true, as described in Figure 12. With 2% inflation, we need portfolio returns to grow up to $167,124.71 in 1,260 trading days. There is a 5% chance to be able to retire at the end of 4th year, following the 900th trading day. Approximately 40% of the simulated returns suggest that it is possible for retirement at the end of five years.

![Figure 12](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_12.png)

In order to retire at the end of the fifth year, with 2% inflation, we need $70,000 to grow up to $167,124.71 by the end of the 5th year, i.e. in 1,260 trading days. It is a more reasonable investment strategy as there is 60% chance that the portfolio return grows up to the sufficient amount. Moreover, retirement is possible following the 750th trading day at a possibility of 5%, In other words, 5% of the simulated portfolios generate enough returns for retirement by the end of the 3rd year.

![Figure 13](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_13.png)

More specifically, with $70,000 initial investment, based on monte-carlo simulation, there is a 5% chance thatthe portfolio return allows retirement at the end of year 3, and 50% of the chance that the portfolio will return enough for retirement by year 5, given 2% inflation, a 90/10 stock-to-bond ratio and withdrawal rate at 4% by the end of the fifth year. In general, an initial investment of over $70,000 would have a greater chance to generate sufficient portfolio value for retirement.

An initial contribution of over $98,000, 4.9 times the original initial investmnet of $20,000, provides a safer retirement within the next five years for the more agressive, 90/10 stock-to-bond portfolio. The retirement portfolio has a greater chance of generating sufficient returns for 4% withdrawal to match projected annual income. Figure 14 suggests that 95% of the simulated portfolios return more than the required amount at the end of the three-year window. The horizontal red line representing required returns meets the lower bound of the 90% confidence interval, exactly at the end of Year 3. 

![Figure 14](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_14.png)

At last but not at least, according to Plaid account analysis, extra savings can come from spending on Transfer category that sumed up to $20,537.34, more than 60% of total spending in the past 90 days. 

![Figure i](https://github.com/Ava33343/API-homework/blob/master/Answer_Code/Images/Fig_i.png)

### References:

#### Portfolio Planner:
> UC Bootcamp Gitlab Repository
> https://guides.github.com/features/mastering-markdown/
> https://plot.ly/python/pie-charts/
> https://github.com/willwillis/python-api-homework/blob/master/portfolio_planner.ipynb
> https://matplotlib.org/gallery/lines_bars_and_markers/vline_hline_demo.html
> https://matplotlib.org/gallery/text_labels_and_annotations/usetex_baseline_test.html#sphx-glr-gallery-text-labels-and-annotations-usetex-* baseline-test-py
> https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.quantile.html
> https://matplotlib.org/api/_as_gen/matplotlib.axes.Axes.axhline.html