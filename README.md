# CryptoClustering
This ReadMe serves to:
   1. Certify that this work is my own,
   2. Specify code source and its location in my 'CryptoClustering' repository,
   3. Explain the process of the challenge


1. 
My name is Brittney Watts, and this challenge is a product my own work from my interpretation of the material I learned in class with some help from forums.

2. 
The source code is my interpretation of the information we have learned in class with some debugging help from forums, and here
is a breakdown of the locations of each element of my assignment:

    CryptoClustering
        CODE
            Resources
                crypto_market_data.csv
            crypto_market_data.ipynb    
        README.md


CryptoClustering:
   My task was to read the data from the "crypto_market_data.csv" file and perform a market prediction on stock data! For this deliverable, I used pandas and hvplot, and scikit-learn's StandardScalar(), KMeans, and PCA modules to scale, analyze, and predict the stock market data.
   The crypto_market_data.csv file lists Crypto Currencies and their price change percentages for 24h, 7-day, 14-day, 30-day, 60-day, 200-day, and 1-year intervals. 
   
3.
My Steps:     

    - PART 1: PREPARING THE DATA
        - First, I loaded the crypto_market_data.csv into a DataFrame and retrieved the summary statistics of the data for a pre-prediction analysis.
        - Used the StandardScaler() module to normalize the crypto_market_data.
        - set the index for 'coin_id' to a new DataFrame with scaled data.

    - PART 2: FIND THE BEST VALUE FOR K 
        - Created lists for inertia values and 'k' values.
        - Added to the inertia list with a for loop that computed the intertia for each value of k.
        - Created a dictionary to hold the values.
        - Plotted a line chart to visualize the data and find the best value for 'k'.
    
    - PART 3: CLUSTERING WITH KMEANS 
        - Initialized KMeans model with n_clusters = best value for 'k'
        - Fit the KMeans model using scaled data
        - Predicted the clusters 
        - Created a copy of the original data with a new column for the predicted clusters.
        - Created a scatter plot with the clusters

    - PART 4: OPTIMIZING CLUSTERS WITH PRINCIPAL COMPONENT ANALYSIS
        - Performed a PCA and redued the features to 3 principal components
        - Calculated the explained variance (to determine how much info can be attributed to each principal component)
        - Created a new DataFrame with the PCA data with the index as 'coin_id'

    - PART 5: FINDING THE BEST VALUE OF K WITH THE PCA DATA
        - Created lists for inertia values and 'k' values.
        - Added to the inertia list with a for loop that computed the intertia for each value of k.
        - Created a dictionary to hold the values.
        - Plotted a line chart to visualize the data and find the best value for 'k'.

    - PART 6: CLUSTERING PCA DATA USING KMEANS
        - Initialized KMeans model with n_clusters = best value for 'k'
        - Fit the KMeans model using PCA Data
        - Predicted the clusters 
        - Created a copy of the original data with a new column for the predicted clusters.
        - Created a scatter plot with the clusters


THANK YOU!!!!!
