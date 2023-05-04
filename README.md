Download Link: https://assignmentchef.com/product/solved-cs585-hw4-data-mining-tool-based
<br>
In this homework, you are going to use three UI-based tools (no coding!), to carry out data mining: <strong>WEKA, KNIME, RapidMiner.</strong> There are 6 questions you need to answer.

<strong>Description</strong>

<h1>WEKA</h1>

Start by downloading WEKA, from <a href="https://www.cs.waikato.ac.nz/ml/weka">https://www.cs.waikato.ac.nz/ml/weka (https://www.cs.waikato.ac.nz/ml/weka).</a> Note – you can use an older 32-bit version, if your laptop is unable to run the latest 64-bit one. FYI WEKA is written in Java, so you need to install Java [most likely you already have it] prior to installing WEKA. WEKA is powerful and capable – you can continue using WEKA long after this course, and in the future, even consider extending it by writing plugins for it.

<a href="https://www.cs.waikato.ac.nz/ml/weka/mooc/dataminingwithweka/">Take a few hours to go through WEKA’s tutorials: https://www.cs.waikato.ac.nz/ml/weka/mooc/dataminingwithweka/</a>

<a href="https://www.cs.waikato.ac.nz/ml/weka/mooc/dataminingwithweka/">(https://www.cs.waikato.ac.nz/ml/weka/mooc/dataminingwithweka/). You can also look at YouTube videos to come u</a>p to speed. It is just a matter of getting familiar with the UI, and with the overall workflow (read in data → possibly cleanup data → possibly do EDA → do analysis → possibly export results).

<a href="http://tunedit.org/repo/UCI/numeric/housing.arff">Here (data/housing.arff) is a famous (in the ML/DM community) dataset called the ‘Boston Housing Dataset’.</a>

<a href="http://tunedit.org/repo/UCI/numeric/housing.arff">(http://tunedit.org/repo/UCI/numeric/housing.arff) As you can read from the description, it is a dataset that c</a>ontains data regarding houses in several Boston suburbs, published in 1993. It has 506 rows (records) of data, and 14 columns (attributes). For this HW, we’ll use the ‘MEDV’ (median home price) attribute as the “class” (the output to predict). In other words, using existing data from the other 13 columns, we want to be able to learn to predict MEDV <a href="https://www.tophap.com/">for a new record (ie. row) that contains known values for those 13 ‘input’ columns. Note that Zillow (https://www.zillow.com/)</a><a href="https://www.tophap.com/">, </a><a href="https://www.tophap.com/">TopHap (https://www.tophap.com/), etc. routinely carry out such an analysis.</a>

<a href="https://www.cs.waikato.ac.nz/ml/weka/arff.html">As you can see, the data is in a WEKA-native format called ARFF [https://www.cs.waikato.ac.nz/ml/weka/arff.html (https://www.cs.waikato.ac.nz/ml/weka/arff.html)], which resembles, but is more descriptive than, CSV.</a>

Q1 (0.5 point). Build a <strong>linear regression</strong> equation, to predict MEDV. Include a screenshot that shows the linear equation. How many terms are in the equation, and ‘why’? In other words, discuss the resulting equation.

Q2 (1 point). Create a ‘MultilayerPerceptron’ <strong>neural network</strong> that learns the data. You can see that you affect the root mean squared error (‘RMSE’) by setting different values for the learning rate (try to keep this between 0.1 and 0.3), and momentum (again, 0.1 to 0.3). What is the lowest RMSE you are able to achieve? Eg. an RMSE of 5.0 would mean that the MEDV predictions for our 506 rows were off by 5.0 units on the average (the actual values max out at 50, so this represents 10% error on the average). Again, include (two) screenshots that show the NN and the RMSE.

<h1>KNIME</h1>

<a href="http://bytes.usc.edu/cs585/s20_db0ds1ml2agi/hw/HW4/data/shells.arff">Here (data/shells.arff) </a>is another dataset to use (scientists go out ‘in the field’ to painstakingly collect such data! ML might be able to automate some/all of <a href="https://www.google.com/search?q=abalone+shells&amp;num=100&amp;rlz=1C1CHBF_enUS723US723&amp;source=lnms&amp;tbm=isch&amp;sa=X&amp;ved=0ahUKEwihrcyRq8zXAhWJCpAKHXDdDDUQ_AUICygC&amp;biw=1280&amp;bih=541">it). It consists of 4177 rows of data regarding abalone shells (https://www.google.com/search?</a>

<a href="https://www.google.com/search?q=abalone+shells&amp;num=100&amp;rlz=1C1CHBF_enUS723US723&amp;source=lnms&amp;tbm=isch&amp;sa=X&amp;ved=0ahUKEwihrcyRq8zXAhWJCpAKHXDdDDUQ_AUICygC&amp;biw=1280&amp;bih=541">q=abalone+shells&amp;num=100&amp;rlz=1C1CHBF_enUS723US723&amp;source=lnms&amp;tbm=isch&amp;sa=X&amp;ved=0ahUKEwihrcyRq8zXAhWJCpAKHXDdDDUQ_AUICygC&amp;biw=</a>

where each row resulted from measuring 9 parameters/features/values for each shell. The data is in text format (.arff format, for input to WEKA, like above), do take a look at it. The idea is to be able to predict the 9th value, number-of-rings, given the other 8 values, using the existing dataset to learn how to predict.

Next, download and install <a href="https://www.knime.com/">KNIME (https://www.knime.com/) </a>(“nime”), and work through the quickstart tutorial. KNIME is also UI-driven, like WEKA; additionally, it’s also visual-dataflow-driven, which means we can do data mining with it, by ‘connecting the boxes’ (where each box reads data or does mining or writes data, etc).

Q3 (1 point). Use KNIME to perform <strong>linear regression</strong> [on all parameters, not a subset]. You need these nodes: AARF Reader, Linear Regression Learner. Create and connect the nodes, and execute each. What is the linear equation? Include a screenshot.

Q4 (1 point). Set up a <strong>‘Decision Tree Learner’</strong> predictor, where ‘sex’ is the predicted variable. Note – think “simple” – no need to partition the data into training and test data, etc! Provide a snapshot (.jpg or .png) of the *entire* decision tree [OK if the nodes are too zoomed out and are therefore unreadable] – hint: look at the *right* side of the split-pane window.

<h1>RapidMiner</h1>

Download <a href="https://rapidminer.com/products/studio/">RapidMiner Studio (https://rapidminer.com/products/studio/),</a> and play with it for a bit – it is also dataflow-based, just like KNIME.

Q5 (1 point). Bring in the shells.arff data (in the operators list, look under Data Access -&gt; Files -&gt; Read), and only work with these 4 params:

length,diameter,height,num_rings (use a ‘Select Attributes’ node, and type in a regular expression that specifies length,diameter,height,num_rings, or use <a href="https://www.youtube.com/watch?v=tQ7oDnQXhmQ">the ‘subset’ attribute filter to pick the ones we want – search the documentation for how (additionally, this will help: https://www.youtube.com/watch? v=tQ7oDnQXhmQ (https://www.youtube.com/watch?v=tQ7oDnQXhmQ)). Create 6 </a><strong><a href="https://www.youtube.com/watch?v=tQ7oDnQXhmQ">clusters</a></strong><a href="https://www.youtube.com/watch?v=tQ7oDnQXhmQ"> (with all the 4 attrs together, ie. you’d be clustering a 4D </a>dataset) out of the 4177 pieces of data (use a kMeans ‘Clustering’ node). Question: how many data points are in each cluster? Include a screenshot.

Q6 (0.5 point). Next, do a <strong>linear regression</strong> to predict num_rings, from length,diameter,height. Question: what is the equation? Include a screenshot. Note that you need a ‘Set Role’ node where you would set num_rings to be a “label”, before doing the regression (to let the regression node know which attribute to predict, using the other non-label ones). The regression itself would be done using a ‘Linear Regression’ operator.