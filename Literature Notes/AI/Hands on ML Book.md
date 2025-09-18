# Ch - 1 

Supervised Learning

• k-Nearest Neighbors 
• Linear Regression 
• Logistic Regression 
• Support Vector Machines (SVMs)
• Decision Trees and Random Forests 
• Neural networks

Unsupervised Learning
• Clustering 
— k-Means
— Hierarchical Cluster Analysis (HCA) 
— Expectation Maximization 

• Visualization and dimensionality reduction 
— Principal Component Analysis (PCA)
— Kernel PCA — Locally-Linear Embedding (LLE)
— t-distributed Stochastic Neighbor Embedding (t-SNE) 

• Association rule learning 
— Apriori 
— Eclat



A related task is ==dimensionality reduction==, in which the goal is to ==*simplify the data without losing too much information*==. One way to do this is to merge several correla‐ ted features into one. For example, a car’s mileage may be very correlated with its age, so the dimensionality reduction algorithm will merge them into one feature that rep‐ resents the car’s wear and tear. This is called feature extraction.

Features = mileage,age

(2 features) mileage + age = wear n tear (1 feature)


Instance based vs Model based ML
Instance = K nearest neighbour etc 
Model = Linear regression etc

 Performance measure
 utility function (or fitness function)  =   how good your model 
 cost function  =  how bad it is.

Main Challenges of Machine Learning  ==  “bad algorithm” and “bad data.”

the trade-off between spending time and money on 
algorithm development vs corpus development.”

By using a non representative training set(the dataset doesn't properly align with the reality of the whole data), we trained a model that is unlikely to make
accurate predictions, especially for very poor and very rich countries.


Sampling Bias
It is crucial to use a training set that is representative of the cases you want to general‐
ize to. This is often harder than it sounds: if the sample is too small, you will have
sampling noise (i.e., nonrepresentative data as a result of chance), but even very large
samples can be nonrepresentative if the sampling method is flawed. 

Eg: of Sampling bias
Nonresponse bias = Bias due to improper response

A company conducted large poll on  winning of Landon vs Roosvelt and out 10million, 2.5 million replied n they predicted that Landon would win with 57% of votes but in return Roosvelt won with 62% votes

Reason: data is collected through mobile phones, magzines n mails which only rich can afford and hence THey selected Landon


Poor-Quality Data

training data is full of errors, outliers, and noise (e.g., due to poor-
quality measurements), =  Harder for the system to detect the underlying
patterns

 most data scientists spend
a significant part of their time doing just that.

1)  If some instances are clearly outliers, it may help to simply discard them or try to
fix the errors manually.

2)  If some instances are missing a few features (e.g., 5% of your customers did not
specify their age), you must decide whether you want to ignore this attribute alto‐
gether, ignore these instances, fill in the missing values (e.g., with the median
age), or train one model with the feature and one model without it, and so on.

Irrelevant Features
As the saying goes: garbage in, garbage out. Your system will only be capable of learning if the training data contains enough relevant features and not too many irrelevant ones

Feature engineering,

1) Feature selection: selecting the most useful features to train on among existing
features.
2)  Feature extraction: combining existing features to produce a more useful one (as we saw earlier, dimensionality reduction algorithms can help).
3) Creating new features by gathering new data.


Overfitting of TRaining DAta
In foreign country taxi driver robbed you, u feel all drivers are the robbers
Same case happens with machines, tis is know as overfitting

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250728113437.png)
Complex models such as deep neural networks can detect subtle patterns in the data,
but if the training set is noisy, or if it is too small (which introduces sampling noise),
then the model is likely to detect patterns in the noise itself. Obviously these patterns
will not generalize to new instances.


Overfitting happens when the model is too complex relative to the
amount and noisiness of the training data

1) To simplify the model by selecting one with fewer parameters
(e.g., a linear model rather than a high-degree polynomial
model), by reducing the number of attributes in the training
data or by constraining the model

2) To gather more training data
3) To reduce the noise in the training data (e.g., fix data errors
and remove outliers)


Regularization
Constraining a model to make it simpler and reduce the risk of overfitting 

A very simple model indeed! If we allow the algorithm to modify θ1 but we force it to keep it small, then the learning algorithm will effectively have somewhere in between one and two degrees of freedom

