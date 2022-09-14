# Cryptocurrencies

## Purpose
The goal of this analysis was to determine if a list of cryptocurrencies
could be grouped using a selection of data points and the k-means clustering
algorithm

## Data
- Data was sourced from Cryptocompare.com
- Data points or features include:
  - Coin Name
  - Hashing Algorithm
  - Proof Type
  - Total Coins Mined
  - Total Coin Supply
- Data was filtered to include
  - only actively trading coins
  - coins with supply greater than 0

## Tools

*Data Cleaning*:

`pandas`

*Analysis tools*:

**sklearn**: `StandardScaler`,`MinMaxScaler`, `PCA`, `KMeans`

*Visualization tools*:

`plotly express`, `hvplot`

## Process
Coin data was filtered as above and transformed as follows:
-  Dummy variable were created to encode coin names and proof type for analysis
- This process resulted in a dataset with 98 features
- All data points, including the newly created dummies, were scaled using StadardScaler
- Principal component analysis was run on the scaled dataset to reduce
features to 3
- KMeans was run to categorize each coin into a cluster group.
- The total number of clusters used was 4, a number arrived at with the help of an elbow curve.
- Data was plotted on 2-d and 3-d plots to visually confirm clustering results.