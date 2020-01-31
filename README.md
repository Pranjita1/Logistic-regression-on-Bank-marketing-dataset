# Logistic-regression-on-Bank-marketing-dataset

Was the campaign successful in targetting customers for their campaign? 
Did they reach out to potential customers at the right time? 
How likely will a customer open a new deposit account?

My dataset is- https://drive.google.com/openid=10lxxaNTtMqtNzIyyyUlMMTzwbOF80vYLbZhw00zJPt4



It is a dataset of a Portuguese bank’s marketing campaign which shows whether a person has responded positively by opening a bank account after the campaign or negatively by not responding at all.

Having had a peer-to-peer marketing experience and also having interest in the insurance and banking aspects of finance, I felt this to be an interesting dataset – not just for this project but also in general. Marketing and thinking better ways to market the bank and it’s product takes up a huge portion of time of a banker. With new-age working culture, marketing is being more and more ingrained with all other divisions, not just in banks but other industries too. After-all, without anybody buying your service or product or idea, the existence of any institution will have no meaning.  Often, marketing campaigns are designed keeping a pessimistic approach that upon launch- it is possible in 90% of the cases target audience would decline the offer, optimistic being 70%. 

And, any campaign creates a budget requirement on the company’s capital.

So, while it is important to assess the target or segment of the market thoroughly while designing and launching your campaigns, it is also important to assess afterwards. Maybe some factors are highlighted from the data which the management could have missed before as they didn’t have the results from a live experiment. 

Hence, this marketing dataset and similar datasets will provide ways to classify – ‘how likely’ will a customer respond positively to your campaign, based upon certain parameters of the customer. Well, I use this word  ‘how likely’ because prediction and reality are two different things. I might have a prediction and proceed likewise, but the outcome maybe opposite to my prediction. 

But still, in the world with millions of people and companies trying their level best to cater to global taste everyday, these predictions are helpful navigators as it saves our time and risk levels which could have incurred by swimming through the pool of global customer profiles without any idea.

About the dataset
This dataset has the following columns:
Data columns (total 17 columns): 
age 11162 non-null int64 
job 11162 non-null object 
marital 11162 non-null object 
education 11162 non-null object 
default 11162 non-null object 
balance 11162 non-null int64 
housing 11162 non-null object 
loan 11162 non-null object 
contact 11162 non-null object 
day 11162 non-null int64 
month 11162 non-null object 
duration 11162 non-null int64 
campaign 11162 non-null int64 
pdays 11162 non-null int64 
previous 11162 non-null int64 
poutcome 11162 non-null object 
deposit 11162 non-null object 
dtypes: int64(7), object(10)

This dataset can be treated valid for binary classification problem because, the target output has only two possible values: yes or no.

Here we have 16 dimensions and 1 target variable column of deposit.

#Preliminary Data Analysis
