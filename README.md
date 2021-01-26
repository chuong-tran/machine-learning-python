# machine-learning-python
deprived from Introduction to Machine Learning with Python A Guide for Data Scientists by Andreas C. Müller, Sarah Guido Book
<h1>Meet the data</h1>
<h3>Iris object contains keys and values iris_dataset.keys()</h3>
{{keys}}<br>
<h3>Value of the key DESCR is a short description of the dataset iris_dataset['DESCR'][:193]</h3>
{{DESCR}}<br>
<h3>Value of the key target_names is an array of strings, containing the species of
flower that we want to predict iris_dataset['target_names']</h3>
{{target_names}}<br>
<h3>Data itself is contained in the target and data fields. data contains the numeric
measurements of sepal length, sepal width, petal length, and petal width in a NumPy
array iris_dataset['feature_names']</h3>
{{feature_names}}<br>
<h3>We see that the array contains measurements for 150 different flowers. Remember
that the individual items are called samples in machine learning, and their properties
are called features. The shape of the data array is the number of samples multiplied by
the number of features iris_dataset['data'].shape</h3>
{{shape}}<br>
<h3>We can see that all of the first five flowers have a petal width of 0.2 cm
and that the first flower has the longest sepal, at 5.1 cm iris_dataset['data'][:5]</h3>
{{columns}}<br>
