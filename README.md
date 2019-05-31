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
having a coeffition of 0.54 can be explained as follows:
it is possible that yhe person who has survival to the disaster is a woman.
<br><br>
<strong>in other words, women were more likely to survive than men</strong>
<br><br>
<strong>BAAM ! it was easy to get OUR first Insight</strong>
</p>


<h2>Pclass Variable</h2>
<p>
use what we concluded earlier to strengthen our analysis
<br>
now use the variable "Pclass" to see which class were the women who survived the disaster
<br>
</p>
<br>

``` Python
len(train.loc[(train['Pclass'] == 1) & (train['Survived'] == 1) & (train['Sex'] == 0)])
len(train.loc[(train['Pclass'] == 2) & (train['Survived'] == 1) & (train['Sex'] == 0)])
len(train.loc[(train['Pclass'] == 3) & (train['Survived'] == 1) & (train['Sex'] == 0)])
```


<h1>Apprentissage</h1>
<h2>Algorithme utilisé</h2>
<p align="center">
  SVM ( Support Vector Machine )
  <br><br>
  <img src="https://zestedesavoir.com/media/galleries/3985/5128cf36-de17-4ebb-9495-90c9d85f006f.png" width="350" title="hover text">
</p>
<h1>Performance</h1> 
<h2>Accuracy</h2>
Accuracy = # prédictions correctes / # prédictions totales
<br>
<strong> Accuracy = 98% </strong>
<h2>Courbes d'apprentissage</h2>

<h2>Comment utiliser le code ?</h2>
1. Clonez le projet et decompressez code.rar
<br>
2. Dans le dossier R vous trouverez les scripts nécessaires pour récuperer les données à partir de la platforme TCGA
<br>
3. Dans le dossier Python vous trouvez un fichier visualisation.py pour visulaiser les données, et un deuxième fichier implementation.py qui contient toutes les étapes de la réalisation du projet.
<h2>Contribution et Remerciement</h2>
<h3>Projet réalisé par :</h3>
- Anes Abdelfatah ABBAD.
