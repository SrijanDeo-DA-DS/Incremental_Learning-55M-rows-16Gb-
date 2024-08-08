# Incremental Learning

Incremental learning, also known as __online learning or sequential learning__, is a machine learning approach where the model learns from data in a continuous, iterative manner rather than all at once. 
This approach is particularly useful when dealing with __large datasets, real-time data streams__, or situations where the entire dataset is not available upfront.

* Here, in this example we have a dataset of __16Gb (55m+ rows)__ and my laptop has 8Gb RAM. Clearly, my laptop is not capable of loading and training the entire dataset at once.
* Here we will use the concept of Incremental Learning

I have approached this problem in 3 ways - 
1. Dask Library + Incremental Learning (Random Forest)
2. Pandas Library + Incremental Learning (Random Forest)
3. River Library + Incremental Learning (Random Forest)

- Random Forest / XgBoost have __'warm_start'__ parameter that helps us perform incremental training
- Other algorithms like SGDClassifier have __'partial_fit'__ that helps us perform incremental training

## Dask 
Dask is a flexible parallel computing library in Python designed to handle large-scale data processing and computation.
It enables you to scale your computations from a single machine to a cluster of machines while providing a familiar interface for users of libraries like NumPy, Pandas, and Scikit-Learn.

#### Classification Report and Training Time
![dask_performance](https://github.com/user-attachments/assets/f73c4373-86b2-431f-809e-c7bde3c6e53a)

* It took approx. __38mins to train a 15Gb dataset__ using Dask

## Pandas

The chunksize attribute in Pandas allows you to efficiently handle large datasets that don't fit into memory by reading the data in smaller, manageable chunks. 
This approach is particularly useful for performing operations on large CSV files or other text-based data sources.

## River
The River library is a Python library designed for incremental learning, which allows you to build and train machine learning models in a way that is suitable for streaming data or large datasets. It is particularly useful when dealing with continuous data streams or when you need to update your model incrementally without retraining it from scratch.
