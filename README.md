 <div align="center" width="100px"> 
     <a href="https://unifeat.github.io/"><img src="https://raw.githubusercontent.com/UniFeat/UniFeat.github.io/main/images/logo.png" alt="logo" width="25%" /></a>
     <p font-size="300px"><b>Universal Feature Selection Tool</b></p> 
     <p font-size="100px"><b>Datasets Repositories</b></p> 
 </div>
 
 ----
[![GitHub stars](https://img.shields.io/github/stars/UniFeat/data)](https://github.com/UniFeat/data/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/UniFeat/data)](https://github.com/UniFeat/data/network)
[![GitHub license](https://img.shields.io/github/license/UniFeat/data)](https://github.com/UniFeat/data/blob/main/LICENSE)

# Data in UniFeat format

Since UniFeat supports a specific format for the datasets, a list of converted datasets to UniFeat format has been provided in this repository. The representation of the input dataset consists of the following parts:

- The first row of the datasets must have the names of all features. 
- The next rows contain all data, with each row corresponding to a sample. A vector of feature values describes each sample with a class label separated by commas. Also, the class labels of all samples must be available in the last column of the dataset.


You can easily import the dataset into the UniFeat tool as a file in comma-delimited format (i.e., CSV file format). The following figure shows an example of a dataset in the UniFeat format. The input dataset contains 12 samples and four features within the class feature. In this case, the class feature has three values including: `Iris-setosa`, `Iris-versicolor`, and `Iris-virginica`.

```
sepal length,  sepal width,  petal length,  petal width,  class
4.3,           3,            1.1,           0.1,          Iris-setosa
4.4,           2.9,          1.4,           0.2,          Iris-setosa
4.4,           3,            1.3,           0.2,          Iris-setosa
4.4,           3.2,          1.3,           0.2,          Iris-setosa
5.5,           2.3,          4,             1.3,          Iris-versicolor
5.5,           2.4,          3.8,           1.1,          Iris-versicolor
5.5,           2.4,          3.7,           1,            Iris-versicolor
5.5,           2.5,          4,             1.3,          Iris-versicolor
6.3,           3.3,          6,             2.5,          Iris-virginica
6.3,           2.9,          5.6,           1.8,          Iris-virginica
6.3,           2.7,          4.9,           1.8,          Iris-virginica
6.3,           2.8,          5.1,           1.5,          Iris-virginica
```

In addition to the dataset files, a separate file that contains the values of the class feature must be imported into the tool. Each value of the class feature is presented in a row. For example, for the dataset in the above figure, the class label file contains three rows each of which represents a class label including: `Iris-setosa`, `Iris-versicolor`, and `Iris-virginica`. It should be noted that rows of the class label file must be compatible with the class feature values in the dataset file.

## Dataset files
Generally speaking, benchmark datasets provided for the feature selection domain are available in two types. In the first type, the dataset file consists of all the samples. In the second type, the datasets are divided originally into two portions: training and test sets. UniFeat supports both kinds of dataset files.

## Missing values in original datasets
Some of the original datasets have several missing values in the features. To resolve this challenge, the missing values have been completed using the mean of the available data of the respective feature. Therefore, current datasets in this repository do not contain missing values.
