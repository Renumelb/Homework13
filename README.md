# Homework13- Clustering Crypto
In this homework assignment, you will put your new unsupervivsed learning into action by clustering cryptocurrencies and creating plots to present your results.You are asked to accomplish the following main tasks:

1. Data Preprocessing: Prepare data for dimension reduction with PCA and clustering using K-Means.
2. Reducing Data Dimensions Using PCA: Reduce data dimension using the PCA algorithm from sklearn.
3. Clustering Cryptocurrencies Using K-Means: Predict clusters using the cryptocurrencies data using the KMeans algorithm from sklearn.
4. Visualizing Results: Create some plots and data tables to present your results.

Steps:
1. Using the provided CSV file, create a Path object and read the file data directly into a DataFrame named crypto_df using pd.read_csv().
2. With the data loaded into a Pandas DataFrame, continue with the following data preprocessing tasks.
    -Keep only the necessary columns: 'CoinName','Algorithm','IsTrading','ProofType','TotalCoinsMined','TotalCoinSupply'
    -Keep only the cryptocurrencies that are trading.
    -Keep only the cryptocurrencies with a working algorithm.
    -Remove the IsTrading column.
    -Remove all cryptocurrencies with at least one null value.
    -Remove all cryptocurrencies that have no coins mined.
    -Drop all rows where there are 'N/A' text values.
    -Store the names of all cryptocurrencies in a DataFrame named coins_name, use the crypto_df.index as the index for this new DataFrame.
    -Remove the CoinName column.
    -Create dummy variables for all the text features, and store the resulting data in a DataFrame named X.
    -Use the StandardScaler from sklearn to standardize all the data of the X DataFrame. 
3. Use the PCA algorithm from sklearn to reduce the dimensions of the X DataFrame down to three principal components to create a DataFrame named pcs_df using as columns names "PC 1", "PC 2" and "PC 3";  use the crypto_df.index as the index for this new DataFrame.
4. Use the KMeans algorithm from sklearn to cluster the cryptocurrencies using the PCA data. Note that the number of clusters that are to be used based on elbow curve may change when you re-run the code.
5. Create a 3D-Scatter using Plotly Express to plot the clusters using the clustered_df DataFrame.
6. Use hvplot.table to create a data table with all the current tradable cryptocurrencies. 
7. Create a scatter plot using hvplot.scatter, to present the clustered data about cryptocurrencies.
