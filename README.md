# SC1015 Mini Project - Twitch.tv
Our team's objective is to make use of the the Twitch's API to help out small or upcoming streamers on how to be opular on twitch. In our project, we will be extracting data from the most popular streamers and find out what factors propels these streamers to become a twitch superstar.
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
The code in this notebook is used to extract data from the Twitch Api and from the twitch tracker website to form our datasets. First, the general info of the top 1000 streamers were


### Linear Regression models notebook


### Classification models notebook

