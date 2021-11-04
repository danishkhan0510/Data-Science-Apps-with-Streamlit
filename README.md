# Data-Science-Apps-with-Streamlit
Web App creation for your Data Science projects have been made easy with Streamlit. Here are some projects to help you familiarize with Streamlit and Python.


## Project 1
### Simple Bioinformatics DNA Count
**Packages** - Pandas, StreamLit, altair(for visualization), PIL(To import jpeg files).  
We have the imported logo displayed at the top. Then we have a text area where we put the entire DNA sequence. A sequence has been implicitly provided. You can type your own sequence and hit Ctrl+Enter.
A dictionary gives you the count of Adenine(A), Thymine(T), Guanine(G), Cytosine(C). This is in the raw dictionary format which may not be readable by the user, so we display the entire strings in the next part. Then we create a data frame with the name and count of each entity which is printed subsequently. In the end we display a count chart for each entity.

## Project 2
### EDA Basketball
**Packages** - Pandas, StreamLit, Matplotlib, Seaborn, Numpy, base64.  
**Note** - If an error occures when you run the app for the first time, install 'lxml' package.  
**Data Source** - https://www.basketball-reference.com/  
First we perform web scraping to get Player Stats for any chosen year.
We then create a sidebar for customised parameter selection from the user. Year is the first paramater. Selecting Team is another, where we can select all, multiple or a single team. Position is another parameter with functionality similar to team.
We filter out the rows for the Team and Position values selected from the sidebar.
We create a function to directly download the csv file from the web application itself. You can visit the linnk given to know more about how to download file in streamlit.
https://discuss.streamlit.io/t/how-to-download-file-in-streamlit/1806
We then create a button which can be pressed to display a heatmap for the correlation of the columns.

## Project 3
### S&P500 Stock Price
**Packages** - Pandas, StreamLit, Matplotlib, Seaborn, base64, yfinance.  
**Data source** - https://en.wikipedia.org/wiki/List_of_S%26P_500_companies  
First we scrape the table containing information of all S&P companies from the above website. We create a sidebar to select the sector of choice and also the number of companies we would want to visualize. We create a function to directly download the csv file from the web application itself. We use yfinance to download stock price information of companies. Use this link to look at the documentation of yfinance https://pypi.org/project/yfinance/
We create a custom function to plot the closing price(I used closing price but you can use any other column of choice) of one company.

## Project 4
### Iris Flower Classification
**Packages** - Pandas, StreamLit, Sklearn.  
**Data Set** - Iris flower data is a very popular dataset implicitly available in sklearn. It has the sepal length, sepal width, petal length, petal width as the independent features. It is  classification problem where we have to essentially predict which type of an iris plant it is i.e. Setosa, Verginica or Versicolor.  
We start by creating a custom function to input all the 4 independent features from the user. We also print the feature values given by the user. We load the datset and seperate the independent and dependent features. We then use the Random Forest classifier for prediction. We get the prediction for our set of independent features and also the probabilities for each class. Finally we print the class labels, our prediction and the prediction probabilities.

## Project 5
### Palmer Penguins Classification
**Packages** - Pandas, StreamLit, Sklearn, pickle.  
**Data Set** - We shall be using the palmer penguins dataset, the goal of which is to provide a great alternative to the iris dataset for data exploration & visualization. The independent features are island, bill length, bill depth, flipper length, body mass and sex. The dependent feature is species. I have uploaded a clean version(missing values removed) of the dataset within the folder for you to use directly.  
We have 2 files and I will talk about each one of them one by one.  
**penguins-model-building.py**  
This is the file where we are building the model. Our first step would be to encode the two categorical features i.e. island and sex. We use get_dummies function for it. We do target encoding for the species column. We then seperate the dependent and independent variables. We build a Random Forest Classifier and lastly we dump the model in a pickle file. This is a good practice because if we don't pickle we will have to run the entire model again and again when we change the input features.  
**penguins-app.py**  
We provide a sidebar for taking inputs from the user. The input here is either through a csv file with all the independent features or you can directly use the sliders and the dropdowns. A sample input file is available for download for you to check out. We create a custom function to check if the user uploads anything or not. If nothing is uploaded we provide preset values or take the input directly from the paramters. We combine the independent feature(either the one provided by the user or the preset values) with the original dataset to make encoding easier. We use the same pre-processing(encoding) steps again. We separate out the input row back now and provide it to the pickled model which we have loaded again. We get the prediction and prediction probabilities and print both subsequently.

## Project 6
### Boston House Price Regression
**Packages** - Pandas, StreamLit, Sklearn, shap(to give you an understanding behind the prediction), matplotlib.  
**Data Set** - You can visit here to know about it in detail https://www.cs.toronto.edu/~delve/data/boston/bostonDetail.html.  
We first load the inbuilt boston dataset of sklearn and seperate the dependent and independent features. We create a sidebar and provide sliders for each independent feature. The default value for each slider is the mean of that column. We use Random Forest Regressor for our predictions. We use the data frame with all input features for the prediction from our model which we print out. Finally we use the shap library to show the feature importance. We visualize it with two plots.  
**Note** - We are not pickling the model and loading it here. Each time we run the model when we change the input features. That is why it takes a lot of time to give the predictions as compared to the previous project where loaded the pickled model. 
