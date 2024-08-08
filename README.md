# Incremental Learning

Incremental learning, also known as online learning or sequential learning, is a machine learning approach where the model learns from data in a continuous, iterative manner rather than all at once. 
This approach is particularly useful when dealing with large datasets, real-time data streams, or situations where the entire dataset is not available upfront.

* Here, in this example we have a dataset of 16Gb (55m+ rows) and my laptop has 8gb RAM. Clearly, my laptop is not capable of loading and training the entire dataset at once.
* Here we will use the concept of Incremental Learning

I have approached this problem in 3 ways - 
1. Dask Library + Incremental Learning (Random Forest)
2. Pandas Library + Incremental Learning (Random Forest)
3. River Library + Incremental Learning (Random Forest)


## Dask 

Dask is a flexible parallel computing library in Python designed to handle large-scale data processing and computation.
It enables you to scale your computations from a single machine to a cluster of machines while providing a familiar interface for users of libraries like NumPy, Pandas, and Scikit-Learn.

## Pandas

The chunksize attribute in Pandas allows you to efficiently handle large datasets that don't fit into memory by reading the data in smaller, manageable chunks. 
This approach is particularly useful for performing operations on large CSV files or other text-based data sources.
