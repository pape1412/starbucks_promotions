# Starbucks Promotions
Optimizing Starbucks promotion strategy.

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
One of Starbucks' goals behind sending out offers is to __increase the response__ of its app users. On the one hand, response can refer to the frequency of transactions and on the other to amounts spent. However, if and how users respond, depends on the __types of offers__ being sent as well as user specific (socio-)__demographic characteristics__. In fact, not getting the fit between the two right can have a significant effect on Starbucks financial performance.

The goal of this project is to __optimize Starbucks' promotion strategy__, whereas the focus lies on maximizing __transaction profits__ per user. In order to do so, I'm going to explore __two different approaches__ of finding the right types of offers for each individual Starbucks app user. The first one is an __alytical solution__ to the problem - simple yet effective - that extracts the optimal combination of offer types including expected transaction profits for different demographic groups. The second one involves __linear and tree-based regression models__ as well as simulations of monetary response for each app user and possible offer type combinations. In the end, both solutions will have to prove their validity against a __benchmark__ of Starbucks current offer response.

## Files
The __data__ used throughout this project is contained in three files: ```portfolio.json```, ```profile.json``` & ```transcript.json```. Despite that, you find all __coding work__ in the jupyter notebook ```starbucks_capstone.ipynb```in the main folder of this repository. Please use the following file tree for further orientation.
```
- data
|- portfolio.json            # Offer portfolio meta data
|- profile.json              # Starbucks app user demographic data
|- transcript.json           # Offer events and trasaction data

- starbucks_capstone.ipynb   # Project notebook
- xgb_regressor.pkl          # Trained regression model
```

### Column Descriptions
#### Portfolio.json
```
- id (string)                # offer id
- offer_type (string)        # type of offer i.e. BOGO, discount, informational
- difficulty (int)           # minimum required spend to complete an offer
- reward (int)               # reward given for completing an offer
- duration (int)             # validity period of offer in days
- channels (list of strings) # communication channels via which offer was sent to user
```
#### Profile.json
```
- age (int)                  # age of the customer
- became_member_on (int)     # date when customer created an app account
- gender (str)               # gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str)                   # customer id
- income (float)             # customer's income
```
#### Transcript.json
```
- event (str)                # record description (ie transaction, offer received, offer viewed, etc.)
- person (str)               # customer id
- time (int)                 # time in hours (the data begins at time t=0)
- value (dict of strings)    # either an offer id or transaction amount depending on the record
```

## Findings

## Acknowledgements
I'd really like to thank __Starbucks__ for providing the data to this project. Please be aware that this data set was provided in [Udacity's Data Scientist Nanodegree Program](https://eu.udacity.com/course/data-scientist-nanodegree--nd025) so it may not be free for everyone to use.
