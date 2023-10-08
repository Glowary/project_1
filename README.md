# First Project - Stock Sector Analysis

## Summary

Using Python and libraries (yfinance, pandas, matplotlib, csv, and os), we performed a stock analysis on the iShares Global Infrastructure ETF (Ticker: IGF).

1.	What country has the largest weight in the index? How are the stocks labeled under that country’s trending?
    -	Created a bar chart to compare the over market capitalizations by country. 
    -	Plotted the closing prices of the largest country’s stocks on a line chart. 
2.	What sectors make up the infrastructure? And how do their performances compare to each other? 
    -	Created a pie chart to show the percentage make-up of the index by sector.
    -	Plotted the closing prices of the largest stock (by market capitalization) in each sector to represent the entire sector within the index.
3.	After visualizing the performance of each sector, do any of them appear to be correlated? If so, is the correlation significant?
    -	The utilities sector and the energy sector appear to be trending in the same direction.
        -	Null Hypothesis: There is no significant correlation between the utilities sector and the energy sector. 
    -	Plotted the daily percentage difference in closing prices on a histogram to see if the distributions are “Normal”. 
    -	Once determined to be “Normal”, we used the t-test to determine the p-value of the data. 
    -	If the data is > 0.05 then the correlation between the two sectors is insignificant, and the Null Hypothesis remains True. If < 0.05 then reject the Null Hypothesis.


## Statistical Analysis

1.	What country has the largest weight in the index? What is the trend of the stocks labeled under that country?
    -	The bar chart that shows the comparison of the market capitalizations by country shows that the United States far exceeds the weight of all the other countries represented within the index. This is most likely because the USA has the largest GDP in the world, which is a lagging economic indicator that is commonly influenced by a country’s infrastructure spending. In addition, the USA’s large GDP and overall economic environment creates lower probabilities of systematic risks which is attractive for companies and investors alike. Therefore, the index is going to include more USA based companies because they appear “safer” to investors. 
    -	The factors estimated to make the index more weighted in USA stocks, don’t guarantee the performance of the stocks. And because the index weight is large, their performance heavily influences to overall share price of the index. That is why we plotted the closing prices of each USA stock on a line chart to visualize the technical trends that could potentially aid in predicting the price trend of the index. Based on the chart, it appears that most USA stocks are in a down-trend which could justify a negative outlook on the performance of the index. 
2.	What sectors make up the infrastructure index? And how do their performances compare to each other? 
    -	Breaking the index down by sector weight allows us to predict the effect that certain market events have on the index’s performance. If the index was heavily weighted in any one sector, then it would also be heavily exposed to the risks associated with said sector. The pie chart we created shows the index’s percentage made-up by sector. The industrial & utilities sectors are similar in weight and make up the majority percentage of the index (77.7% combined). The remaining smaller percentage is made up by the energy sector. The reason for how the index is weighted is most likely to do with risk exposure. Companies within the energy sector tend to involve the production of energy sources, such as oil, gas, and electricity. The prices of these raw materials are heavily influenced by global macro-economic factors, which can cause uncertainty in their prices. Therefore, investors can see energy companies as “riskier” than utilities/industrial companies that are more influenced by national micro-economic factors. 
    -	After determining the sector weights, the next step in the analysis would be to compare the overall performance of each sector. Due to time constraints, we chose the largest company by market capitalization within each sector to represent its sector’s performance. We compared the closing prices of each company for the last 12-months on a line chart so that technical trends were easily identifiable. Based off the chart, the utilities sector (Ticker: AENA.MC) is in an uptrend whereas the energy sector (Ticker: ENB) and the utility sector (Ticker: NEE) are both in down-trends. The performance of each sector could be a result of a variety of different factors that would require further analysis to determine. 
3.	After visualizing the performance of each sector, do any of them appear to be correlated? If so, is the correlation significant? 
    - Based on the previous line chart that compares the performance of the sectors within the index, the energy sector and the utilities sector are similar in the fact that they are both down-trending. Because of this, there is a probability that the two sectors could be influenced by the same factors, therefore correlated. To test for statistical correlation, we will be using the daily percentage change of the closing prices of the two sectors (represented by tickers: ENB & NEE). By plotting the data on a histogram first, we were able to determine that both data sets were normally distributed which will help determine how we should test for correlation.
        -	Null Hypothesis: There is no significant correlation between the utilities sector and the energy sector. 
    -	We used the t-test to determine whether the null hypothesis should be rejected. If the p-value > 0.05 then the correlation between the two sectors is insignificant, and the Null Hypothesis remains True. If p-value < 0.05 then reject the Null Hypothesis. The results from the test: 
        -	The p-value = 0.3299. Which means the null hypothesis remains true and there is no significant correlation between the two sectors.
        