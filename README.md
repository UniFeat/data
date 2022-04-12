# Data in UniFeat format

A specific way of representing datasets is needed for the tool. In UniFeat format, the representation of the input dataset consists of the following parts:

- The first row of the datasets must have the names of all features. 
- The next rows contain all data, with each row corresponding to a sample. A vector of feature values describes each sample with a class label separated by commas. Also, the class labels of all samples must be available in the last column of the dataset.


You can easily import the dataset into the UniFeat tool as a file in comma-delimited format (i.e., CSV file format). This figure shows an example of a dataset in the UniFeat format. The input dataset contains 12 samples and four features within the class feature. In this case, the class feature has three values including: `Iris-setosa`, `Iris-versicolor`, and `Iris-virginica`.

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
