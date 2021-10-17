# Cryptocurrencies-Unsupervised Machine Learning by Kieran Persaud

## Overview of the Challenge
Martha is a senior manager for the Advisory Services Team at Accountability Accounting. Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. They've asked for a report to be created that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system.

Unsupervised machine learning is useful for this purpose, since we don't know the output and since we want to create a classification system. In the challenge, I will first pre-process the data to fit the machine learning models using PCA. I will employ KMeans to cluster the cryptocurrencies, and then create visualizations using ```plotly.express``` and ```hvplot``` that can easily depict the different groups.

## Resources
- Data Source: crypto_data.csv
- Software: Anaconda 4.10.1, kernels mlenv, plotly.express, hvplot, PCA and KMeans libraries; Jupyter Notebook

## Results
After pre-processing the data from the csv file, I determined that there are 532 tradable cryptocurrencies.

### Elbow Curve
![image](https://user-images.githubusercontent.com/84286467/137637637-1bb142eb-7cef-47a9-aa1b-8ef72a05dafb.png)

The elbow curve shows that inertia significantly drops up to k=4, after which there are diminishing drops for each subsequent k value. I use k=4 to create 4 classes in which to categorize the data into the following DataFrame.

![image](https://user-images.githubusercontent.com/84286467/137637832-1c5c4b66-2053-4881-8e47-75c0461542be.png)

### 3D Scatter with Clusters
![image](https://user-images.githubusercontent.com/84286467/137637891-1ac65933-6e79-4ca7-9141-2eb5e2603375.png)

This is a 3D visualization of the above DataFrame.

### Tradable Crypto Table
![image](https://user-images.githubusercontent.com/84286467/137638275-54dc661f-12e3-48be-b6b9-d75019e5ec52.png)

Using hvplot, this interactive table can be created and used to further visualize the cryptocurrencies and classes. I sorted the classes in ascending order, and saw that there is only one cryptocurrency in class 3, which is BitTorrent.

### ScatterPlot of the Total Coins Mined v Total Supply
![image](https://user-images.githubusercontent.com/84286467/137638058-9d328e97-7748-4d1c-a436-ad8471ad7e75.png)

This scatterplot compares the Total Coins Mined versus the Total Supply. Most of the data is aggregated around the x and y axis intersection with some outliers, implying there are many cryptocurrencies with low mining and low supply.
