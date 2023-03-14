
# Code Brews
###### Collaboraters:
###### Nathon Burwick, Rod Hughes, Victoria Sanders, Jason Hanlin,
###### Kelly Hendre, Jarvis Moy, Lynn Orr, Wen Chiou, Talita Urzenda
## Project Description

We are a brewery, Code Brews, looking to expand to a new location. Our goal is to determine potentially successful business locations based on 
- Selling price of imported and domestic beer 
- Monthly expenses
- Number of customers 
- Transportation costs  
- Production costs
- Location

We will use data sets with various cost of living data for cities and countries across the world, but focus our search on US cities only.  We will build visualizations to attempt to relate various costs of goods and services to cities and city attributes.  We will combine data sets to find insights for the perfect market area that might not be apparent to our other competitors.  

These are our questions and findings...

## Transportation Cost & Pricing Analysis

1. What correlations can we see in average monthly income and average cost of beer as well as the  transportation cost and price of beer?
    - Is there a correlation to average income and pricing in an given area?
    - Include domestic and imported beer findings
    
This exploration is looking for any relationships between the cost of transportation and the cost of beer that will help in selecting a good market for opening our brewery.  First, we determined which transportation metric to use.  We have cost of living costs for taxi rides, transit rides, and gas costs.  Since we are a responsible brewery and want to encourage taking rides (taxi or transit) as opposed to driving when drinking our beer, we focus on taxi and transit transportation.  We want to further encourage this by finding cities with cheaper rides. With this in mind, we have created a  “Ride Mode Index,” which is a combination of a 1km taxi ride and a one-way local transit ticket. We want to compare this ride index with the cost of beer; in this case, the cost of a domestic beer in a restaurant.  

Figure 1 - Transportation versus Beer Cost displays cities that have both cheap beer and cheap rides that have the potential to be cities that customers want to go out to.  Both of these factors encourage the consumption of our product, and therefore, are better for business.  Cities on the lower left of the chart describe cities with cheap beer and cheap transportation. These are ideal cities to go out to bars or parties and drink up without having to worry about drinking and driving. These include cities like Greenville, Shreveport, or Denton. However, there is a caveat, cheap beer markets might make it more difficult to sell our products with a margin sufficient to turn a profit. So, we may want to focus on markets with cheap transportation and moderate beer pricing, like Yakima, Rogers, Missoula, Worcester or even Fargo, Austin, and Frederick.  

Bottom line, we want to avoid markets with high costs of transportation that might encourage customers to drive themselves.  Figure 1b - Cheapest Cities for Transportation displays the Top 20 cheapest cities to get a ride (taxi and transit). We take this a step further by analyzing the correlation between the average price of domestic and imported beer and average income in a particular area.

In this piece of our analysis we use the average price of imported and domestic beer to represent the relative supply and demand of beer in an area. This is also used to measure the viability of the beer market in the city. In order to determine if there is a relationship, we took the average of both imported and domestic beer prices for the city and them with with the average income for the same city. Our data demonstrates a moderately strong correlation between the variables with a correlation coefficient of 0.65.

We use the regression line to determine a good price point of the beer based on the average income of the city.
Because there is a strong correlation between the average price of beer and the average monthly income, we can take the top ten cities with the highest monthly income to create a condensed list of potential sites for our brewery.

## Customer Profile Analysis

2. How does household type vs. location affect our target market?
    - Can these factors increase or decrease our product value?
    
In order to answer this question, we merged two csv files that contain population growth and US census data to analyze the US population growth and the different household types within each state to gather insight of our demographic. 

By cleaning up our data to contain specific columns like each household type, city and state, and population growth, we were able to compose two bar graphs. In order to narrow down our search even further,  we gathered the top 10 cities with the highest number of household types. With this cleaned up data we created the "Number of Household Types in US Cities" grouped bar chart. 

In this grouped bar chart, we can easily visualize how many different household types are in each of our top 10 cities. We see that California, specifically Los Angeles, San Diego, Sacramento, and Chico contain the most nonfamily households(red bar) and married households(blue bar). Following California, Texas cities like Austin, Dallas, Houston, Fort Worth, and College Station constain the most cities with potential consumers as well. Because the nature of our business venture typically attracts couples and single consumers, we can assume that these two household types in these two states are our target audience. 

Aside from this visualization, we created a bar chart that focuses on the population growth of these top 10 cities. With this chart, we can see that all of these cities have experienced -2% to 1% growth. California contains the most cities with zero growth, Chicago contains the highest decrease in growth, and Texas contains the highest increase in growth. With this information, we may consider California and Texas as top contenders for Code Brews’ location because they have not experienced negative growth.  

So, with these finidngs, we can conclude that we will have a steady customer base in California or potentially a growing one in Texas. 

## Customer Spending Profile

3. On average, do people tend to spend more than they have? 
    -Is this a positive or negative trait for Code Brews?

On average, domestic beer is 86% of the price of imported beer. In the chart, 'Restaurant vs Home Beer, Domestic vs Import, Beer vs Food' we are focused on cities where customers are willing to pay a premium for domestic beer, so the selected cities demonstrate this.

