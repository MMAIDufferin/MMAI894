# MMAI894
# Deep Learning


•Data Exploration

•Word2Vec

•Glove

•Data Augmentation

•LTSM

•CNN

•Zero Shot Learning


# Executive Summary 

Productivity: 

Though emails can be a valuable source of information and have remained the primary method of communication in the workplace, they can also have a significant negative impact on worker productivity. In fact, reading preview text alone costs workers 87 hours a year.6 That is almost eleven working days (based on an 8-hour day) spent without anything to show for, not even having replied to the emails themselves. With classification, workers are directed to focus their attention on the areas that matter most and are less likely to feel overwhelmed by a full inbox. 

Data Cleaning and EDA: 

    Data is pretty clean; except for Cc and Bcc columns (which are expected to be empty), only Subject and To columns have less than 5% null values. The date column has been converted to datetime during the data cleaning process, 

    The top 2 email senders greatly outweigh the others while a significant number of emails do not have any recipients.  

    Most of the emails have blank string for the subject line 

    In terms of distribution of emails, Wednesday is the busiest day of the week; and as for hours, 2 peaks happen at 10 am and 16 pm 

    Topic exploration is also applied to the Message column and the result is also attached. 

 

By running clusters using k-means we were able to uncover the themes in the vector representations and identified 6 departments. We augmented the list of keywords in each department by using cosine distance. After applying feature engineering, label encoding and tokenization, the data was ready to be modeled. We began by running 3 LSTM models using the same parameters side by side and compared them. The data fed into each of the models respectively was: 

-       Experiment 1: Word2Vec pre-trained embeddings without tuning  

-       Experiment 2: GloVe  pre-trained embeddings without tuning  

-       Experiment 3: GloVe  embeddings that we fine-tuned using our Enron database 

Experiment 3 had the highest accuracy score. Now that we know that tuning the pre-trained model with our data set gives us a better score, we tested a CNN model which accomplised an even higher accuracy score.  

Recommendations and observations 

There are still many recommendations we would propose to make our classifier even more effective. Having more data to train our model as well as more capabilities of the model itself such as project-level sorting, triaging, and recognizing phishing attempts can result in a model that is more likely to be positively received for widespread adoption. 

Operationalization and scaling: 

Prior to production and deployment, there are still many scaling factors to consider for the future. Having a strategy for continuous training after the model has been deployed, data security and compliance, and explainability are all important in ensuring that the model can have an impact in the workplace not only in the short-term but also for the foreseeable future. 
