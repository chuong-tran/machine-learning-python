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
<h1>Measuring Success: Training and testing data</h1>
<p>To assess the model’s performance, we show it new data (data that it hasn’t seen
before) for which we have labels. This is usually done by splitting the labeled data we
have collected (here, our 150 flower measurements) into two parts. One part of the
    data is used to <strong>build our machine learning model</strong>, and is called the training data or
training set. The rest of the data will <strong>be used to assess</strong> how well the model works; this
is called the test data, test set, or hold-out set.</p>
<p>-<strong>scikit-learn</strong>,  contains a function that shuffles/xáo trộn the dataset and splits it for you: <strong>the
    train_test_split function</strong></p>
<p>-This function <strong>extracts 75%</strong> of the rows in the data as the
    <strong>training set</strong>, together with the corresponding labels for this data. The <strong>remaining 25%
    </strong>of the data, together with the remaining labels, is declared as the <strong>test set</strong>.</p>
<p>-We use a capital X because the data is a <strong>two-dimensional array</strong> (a
matrix) and a lowercase y because the target is a <strong>one-dimensional array</strong> (a vector).</p>
<p style="color:blue"><strong>from sklearn.model_selection import train_test_split</strong></p>
<p style="color:blue"><strong>X_train, X_test, y_train, y_test = train_test_split(iris_dataset['data'], iris_dataset['target'], random_state=0)</strong></p>
<p>-To make sure that we will get the same output if we run the same function several
times, we provide the pseudorandom number generator with a fixed seed using the
    <strong>random_state</strong> parameter</p>
<p>- X_train contains 75% of the rows of the dataset,
and X_test contains the remaining 25%</p>
<p><strong>X_train.shape : </strong>(112, 4) <strong>y_train.shape : </strong>(112,) <strong>X_test.shape : </strong>(38, 4) <strong>y_test.shape : </strong>(38,)</p>
<h1>First Things First: Look at Your Data</h1>
<p>One of the best ways to inspect data is to visualize it. One way to do this is by using a
scatter plot</p>
<p>The data points are colored
according to the species the iris belongs to. To create the plot, we first convert the
    <strong>NumPy</strong> array into a <strong>pandas DataFrame</strong>. pandas has a function to create pair plots
called <strong>scatter_matrix</strong>.</p>
<p style="color:blue"><strong>from pandas.plotting import scatter_matrix</strong></p>
<p style="color:blue"><strong>iris_dataframe = pd.DataFrame(X_train, columns=iris_dataset.feature_names)</strong></p>
<p style="color:blue"><strong>grr = pd.plotting.scatter_matrix(iris_dataframe, c=y_train, figsize=(15, 15), marker='o',
 hist_kwds={'bins': 20}, s=60, alpha=.8, cmap=mglearn.cm3)</strong></p>
<p style="color:blue"><strong>from matplotlib import pyplot</strong></p>
<p style="color:blue"><strong>pyplot.show()</strong></p>
![look_at_your_data](main/look_at_your_data.jpg)
