# Project Proposal: Understanding the Impacts of China-US Trade War

### 1. Title 

**Understanding the Impacts of China-US Trade War**

### 2. Abstract

Since the paper introduces interrupted time series (ITS) analysis as a practical method for event’s impact evaluation, we propose to study if we can apply ITS analysis to a different scenario: the China-United States trade war. To do so, we collect several different types of datasets (e.g., U.S. Trade in Goods with China, US foreign trade with product details) from the United States and China’s official website. We will then use ITS analysis on these datasets and see if there exists a significant impact on China-US trade. Moreover, we may try to extend the ITS analysis method to better interpret multiple events and other factors (e.g. tariffs). The visualization of analysis will allow us to understand the economic outcomes easily. Apart from the general implications for exports and imports, we are also interested in investigating further into other aspects of the trade war: increasing tariffs during the trade war, different levels of impacts in various industries, the resulting change in the trade of their business partners such as the European Union. All these results would provide us with a deeper understanding of the impacts of the trade war, and we would try to interpret them from different perspectives.



### 3. Research questions

1. (**General**) How does the trade war affect the bilateral trade (i.e., exports, imports) between China and the US？Which country's products are more competitive？
2. (**Tariffs**) Does the increasing tariff have direct impacts on the trade？
3. (**Different Industries**) Which industry/sector has undergone the most severe decline in the trade war?
4. (**Multilateral International Trade Relationships**) What’s the change in the trade amount of China and the US with their primary business partners?



### 4. Proposed datasets

a. ["U.S. Trade in Goods with China"](https://www.census.gov/foreign-trade/balance/c5700.html) from the United States Census website. 
This dataset records monthly trade amounts (from 1985 to 2020) between the U.S. and China, concerning the exports, imports, and balance. We will use the exports and imports data from 2016 to 2020 to assess the trade trend before and after the trade war breakout.

b. ["US-China Trade War Tariffs: An Up-to-Date Chart"](https://www.piie.com/research/piie-charts/us-china-trade-war-tariffs-date-chart) from the Peterson Institute for International Economics (PIIE).
This dataset presents the bilateral tariffs change during the trade war, paired with the corresponding events. We are planning to use it to analyze the effects of increasing tariffs.We will need to enrich the dataset because its timespan does not cover the period before the trade war (2016 and 2017).

c. ["US foreign trade with product details"](https://www.census.gov/foreign-trade/statistics/country/sitc/index.html) from the United States Census website.
This dataset gives out monthly trade amounts (from 2015 to 2020) between the U.S. and its partner countries, about the industry/sector, exports, imports, and balance. We will use the exports, imports, and industry/sector to analyze the trade war impact on different industries/sectors.

d. ["U.S. Trade in Goods with foreign countries"](https://www.census.gov/foreign-trade/statistics/country/index.html) from the United States Census website and ["China Trade in Goods with foreign countries"](http://www.customs.gov.cn/customs/302249/302274/302277/3227050/index.html) from China General Administration of Customs website. 
The first dataset from the U.S. records monthly trade amounts (from 1985 to 2020) between the U.S. and its partner countries, concerning the exports, imports, and balance. The second dataset records monthly trade amounts (from 2014 to 2020) between China and its partner countries, concerning the exports and imports.We plan to use the exports and imports data from 2016 to 2020 to see if the trade war also impacts the trade amount of the U.S. and China with their other business partners.

### 5. Methods

Following the analysis in “Chilling Effects”, we will use the ITS approach to study the impact of the policy put forward in the China-US trade war:

**Data Collection**: To merge the proposed datasets above, we need to filter out the selected industries’ data in the dataset (c) and selected partners in (d). Then, we will form the split dataset to analyze different research questions.

**Segmented Regression Analysis**: We will regard the trade war's breakout time (March 2018) as an intervention in the bilateral trade relationship and apply segmented regression analysis. We expect to interpret the change in overall exports and imports and the change of their trends with the results.

**Performance Improvement**: We will use the Prais-Winsten method to correct auto-correlation and try to improve the results. Furthermore, given the particularity of the problem (ongoing trade conflict and widespread impacts), we are trying to extend the ITS design to interpret the event in our scenario better.

**Reliance on the Tariffs**: Because the rising tariffs also reflect the trade war's intensity, we think it is essential to consider it. We will apply the regression analysis with the bilateral tariffs and study its correlation with the trade volume.

**Study of Impacts on Different Industries**: We will group the data by categories and use the same methods to study the change. With the statistical comparison, we can discover the impact of different industries in the trade war. We will also include a case study to illustrate how the trade war impacted a specific sector.

**Multilateral International Trade Relations Study**: We will also study the change brought to different related partners and connection topologies. We are still discussing the possible analysis applied in this problem.

**Interdisciplinary Comparative Research**: Our project topic and research questions are closely related to international trade and economics to compare our conclusions with their recent research in the China-US trade war. The interdisciplinary comparative research could provide us with an excellent opportunity to verify and further discuss our analysis results.



### 6. Proposed timeline

- **Step1** (Dec 1st):  Data preparation and data cleaning: Since the proposed datasets include many different data resources, it takes efforts to merge them together for further analysis. Also, for different research questions, we need to form different subsets (e.g., different industries, different business partners).Research segmented regression analysis and visualization methods.

- **Step 2** (Dec 5th): Implement our data analysis methods and visualizations. Make an outline of the data story. Interdisciplinary comparative research to validate our analysis. 

- **Step 3** (Dec 12th):  Improve data visualization, finish the final version of the notebook, and revise the data story.

	 **Step 4** (Dec 18th):  Get our data story and presentation video prepared.	

  (Further details of each milestone will be added with the progress.)



### 7. Organization within the team

- **Step 1** (Dec 1st): YiHsin will handle data preparation and data cleaning. We need to form the different datasets for our proposed research questions. Lin and Wanqi will try to research segmented regression analysis and visualization methods. They will form the draft design of the analysis.
- **Step 2** (Dec 5th): Lin and YiHsin will implement the data analysis methods and visualizations. Wanqi will be assigned with making an outline of the data story.
- **Step 3** (Dec 12th): The team needs to discuss together to revise the data story, after Lin doing the interdisciplinary comparative research. Wanqi and YiHsin will improve the analysis and visualization results.
- **Step 4** (Dec 18th): All the members need to prepare their own responsible part in the project in the final data story and the presentation video.



### 8. Questions for TAs

1. Are we allowed to make some adjustments to our proposal, given that some dataset may be out of expectations in the real analysis?
2. Can you provide us with some suggestions on the improvement of segmented regression analysis?

### TODO:
YiHsin: 
- find new longer dataset for China trade(已找到)(https://trendeconomy.com/data/h2?commodity=TOTAL&reporter=China&trade_flow=Export,Import&partner=World&indicator=NW,TQ,TV&time_period=2008,2009,2010,2011,2012,2013,2014,2015,2016,2017,2018,2019)
- bar chart on trade partner排名
- world map (以年為單位)
- combine original ITS to subplot(同時把code更精簡)
- top5 partner受貿易戰程度的影響
    - 預計使用公式: |postslope.coeff/time feature|