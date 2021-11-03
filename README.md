# Data-Science-Apps-with-Streamlit
Web App creation for your Data Science projects have been made easy with Streamlit. Here are some projects to help you familiarize with Streamlit and Python.


## Project 1
### Simple Bioinformatics DNA Count
Packages used - Pandas, StreamLit, altair(for visualization), PIL(To import jpeg files).  
We have the imported logo displayed at the top. Then we have a text area where we put the entire DNA sequence. A sequence has been implicitly provided. You can type your own sequence and hit Ctrl+Enter.
A dictionary gives you the count of Adenine(A), Thymine(T), Guanine(G), Cytosine(C). This is in the raw dictionary format which may not be readable by the user, so we display the entire strings in the next part. Then we create a data frame with the name and count of each entity which is printed subsequently. In the end we display a count chart for each entity.

## Project 2
### EDA Basketball
Packages used - Pandas, StreamLit, Matplotlib, Seaborn, Numpy, base64.  
Note - If an error occures when you run the app for the first time, install 'lxml' package.  
Data Source - https://www.basketball-reference.com/  
First we perform web scraping to get Player Stats for any chosen year.
We then create a sidebar for customised parameter selection from the user. Year is the first paramater. Selecting Team is another, where we can select all, multiple or a single team. Position is another parameter with functionality similar to team.
We filter out the rows for the Team and Position values selected from the sidebar.
We create a function to directly download the csv file from the web application itself. You can visit the linnk given to know more about how to download file in streamlit.
https://discuss.streamlit.io/t/how-to-download-file-in-streamlit/1806
We then create a button which can be pressed to display a heatmap for the correlation of the columns.

## Project 3
### S&P500 Stock Price
Packages used - Pandas, StreamLit, Matplotlib, Seaborn, base64, yfinance.  
Data source - https://en.wikipedia.org/wiki/List_of_S%26P_500_companies  
First we scrape the table containing information of all S&P companies from the above website. We create a sidebar to select the sector of choice and also the number of companies we would want to visualize. We create a function to directly download the csv file from the web application itself. We use yfinance to download stock price information of companies. Use this link to look at the documentation of yfinance https://pypi.org/project/yfinance/
We create a custom function to plot the closing price(I used closing price but you can use any other column of choice) of one company.

## Project 4
### Iris Flower Classification
Packages used - Pandas, StreamLit, Sklearn.  
Iris flower data is a very popular dataset implicitly available in sklearn. It has the sepal length, sepal width, petal length, petal width as the independent features. It is  classification problem where we have to essentially predict which type of an iris plant it is i.e. Setosa, Verginica or Versicolor.  
We start by creating a custom function to input all the 4 independent features from the user. We also print the feature values given by the user. We load the datset and seperate the independent and dependent features. We then use the Random Forest classifier for prediction. We get the prediction for our set of independent features and also the probabilities for each class. Finally we print the class labels, our prediction and the prediction probabilities.