Find the right balance between fitting the data perfectly and keeping the model simple
enough to ensure that it will generalize well.


The amount of regularization to apply during learning can be controlled by a hyperparameter. A hyperparameter is a parameter of a learning algorithm (not of the model)

 As such, it is not affected by the learning algorithm itself; it must be set prior to training and remains constant during training

If you set the regularisation hyper-parameter to a very large value, you will get an almost flat model (a slope close to zero); the learning algorithm will almost certainly not overfit the training data, but it will be less likely to find a good solution. Tuning hyper-parameters is an important part of building a Machine Learning system

A common solution to this problem is to have a second holdout set called the valida‐
tion set. You train multiple models with various hyperparameters using the training
set, you select the model and hyperparameters that perform best on the validation set,
and when you’re happy with your model you run a single final test against the test set
to get an estimate of the generalization error.

NO FREE LUNCH THEOREM

For any dataset we cant say directly that some X model or  algorithm works best. NO FREE MODEL. We need to go under trail and error to find the best one.




1. How would you define Machine Learning?
	Machine learning is the science in which we program machine(computer) such a way that it learns pattern and rules from data on its own.
	
	Machine Learning is about building systems that can learn from data. Learning
	means getting better at some task, given some performance measure.

2. Can you name four types of problems where it shines?
	1) Item vs Consumption rate in hostel
	2) Finding ulcer region from image dataset
	3) Books genre vs Age group vs Gender
	4) Instagram categorizing content which user likes 

	 Machine Learning is great for complex problems for which we have no algorith‐
	mic solution, to replace long lists of hand-tuned rules, to build systems that adapt
	to fluctuating environments, and finally to help humans learn (e.g., data mining).
	
3. What is a labeled training set?
	It comes under supervised learning, data is labelled so that machine can learn from labels, 
	A labeled training set is a training set that contains the desired solution (a.k.a. a
	label) for each instance.
	
4. What are the two most common supervised tasks?
	1. The two most common supervised tasks are regression and classification.
	2) Classification of emails based on spam n ham
	3) FInding price of car based on predictors(mileage, brand, age) and labels of previous car prices
	Student learning with teacher guidance
	• k-Nearest Neighbors
	• Linear Regression
	• Logistic Regression
	• Support Vector Machines (SVMs)
	• Decision Trees and Random Forests
	• Neural networks
5. Can you name four common unsupervised tasks?
	Common unsupervised tasks include clustering, visualization, dimensionality
	reduction, and association rule learning.
	Student learning without teacher guidance
	• Clustering
		— k-Means
		— Hierarchical Cluster Analysis (HCA)
		— Expectation Maximization
	• Visualization and dimensionality reduction
		— Principal Component Analysis (PCA)
		— Kernel PCA
		— Locally-Linear Embedding (LLE)
		— t-distributed Stochastic Neighbor Embedding (t-SNE)
	• Association rule learning
		— Apriori
		— Eclat
	2) Pooling of people of diff groups based on interests (some qualities)
6. What type of Machine Learning algorithm would you use to allow a robot to
walk in various unknown terrains?
	Reinforcement Learning is likely to perform best if we want a robot to learn to
	walk in various unknown terrains since this is typically the type of problem that
	Reinforcement Learning tackles. It might be possible to express the problem as a
	supervised or semisupervised learning problem, but it would be less natural.
	
	KNN
7. What type of algorithm would you use to segment your customers into multiple
groups?
	If you don’t know how to define the groups, then you can use a clustering algo‐
	rithm (unsupervised learning) to segment your customers into clusters of similar
	customers. 
	
	However, if you know what groups you would like to have, then you can feed many examples of each group to a classification algorithm (supervised
	learning), and it will classify all your customers into these groups.
	CLusterning
8. Would you frame the problem of spam detection as a supervised learning problem or an unsupervised learning problem?
	SL  the algorithm is fed many emails along with their label (spam or not spam).
	
9. What is an online learning system?
	Data learns incrementally as it gets exposed to data during performance
	An online learning system can learn incrementally, as opposed to a batch learning system. This makes it capable of adapting rapidly to both changing data and autonomous systems, and of training on very large quantities of data.
	
10. What is out-of-core learning?
	Out-of-core algorithms can handle vast quantities of data that cannot fit in a computer’s main memory. An out-of-core learning algorithm chops the data into mini-batches and uses online learning techniques to learn from these mini-
