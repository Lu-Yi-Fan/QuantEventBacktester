Systematic Trading Strategies and Systems


# **1) Portfolio Tailoring**

Our portfolio strategy stands at the forefront, harnessing the proven efficacy of systematic trading strategies to navigate the complexities of the markets. Our meticulously crafted investment portfolio is engineered to thrive in the fluctuating economic tides, offering our investors a beacon of stability and growth potential. Our risk appetite is well-balanced, incorporating elements of both aggressive growth and conservative stability, with a keen awareness of the importance of risk management and performance evaluation.

At the heart of our investment ethos lies a momentum-based strategy, underpinned by the dual forces of the Coppock Curve and the Relative Strength Index (RSI) indicators. These formidable tools are our compass, guiding us through the markets with precision and insight. The Coppock Curve, with its prowess in identifying long-term trend reversals, combined with the RSI’s acute sensitivity to short-term price movements, forms a symbiotic alliance that commands the ebb and flow of market momentum.

Our core philosophy revolves around a dual-indicator approach, leveraging both indicators to distill and amplify trading signals. This nuanced strategy is not just about capitalizing on trading opportunities but also about elevating our risk management. Each signal is meticulously decoded, producing values that dictate our tactical moves. The primary objective of this strategy is to dynamically rebalance the portfolio in alignment with the generated signals from these indicators. This is not merely a reactive stance but a proactive one, aiming to position the portfolio optimally before shifts in market momentum become apparent to the wider investing community. Our approach is designed to be adaptive, responsive, and continuously refined to capture the nuances of the market.

This portfolio is constructed with the aim of achieving a delicate balance between aggressive growth and conservative stability. The signals generated from our indicators are not just noise but carefully interpreted data points that guide our investment decisions reflecting our meticulous consideration in our risk appetite assessment. 




# **2) Stock Selection**


## <span style="text-decoration:underline;">2.1 Rationale</span> 

In the construction of our backtesting strategy, we have meticulously curated a portfolio of stocks that exemplifies a cross-section of market dynamics. The selection is predicated on the synergy between the unique attributes of each stock and the core principles of our trading strategy—namely, how we do the daily rebalancing of our portfolio

The assemblage of stocks from Apple Inc. (AAPL), Procter & Gamble Co. (PG), NVIDIA Corp (NVDA), Walmart Inc (WMT), and Alphabet Inc (GOOGL) provides a rich tapestry of market environments. It encompasses the technological innovation frontiers, consumer staples resilience, retail sector bellwethers, and the broader technological ecosystem. This selection is instrumental in our endeavour to validate the adaptability and resilience of our trading strategy across multifaceted market conditions and diverse corporate events.

**Apple Inc. (AAPL)**

Apple's continuous cycle of innovation, marked by the introduction of transformative technologies, allows us to assess how our strategy adapts to market-moving events. The company's significant market activities, like stock splits and consistent capital growth, provide a prime environment for testing our portfolio rebalancing tactics and refining our risk management techniques.

**Procter & Gamble Co. (PG)**

PG offers a diversified profile as a leading consumer staples company. Its worldwide presence and strategic brand management, along with efficient operations, create an optimal setting for testing our strategy's resilience in a less volatile, yet active consumer goods market. This helps in verifying the stability of our daily rebalancing approach.

**NVIDIA Corp (NVDA)**

NVDA's leadership in GPUs and forays into AI and machine learning sectors offer insights into the performance of our strategy within rapidly expanding industries. The stock's fluctuations due to technological innovations and industry news allow us to test our strategy’s risk management techniques in varying market conditions without the need for exits, emphasizing the effectiveness of our rebalancing methods.

**Walmart Inc (WMT)**

Walmart's status as a retail giant provides a lens through which to examine consumer spending trends and the performance of the retail sector, especially in an evolving economic setting. The company's efforts in scaling and e-commerce integration offer varied scenarios to evaluate the adaptability of our strategy’s rebalancing processes throughout different retail and economic cycles.

