# SC1015 Mini Project - Twitch.tv
Our team's objective is to make use of the the Twitch's API to help out small or upcoming streamers on how to be opular on twitch. In our project, we will be extracting data from the most popular streamers and find out what factors propels these streamers to become a twitch superstar. How we will be defining popularity in our project would be through viewer count.
![image](https://user-images.githubusercontent.com/102810962/164954067-f02bca75-5dbb-4495-b3af-2bce64ef6d70.png)
## Tech Stack
- Data retrieval: Twitch API Platform, XMLHttprequest from twitchtracker.com
- Data wrangling: Python
- Data visualisation: Tableau
- Presentation: PowerPoint, Windows movie maker
- 
## Algorithms/Libraries
- Pandas, seaborn
- Naive-bayes
- Linear regression

## Datasets Folder
### General Info
This is general information of the top 1000 streamers from twitchtracker.com based off by rank. Data is scraped through using a fake_useragent to extract data via XMLHttpRequest of the website.
### Live Streams Data 1-4
Here are the data extracted hourly through the twitch api to access live streams of the top 1000 streamers. Data of live streamers like time, language, descriptio, game and user information are retrieved.

Code to extract these datasets can be found under Jupyter Notebooks / Data Extraction

## Group Presentation Folder
### SC 1015 mini project
The powerpoint provide a summary of our project. It covers problem defintion, motivation, data extraction and preparation from the APIs, our core analysis using regression and classification models including naive bayes, evaluation and the conclusions we draw from our work.

## Jupyter Notebooks
### Data Extraction Notebook
The code in this notebook is used to extract data from the Twitch Api and from the twitch tracker website to form our datasets. First, the general info of the top 1000 streamers are extracted. Then, over the course of 2 weeks, live streamers data are retreived via Twitch API hourly through automation. Then, variables such as game name, time started, language, follower count and average hours streamed are modelled to find relations with popularity


### Linear Regression models notebook
This notebook reads data from General info and does linear regression betwn average hours streamed and viewer count using sklearn seaborn and pandas. Data is first cleaned by removing outliers, then is split into test and train data. Data is first visualised using seaborn, then a linear regression mopdel is fitted on both test and train data. Finally to find out correlation between viewer count and average hours streamed, a goodness of fit test is implmneted, which returns a low explanied variance value, implying lack of correlation.


### Classification models notebook
The notebook reads data from live streams data and finds correlation between game, time streamed and language to viewer count through classification models. It
iterates thru the viewer count and time extracted column to categorise them according to quartile range and time range respectively. Then the same is done for game name to remove all games that accounted for less than 1 percent of total number of streams. This is to clean up the data. The Naive Bayes model is used to come up with a prediction array after parsing in the train and test values. Finally, a confusion matrix is used to illustrate accuracy. The accuracy results returned were poor and showed that there are no factors that returns true values in predicting popularity.

##
