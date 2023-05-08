## Feature Engineering

TLDR; 
Feature engineering is like preparing ingredients for cooking. Just like how we need to clean, cut and chop vegetables before cooking, in machine learning, we need to clean and transform data to make it ready for use by the computer. This is important because the computer needs data to be in a certain format to be able to understand it and make predictions. By doing this, we can help the computer learn and make more accurate predictions.


Feature engineering is a crucial step in machine learning where you extract the relevant information from raw data and transform it into a format that can be used by machine learning algorithms. It involves selecting, extracting, and transforming the input features (i.e., the attributes or variables) in a dataset to make them suitable for use in a predictive model.

The goal of feature engineering is to create features that are informative, non-redundant, and relevant to the problem at hand. This process can involve a variety of techniques, such as scaling, normalization, binning, encoding, feature selection, and feature creation.

Scaling and normalization involve rescaling the values of input features to make them comparable and easier for the machine learning algorithm to process. Binning involves grouping continuous values into discrete categories, which can help simplify the input space and make it more interpretable. Encoding involves converting categorical variables into numerical values, which can be processed by machine learning algorithms.

Feature selection involves selecting a subset of relevant features from the input space, which can help improve the accuracy and interpretability of the model. Feature creation involves deriving new features from existing ones, such as computing ratios, differences, or combinations of features, which can provide additional information and improve the predictive performance of the model.

Overall, feature engineering is a critical step in the machine learning pipeline, as it can significantly impact the performance of a predictive model. The process requires both domain knowledge and creativity to extract meaningful insights from the data and transform them into informative features that can be used to make accurate predictions.


## Curse of dimensionality

tldr; The curse of dimensionality is like trying to find a needle in a haystack, but the haystack is getting bigger and bigger. In machine learning, this happens when we have too many different things (dimensions) to look at, and it becomes really hard to find patterns and make sense of all the information. We can try to make things simpler by choosing only the most important things to look at, or by using special tools to help us find what we need. (PCA)



The curse of dimensionality is a problem in machine learning where as the number of input features (i.e., dimensions) increases, the amount of data required to train a model effectively grows exponentially. This happens because as the number of dimensions increases, the volume of the input space also increases rapidly, and the available data becomes sparse, making it difficult for the machine learning algorithm to find patterns or relationships in the data.

To understand this, imagine that you are trying to find a specific book on a bookshelf with only one row of books. If you have 10 books, it's relatively easy to find the book you're looking for by scanning the titles. However, if you have 1000 books, it becomes much more difficult and time-consuming to find the book you need. The same concept applies to machine learning algorithms - as the number of input features increases, the amount of data required to accurately represent the input space also increases exponentially.

To overcome the curse of dimensionality, some techniques include feature selection, dimensionality reduction, and using algorithms that are designed to work with high-dimensional data. It's important to balance the complexity of the input features with the amount of data available, to avoid overfitting or underfitting the model.


## Mean Replacement - (meant only for columns!!)


Mean replacement is a technique used in machine learning to handle missing data. When we have a dataset with some missing values, we can replace those missing values with the average (or mean) value of that feature in the dataset.

For example, let's say we have a dataset that contains information about the height of different people, but some of the heights are missing. We can calculate the mean height of all the people in the dataset, and then replace the missing values with this mean height value.

Mean replacement is a simple and quick method to handle missing data, but it has some limitations. It assumes that the missing values are missing at random, and that the distribution of the data is roughly symmetric. It can also distort the overall distribution of the data and potentially impact the performance of the machine learning algorithm.

Overall, mean replacement is a useful technique for handling missing data when we have a large amount of missing values, but it's important to carefully consider the limitations and potential impact on the analysis.

tldr; Mean replacement is like guessing what the missing piece of a puzzle might be by looking at the other pieces around it. In machine learning, this is done when we have some missing information in our data, and we fill in the missing parts with the average of the information we do have. It's not a perfect solution, but it can help us make sense of the data we have when we don't have all the information we need.

Another alternate is dropping the missing rows. 

## Unbalanced Data

- Major discrepancy in data
Problem seen majorly in Neural Networks

How to deal with it?
Oversampling - duplicate samples from the minority class

Undersampling - Remove the negative ones