Download Link: https://assignmentchef.com/product/solved-comp551-project1-linear-classification-techniques
<br>
<h1></h1>

In this miniproject you will implement two linear classification techniques—logistic regression and linear discriminant analysis (LDA)—and run these two algorithms on two distinct datasets. These two algorithms are discussed in Lectures 4 and 5, respectively. The goal is to gain experience implementing these algorithms from scratch and to get hands-on experience comparing their performance.

<h1>Task 1: Acquire, preprocess, and analyze the data</h1>

Your first task is to acquire the data, analyze it, and clean it (if necessary). We will use two datasets in this project, outlined below.

<ul>

 <li>Dataset 1 (Wine Quality):

  <ul>

   <li>Link:https://archive.ics.uci.edu/ml/datasets/Wine+Quality</li>

   <li>This is a dataset where the goal is to predict the quality of wine based on its chemical properties.</li>

   <li><em>Note: We will only be using the </em>red wine <em>subset of the data.</em></li>

   <li><em>Note: This data contains quality ratings from 0-10. We will convert this task to a binary classification by defining the ratings of </em>{<em>6,7,8,9,10</em>} <em>as positive (i.e., 1) and all other ratings as negative (i.e., 0).</em></li>

  </ul></li>

 <li>Dataset 2 (Breast Cancer Diagnosis):

  <ul>

   <li>Link:https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)</li>

   <li>This is a dataset where the goal is to predict whether a tumour is malignant or benign based on various properties.</li>

   <li><em>Note: We will use the data folder titles </em>breast-cancer-wisconsin.data <em>for this project.</em></li>

  </ul></li>

</ul>

The essential subtasks for this part of the project are:

<ol>

 <li>Download the datasets (noting the correct subsets to use, as discussed above).</li>

 <li>Load the datasets into numpy objects (i.e., arrays or matrices) in Python. Remember to convert the wine datasetto a binary task, as discussed above.</li>

 <li>Clean the data. Are there any missing or malformed features? Are there are other data oddities that need to bedealt with? You should remove any examples with missing or malformed features and note this in your report.</li>

 <li>Compute some statistics on the data. E.g., what are the distributions of the positive vs. negative classes, whatare the distributions of some of the numerical features?</li>

</ol>

<h1>Task 2: Implement the models</h1>

Now you will implement the logistic regression and LDA models. You are free to implement these models as you see fit, but you should follow the equations that are presented in the lecture slides, and you must implement the models from scratch (i.e., you cannot use SciKit Learn or any other pre-existing implementations of these methods).

In particular, your two main tasks in the part are to:

<ol>

 <li>Implement logistic regression using gradient descent, as discussed in Lecture 4.</li>

 <li>Implement linear discriminant analysis using the equations from Lecture 5.</li>

</ol>

You are free to implement these models in any way you want, but you must use Python and you must implement the models from scratch (i.e., you cannot use SciKit Learn or similar libraries). Using the numpy package, however, is allowed and encouraged. Regarding the implementation, we recommend the following approach (but again, you are free to do what you want):

<ul>

 <li>Implement both the logistic regression and LDA models as Python classes. You should use the constructor for the class to initialize the model parameters as attributues, as well as to define other important properties of the model.</li>

 <li>Each of your models classes should have (at least) two functions:

  <ul>

   <li>Define a fit function, which takes the training data (i.e., <strong>X </strong>and <strong>y</strong>)—as well as other hyperparameters (e.g., the learning rate and/or number of gradient descent iterations)—as input. This function should train your model by modifying the model parameters.</li>

   <li>Define a predict function, which takes a set of input points (i.e., <strong>X</strong>) as input and outputs predictions (i.e., <strong>y</strong>ˆ) for these points. <em>Note that you need to convert probabilities to binary 0-1 predictions by thresholding the output at 0.5!</em></li>

  </ul></li>

 <li>In addition to the model classes, you should also define a functions evaluate_acc to evaluate the model accuracy. This function should take the true labels (i.e., <strong>y</strong>), and target labels (i.e., <strong>y</strong>ˆ) as input, and it should output the accuracy score.</li>

 <li>Lastly, you should implement a script to run k-fold cross validation.</li>

