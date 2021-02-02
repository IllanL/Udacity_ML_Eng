# Starbucks Challenge - Capstone Proposal
### Table of Contents

2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Solution](#solution)
4. [Benchmark model](#benchmark)
5. [Metrics](#metrics)
6. [Project design](#project)



## Project Motivation<a name="motivation"></a>

I have selected the Starbucks project for this Udacity Machine Learning Capstone Project.

The project will evaluate the information provided within this dataset, as to determine whether the offers sent to their customer base have an impact on sales, and along the project we will try to perform customer segmentation and clustering, to increase the impact of the campaigns.




## File Descriptions <a name="files"></a>



The dataset comes from Starbucks simulated data.

The data is provided in three files:
- `portfolio.json` - contains offer ids and meta data about each offer (duration, type, etc.)
- `profile.json` - demographic data for each customer
- `transcript.json` - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable of each one of the files:

`portfolio.json`
- id (string) - offer id
- offer_type (string) - the type of offer ie BOGO, discount, informational
- difficulty (int) - the minimum required to spend to complete an offer
- reward (int) - the reward is given for completing an offer
- duration (int) - time for the offer to be open, in days
- channels (list of strings)

`profile.json`
- age (int) - age of the customer
- became_member_on (int) - the date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

`transcript.json`
- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since the start of the test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record


## Solution<a name="solution"></a>

Broadly speaking, we will try to assess the following question: Is there a way to categorize customers as to decide which customers send an offer to, in order to increase spending?

We will try to identify which customers don't need an offer to spend, which are highly sensitive to offers sent to them and finally, which customers respond negatively to any offer sent to them.



## Benchmark model<a name="benchmark"></a>

We will use the massive bombardment emailing method(i.e. sending emails to all users, considering all the same) as the benchmark model, as it seems to be the method currently being used.



## Metrics <a name="metrics"></a>

For the clustering, explained variance will be used as to determine which variables explain the most variance of our target variable.

For our segmentation, accuracy will be the variable used.

We would like to include a variation percentage in revenue as a metric, but as it is not possible, since we cannot evaluate the behavior of our model afterwards, we cannot include it.



## Project design <a name="project"></a>

The project will consist in the following phases:

1) Wrangling of data

2) Exploratory Data Analysis

3) Customer classification on high spenders, middle and low spenders, and susceptible to offers and not (creating our target variable)

4) Variable selection

5) Customer segmentation