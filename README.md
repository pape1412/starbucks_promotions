# Starbucks Promotions
Optimizing Starbucks promotion strategy.

## Intro


## Installation
### Libraries
I've mainly used standard Python libraries throughout the project. However, as I did face issues upgrading to the latest version of scikit-learn with Anaconda, I've decided to list the most important packages and corresponding version numbers used:
- ```python 3.6.7```
- ```pandas 0.23.4```
- ```numpy 1.15.4```
- ```scikit-learn 0.20.2```
- ```xgboost 0.81```

For all plotting purposes I've used ```matplotlib``` & ```seaborn```.

### Data
The data sets being used consist of simulated data from Starbucks and was provided in Udacity's Data Scientist Nanodegree Program. Please see "Files" section for further information.

## Motivation

## Files
```
- data
|- portfolio.json             # Offer portfolio meta data
|- profile.json               # Starbucks app user demographic data
|- transcript.json            # Offer events and trasaction data

- starbucks_capstone.ipynb    # Project notebook
- xgb_regressor.pkl           # Trained regression model
```
The data used throughout this project is contained in three files:
- ```portfolio.json```
- ```profile.json```
- ```transcript.json```

### Column Descriptions
Please refer to the following overview for a description of variables.

### Portfolio.json
```
- id (string)                # offer id
- offer_type (string)        # type of offer i.e. BOGO, discount, informational
- difficulty (int)           # minimum required spend to complete an offer
- reward (int)               # reward given for completing an offer
- duration (int)             # validity period of offer in days
- channels (list of strings) # communication channels via which offer was sent to user
```
### Profile.json
```
- age (int)                  # age of the customer
- became_member_on (int)     # date when customer created an app account
- gender (str)               # gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str)                   # customer id
- income (float)             # customer's income
```
### Transcript.json
```
event (str)                  # record description (ie transaction, offer received, offer viewed, etc.)
person (str)                 # customer id
time (int)                   # time in hours (the data begins at time t=0)
value (dict of strings)      # either an offer id or transaction amount depending on the record
```

## Findings

## Acknowledgements
I'd really like to thank Starbucks for providing the data to this project. Please be aware that this data set was provided in Udacity's Data Scientist Nanodegree Program so it may not be free for everyone to use.
