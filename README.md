# machine-learning-python
deprived from Introduction to Machine Learning with Python A Guide for Data Scientists by Andreas C. Müller, Sarah Guido Book
<h1>Meet the data</h1>
<h3>Iris object contains keys and values iris_dataset.keys()</h3>
dict_keys(['data', 'target', 'frame', 'target_names', 'DESCR', 'feature_names', 'filename'])<br>
<h3>Value of the key DESCR is a short description of the dataset iris_dataset['DESCR'][:193]</h3>
.. _iris_dataset: Iris plants dataset -------------------- **Data Set Characteristics:** :Number of Instances: 150 (50 in each of three classes) :Number of Attributes: 4 numeric, pre ...<br>
<h3>Value of the key target_names is an array of strings, containing the species of
flower that we want to predict iris_dataset['target_names']</h3>
['setosa' 'versicolor' 'virginica']<br>
<h3>Data itself is contained in the target and data fields. data contains the numeric
measurements of sepal length, sepal width, petal length, and petal width in a NumPy
array iris_dataset['feature_names']</h3>
['sepal length (cm)', 'sepal width (cm)', 'petal length (cm)', 'petal width (cm)']<br>
<h3>We see that the array contains measurements for 150 different flowers. Remember
that the individual items are called samples in machine learning, and their properties
are called features. The shape of the data array is the number of samples multiplied by
the number of features iris_dataset['data'].shape</h3>
(150, 4)<br>
<h3>We can see that all of the first five flowers have a petal width of 0.2 cm
and that the first flower has the longest sepal, at 5.1 cm iris_dataset['data'][:5]</h3>
[[5.1 3.5 1.4 0.2] [4.9 3. 1.4 0.2] [4.7 3.2 1.3 0.2] [4.6 3.1 1.5 0.2] [5. 3.6 1.4 0.2]]<br>