**Alphabet Inc (GOOGL)**

Alphabet's extensive business portfolio provides a comprehensive perspective on the tech sector. Its exposure to regulatory shifts and central role in the digital economy's expansion allows for a thorough evaluation of our strategy's capacity to adjust to quick market changes through our disciplined rebalancing routine.

Summary

The carefully selected stocks provide a rigorous testing framework for our trading algorithm, challenging and thus improving the various strategic aspects of our approach. These companies ensure our backtesting platform is indicative of real-world market nuances, enhancing the credibility of our daily rebalancing procedures. 



# **3) Strategy**


## <span style="text-decoration:underline;">3.1 Core Trading Strategy</span>

Our core trading strategy is predicated on the integration of the Coppock Curve, a momentum indicator, with the RSI, a mean-reversion indicator. This dual-indicator approach is designed to exploit the Coppock Curve's ability to discern long-term trend reversals in conjunction with the RSI’s capability to detect short-term price fluctuations. The interplay between these indicators seeks to align the portfolio with the overarching market momentum while also identifying prime trade entry points, offering a comprehensive perspective of market trends and aiding in the filtration of spurious signals.


## <span style="text-decoration:underline;">3.2 Decoding the Signals</span>

The strategy employs a numerical system to decode the signals generated by both indicators:

The Coppock Curve generates a **` 1 `** when it crosses above zero, signaling a shift to bullish momentum, and a **` -1 `** when it crosses below zero, indicating a shift to bearish momentum.

The RSI generates a **` 1 `** when it crosses above 40 from below, or if it remains above 50, suggesting an emerging bullish momentum. Conversely, a **` -1 `** is generated when the RSI crosses below 70 from above, or if it remains below 50, indicating a potential bearish momentum.

These individual signals from the Coppock Curve and RSI are then combined to ascertain the strength and direction of the market signal:



* A Strong Buy Signal is indicated by a combination of (1,1), resulting in a score of** [ 2 ].**
* A Weak Buy or Sell Signal is indicated by a combination of (1,-1) or (-1,1), each resulting in a score of **[ 0 ]**.
* A Strong Sell Signal is determined by a combination of (-1,-1), yielding a score of **[ -2 ]**.

The different stocks in our stock basket will be issued different scores, reflective of the strategic signals derived from our systematic trading approach.

 


## <span style="text-decoration:underline;">3.3 Portfolio Weights and Capital Allocation</span>

We will converting the scores from the signals into proportional portfolio weights:

A score of [2] corresponds to a weight of 6, indicating a strong bullish signal.

A score of [0] corresponds to a weight of 4, representing a weak or neutral signal.

A score of [-2] corresponds to a weight of 1, indicating a strong bearish signal.

This weighting system adopts a non-linear approach to translate scores into portfolio weights. The relationship between scores and weights in this system is designed to reflect the varying levels of confidence and risk associated with different market signals:

<span style="text-decoration:underline;">A score of [2] : 6 weights</span>

This score is assigned a high weight of 6, reflecting a strategic decision to significantly overweight assets that are expected to perform well. The rationale here is that when the confidence in an asset's positive performance is high, it's beneficial to allocate a larger portion of the portfolio to these assets, thus capitalizing on their anticipated growth.

<span style="text-decoration:underline;">A score of [0] : 4 weights</span>

This score is assigned a weight of 4, representing a neutral stance. This implies that even when the market signal is not strongly positive, there's still a reasonable level of confidence in the asset, warranting a moderate investment.

<span style="text-decoration:underline;">A score of [-2] : 1 weight</span>

The score is assigned a minimal weight of 1, indicating a strategy to significantly underweight assets perceived to have a high risk of underperforming. This decision to allocate a smaller portion of the portfolio to these assets is a risk management tactic, designed to minimize potential losses from assets that are expected to perform poorly.

