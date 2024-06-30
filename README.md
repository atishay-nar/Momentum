# Momentum Signals

The Efficient Market Hypothesis states that share prices reflect all information available and that consistent alpha generation in impossible. To some extent, this explains why signals become less profitable as they become more widely known. When the information on signals becomes more widespread, assets are then priced more accurately to accommodate for this new information. This is the cause of alpha decay for signals. As information spread and more people begin to search for signals, assets become more accurately priced, especially at the speed at which information travels in the digital age. Thus it becomes increasingly difficult to find new signals. While my results did not show any alpha decay, this is due to the survivorship bias of selecting stocks that are currently in the Dow Jones. The Dow selects high-performing, high-market caps stocks, and every few years they change the stocks in the portfolio. The reason that the returns I experienced were so great is that I was investing with the current DJIA 30 tickers at a time when many of those stocks may not have been in the portfolio as they hadn’t been deemed blue-chip stocks yet. Additionally, my high returns can also be attributed to the lack of transaction factored into my monthly return. With a monthly turnover of over 70% in the best performing portfolio, any fees charged would add up over time and decrease the returns. For future projects, one should consider the current DJIA 30 and how it changes in the model and consider how transaction fees would decrease the monthly returns. I am also aware that when this same model is run with a larger selection of stocks, such as the S&P 500, the profitability of the signals decays roughly around 2015, when the signal became widely known as thus ineffective.

When choosing which tickers to include in my model, I excluded Visa and Dow. This is because they both had their initial public offering within 20 years of today, thus limiting the scope of my project. I chose to get data all the way back until new years day of 2000, as a little of 24 years seemed like an adequate amount of data with plenty of time to observe patterns and changes. I made quite a few major assumptions, especially with my choice of stocks. As I have mentioned earlier, the DJIA today looks different than the DJIA in the year 2000. In doing this, I have the bias of choosing stocks that historically high performing in the lookback period that, had I been an investor in the year 2000, I would not have considered as they weren’t in the DJIA at the time.

I have created 7 different portfolios, which operate as follows:
-	DOW: invests in all stocks in the portfolio, weighted by value. This is the control portfolio that tracks if you were to invest in 		underlying securities on their own.
-	OG: invests evenly in the top m stocks based on the chosen momentum signal
-	POS: invests evenly in the top m stocks given that the signal is positive
-	RANK: invests in the top m stocks, weighted by signal strength
-	VALUE: invests in the top m stocks, weighted by market cap
-	POSRANK: invests in the top m stocks given that the signal is positive, weighted by signal strength
-	LS: takes a long position in the top m stocks and takes a short position in the bottom m stocks, evenly
-	COMBO: takes a long position in the top m stocks given that the signal is positive and takes a short position in the bottom m stocks given 	that the signal is negative, weighted by signal strength and with the option to weigh more heavily on either long or short positions

To measure the success of these portfolios, I looked at various factors from my performance analytics class. In my opinion, the most important factors are the mean return and the volatility, which are summed up by the Sharpe ratio. It is important to note that the Sharpe ratio that I calculated for the purposes of this project does not factor in the risk free rate, and therefore may not be comparable to Sharpe ratios calculated in other projects. Investing evenly in the DJIA can be considered the control for these tests, which returned the following performance stats:

Mean Return (Annualized)	0.1041901478
Volatility (Annualized)	0.1578841442
Sharpe Ratio	0.6599152079
Hit Rate	0.6224489796
Maximum Drawdown	0.5940771969
Highest Monthly Gain (Annualized)	4.118655225
Worst Monthly Loss (Annualized)	-0.893460785
Monthly Turnover (Average)	0.04368108545

 
This can then be compared to the OG portfolio:

Mean Return (Annualized)	0.37067066
Volatility (Annualized)	0.1494552813
Sharpe Ratio	2.480144274
Hit Rate	0.735915493
Maximum Drawdown	0.8075832275
Highest Monthly Gain (Annualized)	4.974415482
Worst Monthly Loss (Annualized)	-0.7231664575
Monthly Turnover (Average)	0.4164179104

And what is the best portfolio by these standards, the COMBO portfolio:

Mean Return (Annualized)	0.6201215937
Volatility (Annualized)	0.1910982496
Sharpe Ratio	3.245040679
Hit Rate	0.7816901408
Maximum Drawdown	0.5954549375
Highest Monthly Gain (Annualized)	10.12736201
Worst Monthly Loss (Annualized)	-0.9452064084
Monthly Turnover (Average)	0.7143933586

The specific factors that achieved these statistics for the COMBO portfolio were a maximum of 4 long positions and 4 short positions per month, and these positions had a 4:1 bias towards long positions. I included the ability to bias the positions as markets tend to go up in the long run, so long positions are generally more favorable than short ones. When there aren’t any positive signals (or negative signals) the weighting doesn’t have an effect. Thus the short positions primarily exist to hedge against market downturns but can make large returns during a recession. As can be seen in the final chart, this occurred around 2008 when there was a major spike in performance of the COMBO portfolio when compared against the DOW portfolio. While this was corrected for shortly after, had a trader been experiencing the event live, they could have made the necessary changes to adequately capitalize on this situation.

It is difficult to determine short term inadequacies of these portfolios due their large returns, which make it difficult to determine movements early on due to the scale. However, the picture becomes more clear when you plot the difference in the returns streams of the portfolios, especially when compared to the DOW portfolio as seen in the final chart.
In conclusion, I was able to generate significant returns in the 24-year lookback period. Although there are many factors that I have not considered that may influence these returns, from the information I have gathered and processed, momentum trading appears to be a viable strategy to create large returns. I would be happy to receive any and all feedback on this project; please do not hesitate to reach out to me.

