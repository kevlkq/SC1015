# SC1015 Mini Project - Twitch.tv
Our team's objective is to make use of the the Twitch's API to help out small or upcoming streamers on how to be popular on twitch. In our project, we will be extracting data from the most popular streamers and find out what factors propels these streamers to become a twitch superstar. How we will be defining popularity in our project will be through viewer count.

## Contributors
- @kevlkq
- @Purrsona
- @iloveangpao

![image](https://user-images.githubusercontent.com/102810962/164980283-354b5920-5605-4e1f-9aa0-8eecf116c570.png)

## Tech Stack
- Data retrieval: Twitch API Platform, XMLHttprequest from twitchtracker.com
- Data wrangling: Python
- Data visualisation: Tableau
- Presentation: PowerPoint, Windows movie maker

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
The code in this notebook is used to extract data from the Twitch Api and from the twitch tracker website to form our datasets. First, the general info of the top 1000 streamers are extracted. Then, over the course of 2 weeks, live streamers data are retreived via Twitch API hourly through automation. Then, variables such as game name, time started, language, follower count and average hours streamed are modelled to find relations with popularity. This notebook is done by Lua Ker Quan Kevin.


### Linear Regression models notebook
This notebook reads data from General_Info.xlsx and constructs a linear regression model betweenn average hours of streams and average viewer number using sklearn, seaborn and pandas libraries. Data is first cleaned by removing outliers, and then split into test and train data. We visualised the clean data using seaborn, and from there, constructed a linear regression model fitted on both test and train data. Finally to find out correlation between viewer count and average hours streamed, a goodness of fit test is implemented, which returns a low explanied variance value and MSE, implying lack of correlation. This notebook is done by Lu Zihao.


### Classification models notebook
The notebook reads data from live streams data and finds correlation between game, time streamed and language to viewer count through classification models. It
iterates thru the viewer count and time extracted column to categorise them according to quartile range and time range respectively. Then the same is done for game name to remove all games that accounted for less than 1 percent of total number of streams. This is to clean up the data. The Naive Bayes model is used to come up with a prediction array after parsing in the train and test values. Finally, a confusion matrix is used to illustrate accuracy. The accuracy results returned were poor and showed that there are no factors that returns true values in predicting popularity. This notebook is done by Lim Yan Rui.

## Conclusion
For inital data visualisations, we can see that top games maybe a huge contribution to a streamer's popularity. However, our models and accuracy scores shows that there are no gurantees in becoming popular by playing a popular game. The same can be said for other factors such as time of stream, language and hours streamed. The accuracy scores and explained variances are too low to show strong correlation between these factors to viewer count. Since quantitative analysis shows us weak relations, we concluded that it boils down to the personality of the streamer and how they create content that defines their popularity.

## References
- www.twitchtracker.com
- www.twitch.tv
- https://pandas.pydata.org/docs/reference
- https://dev.twitch.tv/docs/cli/api-command
- https://dev.twitch.tv/docs/api/
- https://tqdm.github.io/docs/tqdm/
- https://pypi.org/project/fake-useragent/
- https://scikit-learn.org/stable/
- https://docs.python.org/3/library/os.path.html
- https://seaborn.pydata.org/tutorial/categorical.html