When examining this data, we need to look at the basics of our business: operating a brewery depends on people who enjoy drinking out, as opposed to people who enjoy drinking at home. In our dataset, the average stay-at-home consumer spends \\$2.56 on a 12 oz bottle of domestic beer. Meanwhile, the average leave-the-home consumer spends about \\$5.08 on a 12 oz bottle of domestic beer. This shows that ordering a beer at a restaurant is about 2 times more expensive than drinking a beer at home. Therefore, to keep price relative to average, we will cap the restaurant beer to 3 times the price of having a beer at home.  

Because our brewery will offer food in addition to beer, we decided examine the ratio between money spent on a meal at an inexpensive restaurant and the cost of a beer. Across all cities, the average customer spends about 1/3 of the cost of food on beer. Through this selection of cities, we focused on customers who are willing to pay more than 50% of the cost of food on the cost of a beer. Beer is our business' number one product, so coupling the purchase of beer with food is an accepted addtion to potential profit.

## Production Cost Estimation

4. Can Code Brews estimate our beer production costs relative to each state from the available data (i.e. water cost and electricity/utility cost)?  
    -How does this impact our headquarters selection?

Estimating production costs allows for many assumptions to be made on behalf of expenses and sales. Revenue assumes the new brewery produces an equal share of the local craft beer in the city. Beer consumption per city is estimated using state beer consumption per capita and city population, and it assumes that all produced beer is sold in the taproom and none is distributed elsewhere.

Multiple sources allow us to draw expense estimates. Utilities and rent are estimated using a cost of living dataset. Labor is estimated using the latest state minimum wage and hours are fixed for all cities. The tax estimate includes a flat 21% on revenue and state beer excise taxes.
With all of this, in order to calculate the profit margin, we use this formula: (revenue - expenses)/revenue. We created a subset of data to showcase the top 10 cities within analysis that contain highest profit margins. Please refer to the data below:

| City | State | Profit Margin |
| ---- | ----- | ------------- |
| Los Angeles | CA | 61% |
| Houston | TX | 56% |
| Memphis | TN | 40% |
| Dallas | TX | 40% |
| Ft. Worth| TX | 40%|
| San Diego | CA | 37% |
| Austin | TX | 35% |
| Jacksonville | FL | 29% |
| Columbus | OH | 27% |
| Baton Rouge | LA | 23% |

These cities contain relatively high populations, and production sales were assumed based on beer consumption per capita, likely driving the high revenue figures for these cities. Also, note that two large cities in California make the list - California contains a high population and large brewing scene, but our expense calculation do not account for taxes other than the 21% flat and excise tax, so we are not inclined to lean towards the California margin numbers.

In order to determine the viability and competitiveness of opening up a new brewery, we gathered the following data from a sample of cities in the United States:

 - Number of people over the age of 19 in a city 
 - Number of breweries in a city 

The U.S. Census does not provide data for the age of 21 and above, only 20 and above. Even though 20 is not of legal drinking age in the U.S, we believe the percentage of age 20 in the dataset is not statistically significant enough to skew the results due to the sheer volume of the dataset as we are also looking to project revenues upon opening. From the data points above, the number of potential customers per brewery was calculated. 

In the bar chart depicting city, state, # of breweries in the city, and people per brewery, we see that the higher the number of potential customers per brewery, the higher the chance of a new brewery being profitable. We can also assume less competition with this piece of data.

In conclusion, after gathering all of our data and finding the common denominator city that offers practical transportation, our ideal customer base and spending habits, healthy cost estimates, and overall potential profits, we can confidentally select Austin, Texas as our ideal location for Code Brews.


### Data Sets Used:
 - US Census Buerau - API Collection
 - Cost of Living Data - Kaggle - https://www.kaggle.com/datasets/mvieira101/global-cost-of-living?select=cost-of-living.csv
 - Craft Beer Data - Kaggle - https://www.kaggle.com/nickhould/craft-cans
 - Open Brewery DB - API
 - 2018 Per Capita Beer Consumption: https://www.kaggle.com/datasets/osamaabdullatif/apparent-per-capita-alcohol-consumption-19772018
 - 21% Tax Rate (for some corporations): https://www.irs.gov/publications/p542#en_US_202201_publink1000257885
 - State Minimum Wage: https://www.dol.gov/agencies/whd/minimum-wage/state
 - State Liquor Licenses: https://ballotpedia.org/Liquor_license_costs_by_state,_2018
 - 2021 Market Share: https://www.brewersassociation.org/statistics-and-data/national-beer-stats/
 - American Pilsner Homebrew Recipe: https://www.homebrewersassociation.org/homebrew-recipe/big-brew-2013-recipe-classic-american-pilsner/
 - Corn & Barley Pricing: https://moonshinedistiller.com/ingredients/distilling-grains/ 
 - Yeast and hops Pricing: https://www.morebeer.com/category/brewing-ingredients.html
 - State Beer Excise Taxes: https://taxfoundation.org/state-beer-taxes-2021/


