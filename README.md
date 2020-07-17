Abstracts – Recently there has been a topic of fake news detection on social media, where lots of posts are getting published by many companies and daily basis and in order to identify if there is a fake news or not its not very easy, so with help of Machine learning, we will develop a solution which can identify if this is a fake news or not.

Business Problem Description – In this era, where social media has so much dominance on knowledge and information across the globe, it is very important to identify if it is a fake or a genuine article, so that the knowledge and information is valuable and can a real education for the society.
1. With help of NLP (Natural Language processing), we will create a corpus of words from real and fake news articles. This corpus will be used to create a classifier model, which can predict the news/ article to be fake or real. With this model we can focus on the source of these articles and classify them with high confidence that the news or article coming from the source is real or fake.

Dataset Details – 
There are 20800 and 5 attributes. Key features from the dataset are as below from the training dataset

* id - Identified/ Unique Id for a news articles
* title - Title of a news articles
* author - Author/ Source of the news articles
* text - It is the text of the article; could be incomplete
* label - Label that marks the article as potentially unreliable

Data Preprocessing, performing for the text – attribute
* Remove Line Breaks element
* Remove new Line element
* Remove Hyperlink element
* Remove ampersand
* Remove greater than sign
* Remove less than sign
* Remove non-breaking space
* Remove Emails
* Remove new line characters
* Remove distracting single quotes

Created and plotted the distribution of the sentiments score, it has close to normal distribution, as it seems, it has both positive and negative sentiments almost equally.

![fig9_sentimentsdis](/Images/fig9_sentimentsdis.png)

Correlation matrix, describing the relation between the attributes, the values of the correlation are between -1 and 1, showing positive and negative correlation. There is not strong correlation between any attributes, but there is a negative correlation of -0.12 between length and label.

![fig11cor](/Images/fig11cor.png)

WordCloud from Train Dataset, creating the word cloud of 50 most common words are “Obama”, followed by “Clinton” and “American”.

![fig12wc](/Images/fig12wc.png)

Creating the n-Gram plots for Unigram, Bigram and Trigram, in the unigram, the most common words after stopword and updating stopword, are “trump”, “will” and “one”. In the Bigram, we can see “united states” and “donald trump” and “new york”. In the trigram, we can see the common words are “new york times”, “president Donald trump ” and “new york city”.

![fig14ngwo](/Images/fig14ngwo.png)

T-Statistics helps explain if the means from two samples are different from each other, by calculating the stand error in difference between two means. 
**Null Hypothesis** – Both of the sample are same and equal, there is no difference in their sentiments analysis.
The t-distribution left quartile range is: -1.9600793684470008. The t-distribution right quartile range is: 1.9600793684470004, as shown in fig14

* T-stats =3.249, degree of freedom=20561, cv=1.645, p=0.001, alpha = 0.05.  
* Comparing the critical values to the t-stat, reject the null hypothesis that the means are equal.  
* Comparing the p-value to alpha, reject the null hypothesis that the means are equal. 

Model created for Logistics Regression with Count Vectors, Logistics Regression with TF-IDF Vectors, Multinomial Naïve Bayes classifier with Count Vectors with hyper parameter and Multinomial Naïve Bayes classifier with TF-IDF Vectors with hyper parameter, LSTM (long short term memory) neural network.
![fig16tablescore](/Images/fig16tablescore.png)

Logistic Regression with Count vector has highest AUC-ROC score of 95%.
![fig17roc](/Images/fig17roc.png)


