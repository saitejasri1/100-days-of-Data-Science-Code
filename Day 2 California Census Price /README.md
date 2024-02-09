# California Housing prices dataset from the StatLib Repository taken from the 1990 California Cenus.

# Assumptions and business objective:
 Aim: To predict the housin_prices in the california state from the California Census Data.

 Features included in te dataset that could weigh more for the prediction of our dataset.
        1. Population
        2. Median Income
        3. Median housing price for each block group in California. where the block group has a population of 600 to 3000 and let's call it as districts.

 Based on the above features I consider it as regression model.

# Question to be asked:
    "How can the model that we use or implement help the company?"

# Introduction and notes:
The dataset conists of categorical features and continous featuers.
We have two CSV file named houisng.csv and anscombe.csv.
(20640, 10), (44, 3) are the dimensions for the above datasets repectively. 


# Housing Dataset:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 20640 entries, 0 to 20639
Data columns (total 10 columns):
 #   Column              Non-Null Count  Dtype               My assumptions
---  ------              --------------  -----    ----------------------------------------------------------
 0   longitude           20640 non-null  float64  #Laitude doesn't semm like influence feature
 1   latitude            20640 non-null  float64  #Longitude also doesn't seem like influence feature
 2   housing_median_age  20640 non-null  float64  # Maybe how old the house effect the pricing of the house
 3   total_rooms         20640 non-null  float64  #Linear relationship. more rooms more cost
 4   total_bedrooms      20433 non-null  float64  # same like total_rooms
 5   population          20640 non-null  float64  # more the population more the requirement for the house
 6   households          20640 non-null  float64  # a 50- 50 influence on data
 7   median_income       20640 non-null  float64  # definetely require for prediction
 8   median_house_value  20640 non-null  float64  # same like above
 9   ocean_proximity     20640 non-null  object   # near the ocean more the price
dtypes: float64(9), object(1)
memory usage: 1.6+ MB

If we consider the above info regarding the housiong data we can observe that some values are missing from the total_bedrooms and all the columns have same dtat type except the ocean_proximity. I think it could be a categorical variable.


ocean_proximity
<1H OCEAN     9136
INLAND        6551
NEAR OCEAN    2658
NEAR BAY      2290
ISLAND           5
Name: count, dtype: int64

Ocean_proximity is a categorical variable with 5 categories in it.