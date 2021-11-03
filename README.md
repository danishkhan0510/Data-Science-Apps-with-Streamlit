# Data-Science-Apps-with-Streamlit
Web App creation for your Data Science projects have been made easy with Streamlit. Here are some projects to help you familiarize with Streamlit and Python.


## Project 1
### Simple Bioinformatics DNA Count
Packages used - Pandas, StreamLit, altair(for visualization), PIL(To import jpeg files)
We have the imported logo displayed at the top. Then we have a text area where we put the entire DNA sequence. A sequence has been implicitly provided. You can type your own sequence and hit Ctrl+Enter.
A dictionary gives you the count of Adenine(A), Thymine(T), Guanine(G), Cytosine(C). This is in the raw dictionary format which may not be readable by the user, so we display the entire strings in the next part. Then we create a data frame with the name and count of each entity which is printed subsequently. In the end we display a count chart for each entity.

## Project 2
### EDA Basketball
Packages used - Pandas, StreamLit, Matplotlib, Seaborn, Numpy, base64.
Note - If an error occures when you run the app for the first time, install 'lxml' package.
First we perform web scraping to get Player Stats for any chosen year. The data is available here - https://www.basketball-reference.com/.
We then create a sidebar for customised parameter selection from the user. Year is the first paramater. Selecting Team is another, where we can select all, multiple or a single team. Position is another parameter with functionality similar to team.
We filter out the rows for the Team and Position values selected from the sidebar.
We create a function to directly download the csv file from the web application itself. You can visit the linnk given to know more about how to download file in streamlit.
https://discuss.streamlit.io/t/how-to-download-file-in-streamlit/1806
We then create a button which can be pressed to display a heatmap for the correlation of the columns.