</ul>

<h1>Task 3: Run experiments</h1>

The goal of this project is to have you explore linear classification and compare different features and models. <em>You will use 5-fold cross validation to estimate performance in all of the experiments, and you should evaluate performance using accuracy (i.e., proportion of predictions that are correct). </em>You are welcome to perform any experiments and analyses you see fit (e.g., to compare different features), but at a minimum you must complete the following experiments in the order stated below:

<ol>

 <li>Test different learning rates for logistic regression.</li>

 <li>Compare the runtime and accuracy of LDA and logistic regression on both datasets.</li>

 <li>For the wine dataset, find a new subset of features and/or additional features that improve the accuracy. Werecommend that you use logistic regression for this exploration. <em>Hint: Try exploring different interaction terms.</em></li>

</ol>

Note: The above experiments are the minimum requirements that you must complete; however, this project is open-ended. A project that <em>perfectly </em>meets the minimum requirements would get an A- grade, but to get an A grade you must go above and beyond the minimum requirements. For example, you might investigate different stopping criteria for the gradient descent in logistic regression, analyze the performance trade-offs of different implementation approaches for linear discriminant analysis, or develop an automated approach to select a good subset of features. You do not need to do all of these things, but you should demonstrate creativity, rigour, and an understanding of the course material in how you run your chosen experiments and how you report on them in your write-up. Deliverables

You must submit two separate files to MyCourses (using the exact filenames and file types outlined below):

<ol>

 <li>zip: Your data processing and linear regression code (as some combination of .py and .ipynb files).</li>

 <li>pdf: Your (max 5-page) project write-up as a pdf (details below).</li>

</ol>

<h2>Project write-up</h2>

Your team must submit a project write-up that is a maximum of five pages (single-spaced, 11pt font or larger; minimum 0.5 inch margins, an extra page for references/bibliographical content can be used). We highly recommend that students use LaTeX to complete their write-ups. This first mini-project report has relatively strict requirements, but as the course progresses your project write-ups will become more and more open-ended. You have some flexibility in how you report your results, but you must adhere to the following structure and minimum requirements:

Abstract (100-250 words) Summarize the project task and your most important findings. For example, include sentences like “In this project we investigated the performance of linear classification models on two benchmark datasets”, “We found that the logistic regression approach was achieved worse/better accuracy than LDA and was significantly faster/slower to train.”

Introduction (5+ sentences) Summarize the project task, the two datasest, and your most important findings. This should be similar to the abstract but more detailed. You should include background information and citations to relevant work (e.g., other papers analyzing these datasets).

Datasets (5+ sentences) Very briefly describe the and how you processed them. Describe the new features you come up with in detail. Highlight any possible ethical concerns that might arise when working these kinds of datasets. Note: You do not need to explicitly verify that the data satisfies the i.i.d. assumption (or any of the other formal assumptions for linear regression).

Results (7+ sentences, possibly with figures or tables) Describe the results of all the experiments mentioned in Task 3 (at a minimum) as well as any other interesting results you find. At a minimum you must report:

<ol>

 <li>A discussion of how the logistic regression performance (e.g., convergence speed) depends on the learning rate.(Note: a figure would be an ideal way to report these results).</li>

 <li>A comparison of the runtime and accuracy of LDA and logistic regression on both datasets.</li>

 <li>Results demonstrating that the feature subset and/or new features you used improved performance.</li>

</ol>

Discussion and Conclusion (5+ sentences)     Summarize the key takeaways from the project and possibly directions for future investigation.

Statement of Contributions (1-3 sentences)           State the breakdown of the workload across the team members