batches.
11. What type of learning algorithm relies on a similarity measure to make predic‐
tions?
	KNN
	An instance-based learning system learns the training data by heart; then, when given a new instance, it uses a similarity measure to find the most similar learned instances and uses them to make predictions.
	
12. What is the difference between a model parameter and a learning algorithm’s
hyper-parameter?
	Model parameters(weights and bias) gets fitted during training, hyper-parameters are predefined
	A model has one or more model parameters that determine what it will predict given a new instance (e.g., the slope of a linear model). A learning algorithm tries to find optimal values for these parameters such that the model generalizes well to new instances. A hyperparameter is a parameter of the learning algorithm itself, not of the model (e.g., the amount of regularization to apply).
	
13. What do model-based learning algorithms search for? What is the most common
strategy they use to succeed? How do they make predictions?
	Model based learning algorithm try to fit the mathemaical function like linear, polynomial, complex etc using loss function.
	Finding right weighgts and bias based on the loss function
	they make predictions based on the function founds during training
	
	Model-based learning algorithms search for an optimal value for the model parameters such that the model will generalize well to new instances. We usually train such systems by minimizing a cost function that measures how bad the sys‐ tem is at making predictions on the training data, plus a penalty for model com‐ plexity if the model is regularized. To make predictions, we feed the new instance’s features into the model’s prediction function, using the parameter val‐ ues found by the learning algorithm.
	
14. Can you name four of the main challenges in Machine Learning?
	No free lunch theorem
	it depends on the quality of dataset
	Underfitting and overfitting
	TIme taking to train and parameters
	Some of the main challenges in Machine Learning are the lack of data, poor data
	quality, nonrepresentative data, uninformative features, excessively simple mod‐
	els that underfit the training data, and excessively complex models that overfit
	the data.
	
15. If your model performs great on the training data but generalizes poorly to new
instances, what is happening? Can you name three possible solutions?
	may be underfitting or overfitting or poor dataset quality
	if overfitting = Reduce model complexity
	underfitting = Increase model complexity
	data quality = Try to collect dataset with good featires
16. What is a test set and why would you want to use it?
	Test set is used to see how well is our model generalized for unknown dataset and to set hyper-parameters based on test results
	A test set is used to estimate the generalization error that a model will make on
	new instances, before the model is launched in production.
17. What is the purpose of a validation set?
	Validation set comes in need when we are working with multiple models and want to compare which model performs better,  we use train to train each model and  properly adjust hyper-parameters and validation to check performance of model on unknown dataset to determine if its overfitting or underfitting by comparing training and validation accuracies and finally after model training is done, we test on test set
	A validation set is used to compare models. It makes it possible to select the best
	model and tune the hyperparameters.
18. What can go wrong if you tune hyperparameters using the test set?
	Wecan get good results on that test by finding best parameters  set but we cant be sure if it will give same results during real time
	If you tune hyperparameters using the test set, you risk overfitting the test set,
	and the generalization error you measure will be optimistic (you may launch a
	model that performs worse than you expect).
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250731135611.png)
19. What is cross-validation and why would you prefer it to a validation set?
	To avoid “wasting” too much training data in validation sets, a common technique is
	to use cross-validation: the training set is split into complementary subsets, and each
	model is trained against a different combination of these subsets and validated
	against the remaining parts. Once the model type and hyperparameters have been
	selected, a final model is trained using these hyperparameters on the full training set,
	and the generalized error is measured on the test set.
	Cross-validation is a technique that makes it possible to compare models (for
	model selection and hyperparameter tuning) without the need for a separate vali‐
	dation set. This saves precious training data.

---
# Ch - 2

Exercises
Using this chapter’s housing dataset:

1. Try a Support Vector Machine regressor (sklearn.svm.SVR), with various hyper  parameters such as kernel="linear" (with various values for the C hyperpara‐ meter) or kernel="rbf" (with various values for the C and gamma hyperparameters). Don’t worry about what these hyperparameters mean for now. How does the best SVR predictor perform?

2. Try replacing GridSearchCV with RandomizedSearchCV.

3. Try adding a transformer in the preparation pipeline to select only the mostimportant attributes.

4. Try creating a single pipeline that does the full data preparation plus the final prediction.
5. Automatically explore some preparation options using GridSearchCV.