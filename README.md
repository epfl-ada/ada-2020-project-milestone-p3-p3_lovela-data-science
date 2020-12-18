# Project Proposal: Understanding the Impacts of China-US Trade War

### 1. Title 

**Understanding the Impacts of China-US Trade War**

["Click here to access our data story"](https://jenscode-trash.github.io/lovela-data-science-TradeWar/) to visit our website.

Please consider consulting the file called `project_notebook.html` in order to see our entire work without having to run the notebook `project_notebook.ipynb`.

### 2. Abstract

Since the paper introduces interrupted time series (ITS) analysis as a practical method for event’s impact evaluation, we propose to study if we can apply ITS analysis to a different scenario: the China-United States trade war. To do so, we collect several different types of datasets (e.g., U.S. Trade in Goods with China, US foreign trade with product details) from the United States and China’s official website. We will then use ITS analysis on these datasets and see if there exists a significant impact on China-US trade. Moreover, we may try to extend the ITS analysis method to better interpret multiple events and other factors. The visualization of analysis will allow us to understand the economic outcomes easily. Apart from the general implications for exports and imports, we are also interested in investigating further into other aspects of the trade war: increasing tariffs during the trade war, different levels of impacts in various industries, the resulting change in the trade of their business partners such as the European Union. All these results would provide us with a deeper understanding of the impacts of the trade war, and we would try to interpret them from different perspectives.



### 3. Research questions

1. (**General**) How does the trade war affect the bilateral trade (i.e., exports, imports) between China and the US？Which country's products are more competitive？
2. (**Different Industries**) Which industry/sector has undergone the most severe decline in the trade war?
3. (**Multilateral International Trade Relationships**) What’s the change in the trade amount of China and the US with their primary business partners?



### 4. Proposed datasets

a. ["U.S. Trade in Goods with China"](https://www.census.gov/foreign-trade/balance/c5700.html) from the United States Census website. 
This dataset records monthly trade amounts (from 1985 to 2020) between the U.S. and China, concerning the exports, imports, and balance. We will use the exports and imports data from 2016 to 2020 to assess the trade trend before and after the trade war breakout.

b. ["US foreign trade with product details"](https://www.census.gov/foreign-trade/statistics/country/sitc/index.html) from the United States Census website.
This dataset gives out monthly trade amounts (from 2015 to 2020) between the U.S. and its partner countries, about the industry/sector, exports, imports, and balance. We will use the exports, imports, and industry/sector to analyze the trade war impact on different industries/sectors.

c. ["U.S. Trade in Goods with foreign countries"](https://www.census.gov/foreign-trade/statistics/country/index.html) from the United States Census website and ["China Trade in Goods with foreign countries"](http://www.customs.gov.cn/customs/302249/302274/302277/3227050/index.html) from China General Administration of Customs website. 
The first dataset from the U.S. records monthly trade amounts (from 1985 to 2020) between the U.S. and its partner countries, concerning the exports, imports, and balance. The second dataset records monthly trade amounts (from 2014 to 2020) between China and its partner countries, concerning the exports and imports.We plan to use the exports and imports data from 2016 to 2020 to see if the trade war also impacts the trade amount of the U.S. and China with their other business partners.

d. ["Global Merchandise Trade"](https://stats.oecd.org/Index.aspx?DataSetCode=MEI_TRD#) from Organisation for Economic Co-operation and Development (OECD).
This dataset records monthly international trade from 1950 to 2020. We will export the "Monthly International Merchandise Trade" (IMTS) series from 2016-01 to 2020-10.

e. ["Longer China Trade from WTO"](https://data.wto.org/) from WTO.
The dataset records annually international trade from 1948 to 2020. We will use this dataset to explore the trade relationship between China and its trade partners from 1996 to 2018.



### 5. Methods

Following the analysis in “Chilling Effects”, we will use the ITS approach to study the impact of the policy put forward in the China-US trade war:

**Data Collection**: To merge the proposed datasets above, we need to filter out the selected industries’ data in the dataset (b) and selected partners in (c). Then, we will form the split dataset to analyze different research questions.

**Segmented Regression Analysis**: We will regard the trade war's breakout time (March 2018) as an intervention in the bilateral trade relationship and apply segmented regression analysis. We expect to interpret the change in overall exports and imports and the change of their trends with the results.

**Performance Improvement**: Given the particularity of the problem (ongoing trade conflict and widespread impacts), we are trying to extend the ITS design to interpret the event in our scenario better.

**Study of Impacts on Different Industries**: We will group the data by categories and use the same methods to study the change. With the statistical comparison, we can discover the impact of different industries in the trade war. We will also include a case study to illustrate how the trade war impacted a specific sector.

**Multilateral International Trade Relations Study**: We will also study the change brought to different related partners and connection topologies. We are still discussing the possible analysis applied in this problem.

**Interdisciplinary Comparative Research**: Our project topic and research questions are closely related to international trade and economics to compare our conclusions with their recent research in the China-US trade war. The interdisciplinary comparative research could provide us with an excellent opportunity to verify and further discuss our analysis results.



### 6. Proposed timeline

- **Step1** (Dec 1st):  Data preparation and data cleaning: Since the proposed datasets include many different data resources, it takes efforts to merge them together for further analysis. Also, for different research questions, we need to form different subsets (e.g., different industries, different business partners).Research segmented regression analysis and visualization methods.

- **Step 2** (Dec 5th): Implement our data analysis methods and visualizations. Make an outline of the data story. Interdisciplinary comparative research to validate our analysis. 

- **Step 3** (Dec 12th):  Improve data visualization, finish the final version of the notebook, and revise the data story.

	 **Step 4** (Dec 18th):  Get our data story and presentation video prepared.	



### 7. Organization within the team

- **Step 1** (Dec 1st): YiHsin will handle data preparation and data cleaning. We need to form the different datasets for our proposed research questions. Lin and Wanqi will try to research segmented regression analysis and visualization methods. They will form the draft design of the analysis.
- **Step 2** (Dec 5th): Lin and YiHsin will implement the data analysis methods and visualizations. Wanqi will be assigned with making an outline of the data story.
- **Step 3** (Dec 12th): The team needs to discuss together to revise the data story, after Lin doing the interdisciplinary comparative research. Wanqi and YiHsin will improve the analysis and visualization results.
- **Step 4** (Dec 18th): All the members need to prepare their own responsible part in the project in the final data story and the presentation video.



### 8. Questions for TAs

1. Are we allowed to make some adjustments to our proposal, given that some dataset may be out of expectations in the real analysis?
2. Can you provide us with some suggestions on the improvement of segmented regression analysis?



### 9. Contributions of all group members

- Yuan Lin: Implement data analysis methods and research visualization methods; Mainly focus on research question 1; Data visualization for part 1; Revise data story
- YiHsin Jen: Handle data preparation/cleaning on proposed datasets; Mainly focus on research question 3; Data visualization for part 2; Revise data story
- Wanqi Hong: Build data story webpage; Mainly focus on research question 2; Data visualization for part 3; Revise data story