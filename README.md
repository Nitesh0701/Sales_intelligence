#### Part 1



1\. What is the real business problem?

The visible issue is that the company’s win rate has declined, we have to understand what factors are causing the decline,Where risks exist in the pipeline and What actions can improve revenue outcomes.





2\. What key questions should an AI system answer for the CRO?

The AI system should answer the things about pipeline health like if the sales cycle getting longer?,are deals getting stuck in some stages, it should tell about performance drivers like which lead sources produce the best conversions?,Which industries or regions have the highest and lowest win rates? and risk identification like are high vale deals are greater risk? which deals have exceeded normal sales cycle duration





3\. What metrics matter most for diagnosing win rate issues?

There are some matrics that helps to diagnose win rate issues

&nbsp;Average sale cycle length - time taken to close deals. sometimes longer the sale cycle length lower the win rate.

&nbsp; win rate by segment - like region, industry, lead source, product type helps identify which segments are underperforming. and Average Deal Size (Won vs Lost) Helps identify whether larger deals are harder to close.



4\. What assumptions are being made about the data or business?

Completeness and consistency of the data and No Major Structural Changes in the Sales Process

The analysis assumes that the sales process, pricing strategy, and target market remained relatively stable during the time period covered by the data. Major changes in strategy could influence win rates independently of the factors measured here.





#### Part 3



##### Option B – Win Rate Driver Analysis

#### 

**Problem** **Definition**: The sales organization is experiencing a decline in win rate despite maintaining a healthy pipeline volume. Leadership needs to understand which factors are influencing deal outcomes and what actions can improve conversion rates.





A rule-based decision engine was designed using insights derived from exploratory data analysis.Higher variation indicates a stronger potential impact on deal outcomes



The following drivers were analyzed:



* Lead source performance
* Industry performance
* Sales representative performance
* Deal size trends



These factors were chosen because they influence conversion rates and are actionable from a business perspective.



The decision engine does 3 things:



* Measures win rate by factors
* Identifies strongest drivers
* Generates actionable insights



**Key Findings:**



\- Lead source variation is small



\- Industry variation is small



\- Sales rep variation is larger



\- Sales cycle not strong



Sales cycle duration does not show a strong separation between won and lost deals, suggesting that deal duration alone is not a reliable predictor of success.

Win rate differences across lead source and industry are relatively small, suggesting these factors alone do not strongly determine deal success.

However, variation across sales representatives is more noticeable, indicating that execution quality or sales strategy may have a stronger influence on outcomes.





**A sales leader could use this system to**:



* Identify high and low performing sales representatives
* Focus coaching efforts where win rates are lowest
* Monitor pipeline health by segment
* Investigate deal execution practices among top performers







#### Part 4



##### Mini system Design



The goal of the Sales Insight \& Alert System is to continuously monitor sales pipeline data, identify trends affecting win rates, and generate actionable insights for sales leaders.



**Architecture:**



&nbsp;so the system will have 4 components



1- Data injection layer

2- Processing and analytics

3- Insight generation engine

4- Alerting and dashboard layer



Data Ingestion Layer: Sales data is collected from CRM systems (such as Salesforce or HubSpot etc).

The data includes deal details, stages, outcomes, lead sources, and sales representatives and details required.



Processing and analytics : here Data is cleaned, transformed, and aggregated to compute key metrics such as win rate, sales cycle duration, and deal distribution across dimensions like region and industry.



Insight generation engine : A rule-based decision engine evaluates win rates across different dimensions and identifies drivers showing significant variation. The engine generates insights such as Segments with declining win rates, Performance variation across sales representatives.



Alerting \& Dashboard Layer : Here Insights are delivered to sales leaders through dashboards and automated alerts.

example - Alerts may be triggered when:Win rate drops below a threshold,A region or segment underperforms







**Data Flow :**



The system operates in the following sequence 

Sales data is extracted from the CRM system ---> Data is cleaned and transformed -->Metrics and win rate drivers are computed ---->Insights and alerts are generated --->Results are displayed on dashboards or sent via notifications





**Example Alerts or Insights:**



Alerts like - "Win rate for a specific sales representative dropped below 40% this month"

--"Lead source performance declined compared to the previous quarter"

-- "A region shows unusually high deal loss rates"

-- "Pipeline volume is increasing but win rate is decreasing"

-- "A high percentage of deals are being lost in the same stage of the pipeline"





**How Often It Runs:**

The system can run on a daily or weekly schedule depending on business requirements.

Daily processing helps identify risks early, while weekly reporting is useful for strategic reviews.





**Failure Cases and Limitations:**



-- Rule-based insights may miss complex relationships between variables

-- Sales processes and market conditions may change over time, requiring periodic recalibration of rules

-- Win rate may be affected by external factors such as competition, seasonality, or pricing changes, which may not be reflected in internal CRM data.





#### Part 5



1\. What assumptions in your solution are weakest?



In real-world scenarios, the system could be affected by data quality issues such as missing or inconsistent CRM records, which may impact metric calculations and insights,

One of the weakest assumptions in this analysis is that win rate drivers can be evaluated independently. In reality, deal outcomes are often influenced by combinations of factors such as industry, deal size, and sales execution working together.







2\. What would break in real-world production?



Changes in sales processes, pricing strategies, or territory assignments could also impact win rates in ways that the system may not immediately capture.

or if we are taking small sample sizes - small sample sizes in certain segments could produce misleading insights if not handled carefully.

also system could be affected by data quality issues such as missing or inconsistent CRM records.







3\. What would you build next if given 1 month?



Developing an interactive dashboard for real-time monitoring of pipeline health, Building a predictive model to estimate win probability for open deals







4\. What part of your solution are you least confident about?



The part I am least confident about is determining the true strength of win rate drivers using limited variables. Without additional contextual data such as customer engagement or competitive factors, it is difficult to fully explain why deals are won or lost. This analysis provides directional insights, but deeper investigation would be required.

