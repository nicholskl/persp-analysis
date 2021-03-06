# Persp-Analysis Assignment 1

#### Name: Mengchen Shi

#### Date: October 15th, 2017

## Internet interaction and the stock market: evidence from stock forums in China

### Introduction
The relationship between information and stock market is one of the core problems in finance. According to Efficient Market Theory (Fama, 1970), the accessibility of information determines the efficiency of the market. 

Unlike mature stock markets, the stock market in China consists of a large number of individual investors. The transaction volumes generated by Individual investors in China accounted for 1/3 of that in the whole world in 2015 (World Federation of Exchanges). Traditional finance theories hold that individual investors tend to have less funds, to pay more to obtain information, and have few ways to express opinions. Thus, individual investors are at disadvantage in obtaining information and influence the market through expressing their opinions. Individual investors can be easily misled by information, leading to irrational volatility in the stock market. 

Traditional analyses and predictions about stock market based on structured data such as historical data and financial indexes. With the widespread of internet, more and more individual investors gain information, express views and interact on the internet and social media. Therefore, unstructured data such as blogs and posters from stock forums have being included in stock market analyses(fung et al, 2002). Does people’s interaction on the internet influence the stock market in China? In our research, we hope to answer this question by grabbing, digging and analyzing data from the internet, specifically, stock forums in China. There are two hypotheses:

  * The number of positive opinions of a stock has a positive relationship with the volumes and yields.
  * The disagreement of the market will increase the transaction volumes and the volatility in the market.  

### Data
There are two kinds of data we plan to use in the research. The first one is the interaction data from stock forums. We could use text mining and data crawling tools analyzed the posters on Guba and Xueqiu, the two largest stock forums in China. Posters on these forums are posted by users, mainly individual investors, to show their views, share their experience, or simply express their emotions about the market. One poster is posted by one main user(Louzhu), and can be “liked” or “rejected” by other users. Other users can post their response to Louzhu’s views under the poster. The posting time, the numbers of readers and responses of each poster are available to all users, and thus available to researchers as well.

The second type of data will come from the stock market: the index, prices, transaction volumes, volatility and yields of the whole market as well as individual stocks. The internet interaction’s impacts on the stock market can be very quick yet slight. In order to catch these instant volatilities, high frequency data are preferred. 

### Method
We will analyze the relationship between internet interactions with the whole stock market and individual stocks, separately. Forecasting strategy is the best approach in designing an observational study to answer our questions. 

There are two variables of internet interactions to be constructed: the degree of positive/negative emotions reflected in the posters, and the degree of disagreement among users. The degree of positive/negative emotions indicates the collective attitudes towards the market or an individual stock. The degree of disagreement refers to how investors’ ideas about the market or a stock diverge. These degrees can be evaluated by counting the number of main posters and their numbers of “liked”, “rejected””, readers and the responses. To sort “positive”, “negative” and “neutral” emotions and to divide “support” and “reject” attitudes in the texts, we will first analyze some pieces of information by hand, and then apply machine learning techniques to training the computer to determine the emotions of the remain observations.

Then we can do correlation analysis and regression analysis to figure out the relationship between the internet interaction and the performance of the market. After that, we can utilize our results to predict the changes in the stock market according to the degrees of emotions and the degrees of disagreement in stock forums. For instance, we have a guess that a pervaded positive opinion is strongly related to the good performance in the short-term market. We can explore the relationship between them and validate the connection by forecasting the market according to the collective views in stock forums. The relationship is proved to exist if the real market performance is consistent with our predictions. Hopefully, the internet interaction among individual investors can be used to forecast the performance of stock market in practice. 

### Discussion
#### How does this project illustrate the good characteristics of big data
The project can benefit from all three good characteristics of big data mentioned by Salganik. 

First of all, the research benefit from the a big volume of data. The data comes from the two largest stock forums in China, where thousands of main posters appear every day with 800 clicks and 5 responses on average. Such a big number guarantees the representativeness of the observational data, and increase our ability to drive causal estimation.

Second, the “always-on” characteristic of big data provides us with data over long time, which enlarges the number of observations as well as enables real-time information. For instance, we can analyze the relationships during a long period as long as the posters still exist. Moreover, the data on the internet are always-on as anyone can post any information at any time, and the data of stock market are changing continuously. This fact enables us to conduct instant observations. For example, to validate the forecasting capability, we can closely observe the real-time relationship between the interactions on the internet and the instant responses in the stock market.

Finally, our research will not have reactive problems. Users will not be aware that their behaviors will be used to research, since the data crawling methods do not disturb or interact with users directly. Even though the users might realize that their behaviors can be observed by others, they will not care— this is the nature of forums on the internet.

#### How to overcome the weaknesses of big data
Although the data take advantage of big data, three shortcomings of big data – incompleteness, drifting, and dirty – bring problems to the research.

Incompleteness is the first problem. Not all posters and responses exist forever. Some of them might be deleted over time, which means loss of considerable amounts of observations. Moreover, every individual is allowed to have several IDs in one forum, and we lack complete information to figure out whether some similar opinions are put forward by the same individual. To overcome this problem, we can analyze users’ ID and IP to merge similar opinions from the same individual.

The second problem is drifting. The users (population drifting) and the behaviors of users can change over time. In addition, the system (e.g., how to post, response and like a poster) and the management rules of the stock forum can change over time. To eliminate the potential influence driven by drifting, we can first analyze the composition of users during different periods and their behavioral data, and then create variables to describe these features. For example, variables about age, gender, experience, and the active frequency of users can be included in the regression function when analyzing the relationships. To avoid problems caused by system drifting, we can divide data into groups according to the time the systematic changes happened, and then analyze the data in different periods separately. 

Another potential concern is dirty. Some contents in the forum might be unrelated to investment, or are repeated by the same user for many times, causing dirty data. This problem, however, can be easily handled by advanced text mining and machine learning tools. For instance, we can train the computer to exclude the useless and miscellaneous information. 

In conclusion, the bigness of data improves our abilities to explore the questions. Although we might suffer from some problems brought up by its disadvantages, we can overcome them with appropriate tools.

### Reference
[1]Fama, E. F. (1970). Efficient capital markets: a review of theory and empirical work. Journal of Finance, 25(2), 383-417.  
[2]Fung, G. P. C., Yu, J. X., & Lam, W. (2002). News Sensitive Stock Trend Prediction. Pacific-Asia Conference on Advances in Knowledge Discovery and Data Mining (Vol.174, pp.481-493). Springer-Verlag.  
[3] World Federation of Exchanges, <https://www.world-exchanges.org/>
