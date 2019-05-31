<h1>
kaggle-Titanic-Machine-Learning-from-Disaster-Solution
</h1>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/maxresdefault.jpg" width="50%" title="logo">
</p>
In this challenge, we will complete the analysis of what sorts of people were likely to survive. In particular, we will apply the tools of machine learning to predict which passengers survived the tragedy.
<h2> Tools : </h2>
Python : Scikit-Learn, Matplotlib, Numpy, Pandas.
<h2>Data</h2>
891 Observations.
<br>
12 Features :
- Survival , Ticket class, Sex, Age in years, spouses aboard the Titanic, children aboard the Titanic, Ticket number, Passenger fare, Cabin number, Port of Embarkation.
<h1>Data Analysis</h1>
<h2>Correlation Coefficient</h2>
<p> 
 we will use the correlation coefficient to know the best predictor variables
</p>
<p align="center">
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/Capture.PNG" title="logo">
</p>
<p>
it's clear that the two variables that have a correlation coefficient closest to one are:
<br>
- Sex: - 0.54
<br>
- Pclass: - 0.32
<br>
we remind that a perfect correlation between two variables is equal to one that is why we see that the correlation coefficient between Survived and itself is equal to one, because the values are the same                                                                     
</p>

<h2>Sex Variable</h2>
<p>
let's take a look at the sex variable now.
this variable is Boolean ie it can have two values:
<br>
<strong>1: For men</strong>
<br>
<strong>0: For woman</strong>
<br>
the variable "Survived" is also Boolean:
<br>
<strong>1: the passenger will survive</strong>
<br>
<strong>0: the passenger will not survive</strong>
<br>
after calculating the correlation coefficient with the variable "Survived" we found a coeffition of - 0.54.
<br>
a negative coeffition means that the values of the two variables evolve in a contrary direction, we call it a negative correlation.
this means that when the variable "Survive" is Zero the variable "Sex" is equal to One and vice versa.
having a coeffition of -0.54 can be explained as follows:
it is possible that the person who survive to the disaster is a woman.
<br><br>
<strong>in other words, women were more likely to survive than men</strong>
<br><br>
<strong>BAAM ! it was easy to get OUR first Insight</strong>
</p>


<h2>Pclass Variable</h2>
<p>
let's use what we concluded earlier to strengthen our analysis
<br>
now  we will use "Pclass" variable to see which class were the women who survived the disaster
<br>
</p>

``` Python
len(train.loc[(train['Pclass'] == 1) & (train['Survived'] == 3) & (train['Sex'] == 0)])
len(train.loc[(train['Pclass'] == 2) & (train['Survived'] == 2) & (train['Sex'] == 0)])
len(train.loc[(train['Pclass'] == 3) & (train['Survived'] == 1) & (train['Sex'] == 0)])
```
<br>
<p>
That's return :
<br>
54
<br>
54
<br>
63
</p>
<br>
<p>
 unfortunately this information does not add value to our analysis we can't say that the women who survived were in a very specific class
<br>
the analysis stage is far from over, we could try to see other variables ( of course we were interested in the two best variables but maybe we could get some other informations from the remaining variables ) or create predictive models to better understand our data.
<br>
but our goal is not to stop here, it's just a good start for creating a powerful model that can predict whether or not a passenger will survive the titanic disaster
</p>

<h2>Data Distribution</h2
<p align="center">
  <br><br>
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/datadist.png" title="hover text">
</p>
<p>
  some machine learning algorithms like linear regression and SVM work better when the distribution of variables be Gaussian (normal)
<br>
and therefore it's wise to apply a "log" transformation to have this distribution
</p>

<h1>Learning</h1>
<h2>Algorithm</h2>
<p align="center">
  Random Forest
  <br><br>
  <img src="https://storage.googleapis.com/kainofreelancerpictures/anes/rf.jpg" width="500" title="hover text">
</p>
<h1>Performance</h1> 
<h2>Accuracy</h2>
Accuracy = # correct predictions / # totals predictions
<br>
<strong> Accuracy = 81% </strong>

<h2>How to use the code</h2>
1. Clone the project
<br>
2. in the script.py you will find all steps of the project
<h2>Contribution</h2>
<h3>Realized by:</h3>
- Anes Abdelfatah ABBAD.
