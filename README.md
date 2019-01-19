# Starbucks Promotions
Optimizing Starbucks promotion strategy.

## Intro


## Installation
### Libraries
I've mainly used standard Python libraries throughout the project. However, as I did face issues upgrading to the latest version of scikit-learn with Anaconda, I've decided to list the __most important packages__ and corresponding version numbers used:
- ```python 3.6.7```
- ```pandas 0.23.4```
- ```numpy 1.15.4```
- ```scikit-learn 0.20.2```
- ```xgboost 0.81```
For all plotting purposes I've used ```matplotlib``` & ```seaborn```.

### Data
The data sets being used consist of __simulated data from Starbucks__ that mimics customer behaviour on the Starbucks rewards mobile app, including transactions and offer response. While some users receive an offer once every few days on the mobile app, users might not receive any offer during certain weeks. An offer can be anything from a drink advertisement to an actual discount or buy-one-get-one-free. It was was provided in [Udacity's Data Scientist Nanodegree Program](https://eu.udacity.com/course/data-scientist-nanodegree--nd025).

## Motivation

## Files
The __data__ used throughout this project is contained in three files: ```portfolio.json```, ```profile.json``` & ```transcript.json```. Despite that, you find all __coding work__ in the jupyter notebook ```starbucks_capstone.ipynb```in the main folder of this repository. Please use the following file tree for further orientation.
```
- data
|- portfolio.json             # Offer portfolio meta data
|- profile.json               # Starbucks app user demographic data
|- transcript.json            # Offer events and trasaction data

- starbucks_capstone.ipynb    # Project notebook
- xgb_regressor.pkl           # Trained regression model
```

### Column Descriptions
Please refer to the following __list__ for a description of variables.

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
- event (str)                # record description (ie transaction, offer received, offer viewed, etc.)
- person (str)               # customer id
- time (int)                 # time in hours (the data begins at time t=0)
- value (dict of strings)    # either an offer id or transaction amount depending on the record
```

## Findings

## Acknowledgements
I'd really like to thank __Starbucks__ for providing the data to this project. Please be aware that this data set was provided in [Udacity's Data Scientist Nanodegree Program](https://eu.udacity.com/course/data-scientist-nanodegree--nd025) so it may not be free for everyone to use.
