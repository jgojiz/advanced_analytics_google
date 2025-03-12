# EDA

**Dummy Variables**
Just 0 and 1 which indicate false (absence) or true (presence).

**Outliers**
When it comes to exploratory data analysis, or EDA, there are essentially three main ways to handle outliers: delete, reassign, or leave them in.
* Delete them: If you are sure the outliers are mistakes, typos, or errors and the dataset will be used for modeling or machine learning, then you are more likely to decide to delete outliers. Of the three choices, you’ll use this one the least. 
* Reassign them: If the dataset is small and/or the data will be used for modeling or machine learning, you are more likely to choose a path of deriving new values to replace the outlier values. 
* Leave them: For a dataset that you plan to do EDA/analysis on and nothing else, or for a dataset you are preparing for a model that is resistant to outliers, it is most likely that you are going to leave them in.

**Label encoding** 
You might want to encode categorical data to process inputs in the model faster. Transforming and joining numbers is much faster.

**Some potential problems with label encoding**
Imagine you’re analyzing a dataset with categories of music genres. You label encode “Blues,” “Electronic Dance Music (EDM),” “Hip Hop,” “Jazz,” “K-Pop,” “Metal,” “ and “Rock,” with the following numeric values, “1, 2, 3, 4, 5, 6, and 7.” 

With this label encoding, the resulting machine learning model could derive not only a ranking, but also a closer connection between Blues (1) and EDM (2) because of how close they are numerically than, say, Blues(1) and Jazz(4). In addition to these presumed relationships (which you may or may not want in your analysis) you should also notice that each code is equidistant from the other in the numeric sequence, as in 1 to 2 is the same distance as 5 to 6, etc. The question is, does that equidistant relationship accurately represent the relationships between the music genres in your dataset? To ask another question, after encoding, will the visualization or model you build treat the encoded labels as a ranking? 

The same could be said for the mushroom example above. After label encoding mushroom types, are you satisfied with the fact that the mushrooms are now in a presumed ranked order with button mushrooms ranked first and toadstool ranked eighth? 

In summary, label encoding may introduce unintended relationships between the categorical data in your dataset. When you are making decisions about label encoding, consider the algorithm you’ll apply to the data and how it may or may not impact label encoded categorical data.      

Fortunately, there is another method for categorical encoding that may help with these potential problems.

**Label encoding or one-hot encoding: How to decide?**
There is no simple answer to whether you should use label encoding or one-hot encoding. The decision needs to be made on a case-by-case, or dataset-by-dataset basis. But there are some guidelines to help you. 

Use label encoding when:

* There are a large number of different categorical variables — because label encoding uses far less data than one-hot encoding

* The categorical values have a particular order to them (for example, age groups can be grouped as youngest to oldest or oldest to youngest)

* You plan to use a decision tree or random forest machine learning model

Use one-hot encoding when: 

* There is a relatively small amount of categorical variables — because one-hot encoding uses much more data than label encoding. 

* The categorical variables have no particular order

* You use a machine learning model in combination with dimensionality reduction (like Principal Component Analysis (PCA))

**Heatmap**
Type of data visualization that depicts the magnitude of an instance or set of values based on two colors.

**Plotly Express package**
When you're working with hundreds of thousands of data points plotted on a map, it takes a lot of computing power. To make it a shorter runtime, we'll use the Plotly express package. The package is designed to keep runtimes as low as possible.