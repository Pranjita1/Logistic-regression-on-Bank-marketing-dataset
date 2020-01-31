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

Preliminary Data Analysis

1st we check for null values.

Next, we check mean, quartiles, median and mode. From mode we see that majority answer is "NO", which hints that something was wrong with the campaign. We try to find out what?

Next, we plot charts with each of our dimension parameters vs the target feature we would like to predict.

1. Age vs Deposit - we see that majority age group lied between 25 to 60, with peaks in range 30 to 36. From the catplot, we see that the majority who opened a deposit account belonged to lower age below 60, while majority who said 'NO' belonged to upper age.

2. Deposit vs job - From this countplot we see that most people in blue-collar jobs responded negatively to the campaign. However, more proportion of students, retired, management and unemployed said Yes than No. This can be indicative of two things - 

a) retired includes people who have taken early retirement.
b) this deposit scheme suits those who are either not financially secure or dependent or in professions where thare is no financial stability.

But, surprisingly, the groups whose response were YES were not the majority contacted by the bank.

3. Comapred to marital status - we find higher proportion of singles responding in YES while higher proportion of married people responded in No. Also, looking at the divorced column, we find Yes and No in almost near equal proportion to each other. This can be indicative of the fact that - if a person is married, perhaps he / she is financially secured by the other spouse, else, they find this scheme beneficial to support themselves financially. But, the number contacted more by the bank were married people.

4. Comparing to education - people with tertiary education favoured this scheme, while people with primary and secondary education didn't quite comply to the campaign. It maybe due to:

a) Majority with tertiary education are either: students / managers / trying to find a job which suits their qualification / retired
b) Most people with secondary and primary education contacted by the bank are into blue collar jobs

5. From assesing loans and defaults columns aanist deposit, we find that the bank seems to have contacted majorly those people who didn't have loans or who aren't defaulters. In either case, the response was a higher proportion of "NO" compared to YES.

6. It seems that almost equal propportion of people with or without housing were contacted by the bank. And again, people without housing preferred the deposit scheme more compared to those with housing.

7. It seems that cellular and digital mode of commuincation is the most preferred mode of contact for customers.

8. From months, we find a pattern - most contacts made during the months of September, October, December, February, March, April resulted in successful campaign result because an account was opened. However, the Bank made most of it's calls during May when mostly the outcome was a 'NO' perhaps because it May is usually time for Summer break and people were either traveling or relaxing or just not in mood for banks.

9. From comparing days to deposit we see that while the distribution is mostly evenly spread, the proportion of YES for calls made on the 30th of the month is higher while the proportion of NOs is higher is for the calls made during the middle of the month.

10. Comaparing duration with the outcome of deposit showws that in cases of YES, the highest duration of a call was a little less than 4000 minutes, while for NOs, the maximum call duration was for 3250 minutes. The median duration of YES is higher than NO and from this, we can infer that - perhaps the marketing personnel had to do a lot of convincing talks for people to open up a deposit account. This might indicate that perhaps either the features in the deposit account were not that good, so it needed some selling effort. Or perhaps the features were not well presented in the marketing manuals created for the campaign.

From the above, we can infer that - The Bank were not able to segment their potential customer group properly in terms of who would be appealed the most by the benefits of their products. Otherwise, the campaign would have been a huge success.

Refer to the notebook for code.

After this analysis, a Logistic regression model tells us that given the present situation, if a new person is considered with characteristics under the dimensions of this study, if or not he or she will open a bank account.
