# crypto_clustering
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data Martha works with is not ideal and must be processed to fit a machine learning model. Since there is no known output that Martha is looking for, she decides to use unsupervised learning. To group cryptocurrencies, Martha decided to use her clustering algorithm. She uses data visualizations to share her findings with the board.
## Preprocessing The Data:
Given my knowledge of pandas, I preprocess the dataset to run PCA on Workoutcom2.Create a new DataFrame containing only cryptocurrency names and use the crypto_df DataFrame index as the index of this new DataFrame. Remove the CoinName column from the crypto_df dataframe as it is not used in the clustering algorithm.

Make sure i used crypto_d DataFrame looks like the image below.
```
# Load the crypto_data.csv dataset.
file = ...\crypto.csv'
df_crypto = pd.read_csv(file).set_index("Unnamed: 0")
df_crypto.index.name = None
df_crypto.head(10)
```
![image](https://user-images.githubusercontent.com/23088053/213334852-7bfd28f2-b06d-48aa-a8a7-c987bdf5f4fa.png)

## Reducing Data Dimensions Using PCA

Using our knowledge of the application of the PCA (Principal Component Analysis) algorithm, we reduce the dimensions of the X-DataFrame to three principal components and place these dimensions into a new DataFrame.
Using the information provided, we apply PCA to reduce the dimensionality to three main components.

![image](https://user-images.githubusercontent.com/23088053/213335255-a586fec4-a5f6-4c6a-a0c3-9d1b6c274d1e.png)

## Clustering Cryptocurrencies Using K-means

Using our knowledge of the K-means algorithm, we create an elbow curve using hvPlot to find the best value for K from the pcs_df dataframe created in Artifact 2. Then, run the K-means algorithm to predict K clusters of cryptocurrency data.

![image](https://user-images.githubusercontent.com/23088053/213335547-bdb0e062-f048-4cfd-be1f-926162dc0eef.png)

##Visualizing Cryptocurrencies Results

Using your knowledge of creating scatter plots with Plotly Express and hvplot, you’ll visualize the distinct groups that correspond to the three principal components i created in section 2, then i'll create a table with all the currently tradable cryptocurrencies using the hvplot.table() function.
## 3 PCA data on cluster graph
![newplot](https://user-images.githubusercontent.com/23088053/213335918-53791203-3acc-445b-862a-47e095b648a6.png)
## tradable cryptocurrencies cluster graph
![newplot (1)](https://user-images.githubusercontent.com/23088053/213335908-761f7d22-de52-4096-8618-d06780032e77.png)
## Hvplot.scatter using x="TotalCoinsMined" and y="TotalCoinSupply
![bokeh_plot (1)](https://user-images.githubusercontent.com/23088053/213335902-eedd7f30-5abd-49f2-abe7-c3a3633e568a.png)
