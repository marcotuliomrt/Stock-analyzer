# Stock-analyzer
Profitability analyzer based on financial indicators


## Introduction

Decisions about stock trading are fundamentally associated with estimating the intrinsic value that the company will have in a given period. This project is based on the hypothesis that it is possible to extract relevant information to carry out these estimates of companies' financial indicators.

The value behind a classifier like this is the standardization of the good investment selection process.



## Goal

This project aims to carry out a systematic analysis of the financial indicators of a given stock and answer the following question: In a period of one month, will a given stock increase in value or not?

Initially, the application of this model was designed to manage a portfolio of shares whose purchase and sale operations were carried out every month, so the test would be performed for all shares in the portfolio and for any shares that aroused interest in the acquisition. In the case of portfolio shares, the positive result for appreciation would result in the decision to keep it, otherwise it would be sold.



## Technique used

The technique used in this project was the classification of financial indicators by four methods, Multinominal Logistic Regression, Random Forest, Gradient Boosting and a combination of the three previous ones in parallel.
Why analyze the behavior of financial indicators and not just stock prices?

The behavior of stock prices, as well as that of any other financial asset (real estate, currency, bonds, etc.), is characterized by relatively high volatility as it is influenced by many factors of different natures, such as global financial stability, level of market apprehension financial, behavioral factors of specific individuals (such as state leaders), natural disasters, among others. Therefore, purely stock price analysis can generate promising results for a while, but the trend is that its accuracy is naturally reduced as the Training Database is filled with data from periods influenced by the factors of various natures mentioned above .

The analysis of indicators is more grounded, complete and faithful in understanding the company's behavior over time. For example, some indicators show how often shareholders are paid, the profitability for each share of that company (as opposed to profitability only), or even the quality of the investments that that company makes in itself.

These indicators can be translated, for example: in how reliable the company is to pay its shareholders, how efficient it is in generating profit and how capable it is to make good investments with the shareholders' money. As such, they represent much more versatile information to interpret and combine with other statistics, compared to just the share price.


### Multinomial Logistics Regression

Logistic Regression works based on the Maximum Probability (MLE) method, in which the parameters of the function are maximized so that it represents as much of the training data as possible. In the context of analyzing financial indicators, the idea is to relate them to the 'target' variable, a binary that represents whether the stock appreciated or devalued in a given month.
Random Forest

### Random Forest
Random Forest is a classification method that is based on another more fundamental classification model, the decision tree. The differential of Random Forest is that it creates numerous decision trees by reorganizing the classification criteria, it exchanges the data from the training DataSet and creates new ones with these values, and for each it creates a decision tree with particular criteria of each new DataSet .
Gradient Boosting

### Gradient boosting 
Like Random Forest, this method is based on a simple and weak model, which, when going through a process of numerous permutations, repetitions and adaptations of the structure itself, becomes very efficient, analyzing the classification errors in the training data. This base model is even simpler than decision trees and is known as 'Stump', which is basically a decision tree with just one branch and 2 leaves.



## Database Description

The database used in this project is composed of financial indicators collected over 34 years (1986-2020) from the Microsoft company. Your file was collected from the Bloomberg Professional Services financial database

Indicators collected quarterly

- NET_INCOME: The difference between the company's gross profit and expenses. (in 106 dollars)
- CF_FREE_CASH_FLOW: Company money that is available to be distributed to shareholders.
- CF_CASH_FROM_OPER: Cash flow generated by the company from its regular activities.
- CF_CASH_FROM_INV_ACT: Cash flow invested by the company.
- CF_CASH_FROM_FNC_ACT: Debits flow, for example: Profit generated by a loan - loan amount.
- CUR_RATIO: Liquidity of company assets, the ease with which the company can turn its assets into cash.
- TOT_DEBT_TO_COM_EQY: Ratio between the company's debt and equity.
- RETURN_COM_EQY: Ratio between company profits and shareholders' money.


indicators collected daily

- CUR_MKT_CAP : Market value, value of one share times the total number of shares.
- TURNOVER : Indicates how quickly the company is able to raise money from its inventory.
- PX_LAST: Share Price .
- EQY_SH_OUT : Number of shares held by shareholders.
- PE_RATIO : Ratio between the total value of the shares and the company's profit.
- PX_TO_BOOK_RATIO : Ratio between the price of a share and the company's sales price per share.
- EQY_DPS: Ratio between money paid to shareholders and number of shares.