This non-linear allocation strategy is characterized by aggressive positioning in assets with strong positive signals and a conservative approach to assets with negative signals. It's a tactic that aims to maximize gains from high-confidence opportunities while minimizing exposure to potential downturns. By creating a pronounced difference in weights, the strategy underscores a decisive and proactive stance in portfolio management, emphasizing high conviction in bullish scenarios and cautious prudence in bearish ones.

_An example of daily score to weight trade _


<table>
  <tr>
   <td>
   </td>
   <td>AAPL
   </td>
   <td>PG
   </td>
   <td>NVDA
   </td>
   <td>WMT
   </td>
   <td>GOOGL
   </td>
  </tr>
  <tr>
   <td>Score
   </td>
   <td>0
   </td>
   <td>2
   </td>
   <td>2
   </td>
   <td>-2
   </td>
   <td>0
   </td>
  </tr>
  <tr>
   <td>Weight
   </td>
   <td>6
   </td>
   <td>4
   </td>
   <td>1
   </td>
   <td>6
   </td>
   <td>1
   </td>
  </tr>
  <tr>
   <td>Portfolio Allocation
   </td>
   <td><em>6 / 18</em>
<p>
33%
   </td>
   <td><em>4 / 18</em>
<p>
22%
   </td>
   <td><em>1/18</em>
<p>
6%
   </td>
   <td><em>6/18</em>
<p>
33%
   </td>
   <td><em>1/18</em>
<p>
6%
   </td>
  </tr>
</table>



## <span style="text-decoration:underline;">3.4 Rule Variable Parameters of Coppock Curve strategy</span>

Our strategy is dedicated to continuous improvement and optimization. We engage in an iterative process of refining the Coppock Curve parameters.

The smoothing mechanism of the Coppock Curve is another focal point for optimization. The conventional model utilizes a 10-period Weighted Moving Average (WMA) for smoothing the curve. Our strategy enhances this by incrementing the WMA period by 40 days in each subsequent variation, systematically exploring the impact of these adjustments on the strategy's performance. The 3 parameters we would be testing would be the different values (10, 50, 90) for the WMA period. 

We want to adapt the traditional Coppock Curve to different trading time frames (10, 50, 90) for a longer-term investment strategy and less sensitivity to short-term price fluctuations. For the RSI, the standard parameter for the look-back period is 14 days and we would be using 14 days still. 

We will be adopting these 3 variations for our training period and select the best strategy/variation to evaluate its performance of the testing set.

By methodically varying the WMA period, we aim to identify the most effective configuration that aligns with our portfolio's performance goals. Each variation is meticulously back-tested, ensuring that the adjustments contribute positively to the robustness of the trading mechanism.


## <span style="text-decoration:underline;">3.5 Rebalancing/Position Size/Risk Management </span>

Let’s delve into the critical elements of executing our trading strategy effectively. These rules are the linchpin of our approach, ensuring a disciplined and calculated execution that aligns with our overarching market analysis. 


### 3.5.1 Daily rebalancing

Instead of traditional exit points, our strategy involves daily rebalancing. Each day, the portfolio is adjusted based on the latest signals generated by the Coppock Curve and RSI. If a stock's signal weakens, the portfolio allocation is reduced, and if it strengthens, the allocation is increased. This dynamic and frequent rebalancing approach ensures that the portfolio is always aligned with the current market conditions and reduces the impact of prolonged adverse trends. 


### 3.5.2 Position Size

Management of Position sizing is a key factor in risk control and capital preservation. Our strategy dictates that the size of a position should be proportional to the strength of the signal. Larger positions are initiated in response to Strong Buy or Sell signals, while smaller positions may be appropriate for Weak signals. This dynamic sizing approach allows us to capitalize on high-confidence trades while mitigating risk in more ambiguous market conditions.


### 3.5.3 Risk management

Risk management is embedded in every facet of our strategy. With an emphasis on ensuring that potential gains outweigh potential losses. By adhering to these rules of strategy, we aim to navigate the dynamic landscape of the financial markets with a calculated and disciplined approach, enhancing the probability of success in our systematic trading endeavors through daily portfolio rebalancing.
