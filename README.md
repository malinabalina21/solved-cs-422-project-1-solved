Download Link: https://assignmentchef.com/product/solved-cs-422-project-1-solved
<br>
<strong>Logistics: </strong>You must implement everything stated in this project description that is marked with an <strong>implement </strong>tag. Whenever you see the <strong>write-up </strong>tag, that is something that must be addressed in the project README.txt. Graduate students are required to implement everything including items tagged with <strong>622</strong>. Students in 422 do not need to complete these extra elements. <strong>You cannot import any packages unless specifically noted by the instructor. </strong>In this project, you may import the numpy, math (for log), scipy.spatial (for euclidean distance) and random.randint (for random integer generation) packages. You are welcome to ask about particular packages as they come up. The idea is to implement everything from scratch.




<h1>1        Decision Trees</h1>

<h2>File name: decision trees.py</h2>

<strong>Implement </strong>a function in python:

DT_train_binary(X,Y,max_depth)

that takes training data as input. The labels and the features are binary, but the feature vectors can be of any finite dimension. The training feature data (X) should be structured as a 2D numpy array, with each row corresponding to a single sample. The training labels (Y) should be structured as a 1D numpy array, with each element corresponding to a single label. Y should have the same number of elements as X has rows. max depth is an integer that indicates the maximum depth for the resulting decision tree. DT train binary(X,Y,max depth) should return the decision tree generated using information gain, limited by some given maximum depth. If max depth is set to -1 then learning only stops when we run out of features or our information gain is 0. You may store a decision tree however you would like, i.e. a list of lists, a class, a dictionary, etc. <strong>Write-Up</strong>: describe your implementation concisely. Bulleted lists are okay!

Binary data for testing can be found in in data 1.txt and data 2.txt.

<strong>Implement </strong>a function in python:

DT_test_binary(X,Y,DT)

that takes test data X and test labels Y and a learned decision tree model DT, and returns the accuracy (from 0 to 1) on the test data using the decision tree for predictions. <strong>Write-Up</strong>: describe your implementation concisely.

1

<strong>Implement </strong>the following function in python:

DT_make_prediction(x,DT)

This function should take a single sample and a trained decision tree and return a single classification. The output should be a scalar value. <strong>Write-Up</strong>: describe your implementation concisely.

<strong>622 </strong><strong>Implement </strong>the following functions in python:

DT_train_real(X,Y,max_depth)

DT_test_real(X,Y,DT)

These functions are defined similarly to those above except that the features are now real values. The labels are still binary. Your decision tree will need to use questions with inequalities: <em>&gt;</em>, ≥, <em>&lt;</em>, ≤. <strong>Write-Up</strong>: describe your implementation concisely. Real-valued data for testing is provided in data 3.txt

<h1>2        Nearest Neighbors</h1>

<h2>File name: nearest neighbors.py</h2>

<strong>Implement </strong>a function in python:

KNN_test(X_train,Y_train,X_test,Y_test,K)

that takes training data, test data, and K as inputs. KNN test(X train,Y train,X test,Y test,K) should return the accuracy on the test data. The training data and test data should have the same format as described earlier for the decision tree problems. Your function should be able to handle any dimension feature vector, with real-valued features. Remember your labels are binary, and they should be −1 for the negative class and 1 for the positive class. data 4.txt has some test data for your KNN algorithm. Try <em>K </em>= 1, <em>K </em>= 3, and <em>K </em>= 5. <strong>Write-Up</strong>: describe your implementation concisely.

<strong>622 </strong><strong>Implement </strong>the following function in python:

choose_K(X_train,Y_train,X_val,Y_val)

that takes training data and validation data as inputs and returns a K value. This function must iterate through all possible K values and choose the best K for the given training data and validation data. K must be chosen in order to achieve the best accuracy on the validation data. <strong>Write-Up</strong>: describe your implementation concisely.

<h1>3        Clustering</h1>

<h2>File name: clustering.py</h2>

<strong>Implement </strong>a function in python:

K_Means(X,K,mu)

that takes feature vectors X and a K value as input and returns a numpy array of cluster centers C. Your function should be able to handle any dimension of feature vectors and any <em>K&gt; </em>0. mu is an array of initial cluster centers, with either K or 0 rows. If mu is empty, then you must initialize the cluster centers randomly. Otherwise, start with the given cluster centers. <strong>Write-Up</strong>: describe your implementation concisely. data 5.txt and data 6.txt have some sample data for you to test out your implementation.

<strong>622 </strong><strong>Implement </strong>the following function in python:

K_Means_better(X,K)

that takes feature vectors X and a K value as input and returns a numpy array of cluster centers C. Your function should be able to handle any dimension of feature vectors and any <em>K&gt; </em>0. Your function will run the above-implemented K Means(X,K,[]) function <strong>many </strong>times until the same set of cluster centers are returned a majority of the time. At this point, you will know that those cluster centers are likely the best ones. K Means better(X,K) will return those cluster centers. <strong>Write-Up</strong>: describe your implementation concisely.

2