# Neural_Network_Charity_Analysis

### Project's Overview 

This project is related with Neural Networks and how it is used in the creation of a binary classifier, capable to predict whether applicants will be successful if funded by Alphabet Soup, a non-profit foundation interested on helping organizations that protect the environment and improve people's well-being.

The purpose of this analysis was to explore and implement neural networks using TensorFlow in Python. Neural networks is an advanced form of Machine Learning that can recognize patterns and features in the dataset. Neural networks are modeled after the human brain and contain layers of neurons that can perform individual computations. A great example of a Deep Learning Neural Network would be image recognition. The neural network will compute, connect, weigh and return an encoded categorical result to identify if the image represented. 

### Results 

##### Data Preprocessing:

1.What variable(s) are considered the target(s) for your model?

Checking to see if the target is marked as successful in the DataFrame, indicating that it has been successfully funded by AlphabetSoup.Hence the IS_SUCCESSFUL column is considered the target for our model.

2.What variable(s) are considered to be the features for your model?

The APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT columns are considered to be the features of our model.

3.What variable(s) are neither targets nor features, and should be removed from the input data?

The EIN, NAME, STATUS, and SPECIAL_CONSIDERATION columns are neither targets nor features and should be removed from the input data.These columns will not increase the accuracy of the model and can be removed to improve code efficiency.

##### Compiling, Training, and Evaluating the Model

4.How many neurons, layers, and activation functions did you select for your neural network model, and why?

I selected 120 neurons with a sigmoid function for my first layer, 100 nuerons with a ReLU function for the second, then 80 neurons with a tanh classification for the third and 60 for the fourth, and a sigmoid function for the outer layer. I chose to change the activation function for the first layer because it increased the model's performance.

<img width="970" alt="Screen Shot 2022-04-25 at 7 00 14 PM" src="https://user-images.githubusercontent.com/95304774/165188164-e17d4454-c393-47c4-9109-a62ae4e1aa4d.png">

<img width="580" alt="Screen Shot 2022-04-25 at 7 00 48 PM" src="https://user-images.githubusercontent.com/95304774/165188215-88f2ea92-4b51-4e36-800d-e74c342ed71f.png">

5.Were you able to achieve the target model performance?

Yes, I was able to achieve the target model performance. The target was 75% and we achieved 78.12%. 

<img width="760" alt="Screen Shot 2022-04-27 at 12 53 44 PM" src="https://user-images.githubusercontent.com/95304774/165578794-0cf0c3bd-5f12-49fe-bf46-984e3621e162.png">

<img width="760" alt="Screen Shot 2022-04-27 at 1 02 35 PM" src="https://user-images.githubusercontent.com/95304774/165580384-046baaa5-cf6d-4d53-a2ea-3986572d5823.png">

6.What steps did you take to try and increase model performance?

We tried to increase the model performance by dropping more columns, creating more bins for rare occurances in columns, decreasing the number of values in some bins, adding more neurons to the hidden layers, using a differnet activation function, and increasing the number of epochs. Desiging the model and creating a callback that saves the model's weights every 5 epochs. We tried more hidden layers and increased epochs to 100 to increase model performance.Columns were reviewed and the STATUS and SPECIAL_CONSIDERATIONS columns were dropped as well as increasing the number of neurons and layers. Other activations were tried such as tanh.Linear activation produced the worst accuracy, around 28%. The relu activation at the early layers , tanh activation in the middle and sigmoid activation at the latter layers gave the best results.

### Summary:

A neural network classifier is designed, trained and tested. And in order to improve its performance, three different ways to optimize the model were considered. Even with all the considered changes of removal of features, addition of layers and neurons in the model, and increasing of number of fitting epochs, the accuracy remains the same (~72%). Since different changes in the model were considered, and they did not work as expected, it could be recomended to work with another kind of classification model, i.e., a Random Forest classifier that has a similar accuracy performance than Deep Learning models but that it is much easier to interpretate.





