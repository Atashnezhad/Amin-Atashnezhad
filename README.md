

# Welcome to my personal webpage


I am currenlty a Post-doctoral fellow in Chemical and Petroleum Engineering at [Oklahoma State University](https://go.okstate.edu/) working on engineering modeling, optimziation and simulation. I am an aspiring data scientist.
Last two years I have been involved in developing an AI platform for autonomous drilling in geothermal wells which I developed a standalone software in python using tkinter library. 
I love astronomy, piano, and mechanical clocks and I am building one in my spare time.


Here is the list of the latest projects that I have been working on in the data science domain.



<!-- 
## [Developing PDC ROP model using symbolic regression algorithm](https://github.com/Atashnezhad/Machine-learning-to-develop-PDC-ROP-model)
In this project, the symbolic regression machine learning algorithm was used for developing a PDC ROP model.
The SALib library was used for sensitivity analysis and the first and second-order interactions between paramters are seen in the Figure below.

<p float="center">
  <img width="450" src="Assets/symbolic reg ROP.png" >
</p>

The Pysr clearly ignores the dimensionality of mathematical equations. The PySR guides the searching processes toward those equations which result in higher accuracy.
It would be beneficial if the ML algorithm (symbolic regression package) comes with new feathers to consider the dimensionality in the process of evolution.
One method that can be used for dimensionality consideration in PySR is by using a customized loss function. In such a case, it is suggested to develop a function that can measure the normalized behavior of separate input parameters into the dependant parameter. The influence of independent parameters on dependant parameters can be studied separately using lab data or from literature. For instance, there is almost an agreement that the WOB affects the ROP with power bigger than 1. Note that this is true before achieving the flounder point. Once the customized objective function was prepared, it is expected that the PySR incorporate more physics into developing equations.
The sensitivity analysis package in this study was used. As it is seen in the above graph, the PySR found that the WOB, RPM, and UCS have a bigger effect on ROP compare to Dc and NOC.
The results can be affected by the available number of data points too.
Besides the effect of independent parameters in dependant, One should consider the interaction effects. The interaction between independent parameters effectively affects how one independent parameter influences the dependant parameter.
For a problem with five independent parameters, the interaction between independent parameters can happen in the second-order, third-order, and fourth-order fashion ways. Therefore, from a statistical point of view, one should consider more than five independent parameters for modeling purposes. For a problem with five independent parameters, there are 206 interactions and for a 10D problem, there are more than 6M interactions (please check out the interaction calc Notebook in the directory).
The second-order interaction between independent parameters for this study is seen in the following figure. Statistics Analysis visualization was done using the SALib library. The below figure shows the contribution of each input to output parameters along with second-order as indices width.

-->


## [Artificial intelligence for lung disease detection using chest CT scan images](https://github.com/Atashnezhad/Lung_Disease_Detection_Deeplearning)

<p float="center">
  <img width="800" src="Assets/head_2.png" >
</p>

### Main branch on GitHub:
This project is composed of two sub-projects including two class and four class classifications.
Tensorflow library was used to develop deep convolutional networks. In a two-class classification project, data augmentation was used and the new data was divided into three sections including train, validation, and test. A CNN network was applied to find the pattern in the  CT scan chest images.

In the four-class classification project, the data was imbalanced, therefore to overcome imbalance data, two different techniques including weighted objective function and over-sampling were applied.

The four-class classification codes were uploaded into the google collab to be ran using GPU. The results along with network visualization were provided.
Both CNN models are able to classify the problems with good accuracy. Using a generator to increase the number of images is not suggested in general. Fluctuations in the validation data set accuracy versus iteration were observed (see below Figure). 

<p float="center">
  <img width="500" src="Assets/LearningCurvefourClassClassification.png" >
</p>

The CNN network fits the train data fine while it fails in the validation part (can't capture the patterns) which can be a sign of having bias (due to network size). Having fluctutation in the validation curves (both for accuracy and validation) can be a sign of overfitting which is due to lack of data for two classes (Pneumocystis and Streptococcus) in four class classification project. In the following, a smaller network was trained.

### Second branch on GitHub (Default):

Using ImageDataGenerator does the normalization. Note that in the validation and test section, I just applied the normalization. In two-class classification, the number of images is equal so there is no need for balancing the dataset. However, for the four-class classification, I have imbalanced data and I need to consider it to prevent bias. In four class classification, I augmented and oversampled for all four classes. The Normal and Covid cases were augmented and over-sampled from 190 to 1000 images. The Pneumocystis and Streptococcus were augmented and over-sampled from 21 and 12 to 1000 images. Both classification models' accuracy reached 80%. Deep Convolutional Network Network (CNN) Classification results for four classes are seen below.



<p float="center">
  <img width="1000" src="Assets/Colab/plot_4C_Normal.png" >
  <img width="1000" src="Assets/Colab/plot_4C_COVID.png" >
  <img width="1000" src="Assets/Colab/plot_4C_Pneumocystis.png" >
  <img width="1000" src="Assets/Colab/plot_4C_Streptococcus.png" >
</p>







## [Binary Class Classification (NASA and Space) on Reddit data using NLP](https://github.com/Atashnezhad/Natural_language_processing_Project)

Check out the below sentences. It is hardly possible to differentiate between sentences from NASA and Space community? However AI does differentiate sentences easy! In this project, new featuer engineered data, boost AI estimation accuracy from 75% to 96%. AI amazingly does such complicate tasks.
```
A) A star shining through Saturn's rings.
B) Online space-related degree.
C) M1: The Incredible Expanding Crab Nebula.
D) Took this with a camcorder since I don't have any fancy telescopes or nothin.
E) I went to ksc for Christmas and got to see what made me interested about spaceflight.
F) I went to the John F. Kennedy Space Center.
```
The A,C,E,and F senteces are from NASA community and B and D are from Space community.

In this project, NLP was applied for two-class classification purposes. The data were gathered from Reddit for two close subjects including space and NASA.
A new set of data were featured and extracted which was later used for ML algorithm classification. 
The analysis shows that a new engineered set of data (EDA) shows higher accuracy and boosts the ML algorithms performance. 
Merging both vectorized text and Engineered data set (EDA) even helps more and boosts the accuracy above 80%. 
Finally having an ensemble model works the best with an accuracy of 96%. The ROC curve for different algorithms used along with data are seen at the following figure.

<!--
Comparison between different algorithm accuracies and type of data set used is seen in the following Figure.


<p float="center">
  <img width="600" src="Assets/plot_04_03_4.png" >
</p>
-->
<p float="center">
  <img width="550" src="Assets/plot_05_ROC.png" >
</p>




## [Frauds Detection Project](https://github.com/Atashnezhad/Frauds-Detection-Project)

In this project, a set of data from Talking Data competition was used for two-class classification. Different ML algorithms were used for this purpose. The data was imbalanced therefore I used several approaches to deal with data including, oversampling, reading data in batch considering the machine RAM into account and then applying ensumple method using all developed train models, a customized appraoch where I filtered the data with a value of 1 out of 7 GB data and then count the same number of 0 values and added to base data. Results were a CSV file with 800k rows data points but balanced (now all 1 values are included and the ML algorithms can learn more effecintly) and lastly I selected appropriate hyperparameters to deal with imbalanced data. 

In a seperate sub-project, a python library for symbolic regression was used on sub-set data. The data normalized and was fed into the symbolic regression algorithm.





## [XGBoost Hyperparameters Tuning using Differential Evolution Algorithm - Frauds detection application](https://github.com/Atashnezhad/XGBoost_Hyperparameters_Tuning)

In this project, the metaheuristic algorithm is used for tuning machine learning algorithms hyper-parameters. A fraud detection project from the Kaggle challenge is used as a base project. The Project composed of three distinct sections.

* Metahurestic Algorithm (MA): 
  Differential Evolution Algorithm (DEA) selected as an intelligent searching tool. The DE Algorithm is work on top of the ML Algorithm (in this case XGBoost) to find the best set of hyper-parameters.
* Machine Learning Algorithm: 
  The XGBoost which is a powerful machine learning algorithm is selected and the DEA is applied to find the best set of hyper-paratmers.
* Final step: 
  The Tuned ML algorithm is applied to the Fraud detection challenge (training, validation, and test). The results was promising and showed 89% accuracy on test data.
In this notebook, we apply the Intelligent search methods like Differential Evolution Algorithm to find the best ML algorithm hyper-parameters. Previous options are using either predetermined or randomly generated parameters for the ML algorithms. Some of these searching methods are actually a simulation of Intelligent agents in nature like the folk of birds or school of fishes.

## [Big Data Project using Pyspark in Docker](https://github.com/Atashnezhad/Fraud_Detection_Pyspark)

<p float="center">
  <img width="600" src="Assets/fraud.png" >
</p>


In this project, the [Kaggle Fraud detection challenge](https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection) was studied. A docker image of Pyspark along with the Jupyter Notebook was used. 





 

### My Hobby projects: A Clock inspired by Hisashige Tanaka a Japanese rangaku scholar 

I love mechanical clocks and this is my hobby project. 

Hisashige was a Japanese rangaku scholar, engineer and inventor during the Bakumatsu and early Meiji period in Japan. In 1875, he founded what became the Toshiba Corporation. He has been called the "Thomas Edison of Japan" or "Karakuri Giemon." (Wikipedia)

The following visualization in python shows my clock design for STILLWATER, OK, USA. The clock indexes dynamically shift based on the length of the day depending on the season. In summer more hours indexes show up at the top side of the clock which is representative of daylight, while during winter more hour indexes are seen at the lower side of the circle.

<p float="center">
  <img width="150" src="Assets/My_Clock.gif" >
  <img width="400" src="Assets/Amin_clock_OKC_2.gif">
</p>



And some dancing sculptures [here](https://vimeo.com/manage/videos/508537606) and [here](https://vimeo.com/manage/videos/516458620).

