### Welcome to the Women's world cup 2023 Analysis

My name is Monica. I'm a data nerd and washed up soccer player who can still
claim a couple of D3 records to her name. Of course with the world cup I wanted
to jump in and get my hands dirty.

How did I get here? I work for Starburst as a Developer Advocate and I'm always
on the prowl for fun creative datasets to create example projects from. I'm
much more motivated when the data is something interesting, and with the
upcoming webinars I had, I thought why not do a demo involving women's world cup data.
I then found Gustavo's analysis, and figured I'd do my part
here to support women's sports - I can do my part and analyze the women's data
and popularize the tournament just a little bit more. #EqualityinSport

Instead of just doing a demo for Starburst, I decided to push myself out of my comfort
zone and try predictive analysis for the women's world cup. One small
step for women's equality, one giant leap for Monica.

A big thank you and major credit towards [Gustavo
Santos](https://gustavorsantos.medium.com/predicting-results-and-goals-with-machine-learning-599e99d6e3e0)
who's project on the men's world cup I then recreated for the women. You can
view
his initial work (here)[https://github.com/gurezende/World_Cup_2022/blob/main/Results/FIFA_WorldCup2022.png].



### Monica vs the Machine

I plan to write a four part article series around this - The Introduction, The
Data Wrangling, The Analysis, and The Result. Here's the TLDR for each one.


## The Introduction

Basically everything you read above, with the added thank you to my favorite
collaborator [@emiller](https://github.com/Emiller88) who was an awesome rubber duck to pair program with.

## The Data Wrangling

Every project starts with the data wrangling. I found this [Kaggle
dataset](https://www.kaggle.com/datasets/martj42/womens-international-football-results?select=results.csv),
then did some data cleaning to only take into account data from the last 20
years. I also filtered the data to only consider countries that were in the
world cup. The data was not fully up to date, so I updated the data from any
international matches including these teams within the last year.

## The Analysis

I used the CatBoost algorithm for my predictive analysis. The [train model
notebook](https://github.com/monimiller/womens_wc_23/blob/main/notebooks/train_model.ipynb)
is where I ran the analysis to create my model.  Much of this was me simplifying
Gustavo's previous work and tailoring it to my needs. I also weighted every
match equally, so instead of the home team being weighted differently than the
away team, those outcomes were statistically equally probable.

My [run predictions
notebook](https://github.com/monimiller/womens_wc_23/blob/main/notebooks/run_predictions.ipynb)
is where I then used the trained model to produce probabilities for all the
results. These results can be found in the [model generated predictions
folder](https://github.com/monimiller/womens_wc_23/tree/main/model%20generated%20predictions).

Based on the group play predictions, I then ran through all the playoff games
and built out the full bracket. 

## The Result

Just like I make most decisions, all my predictions were based on my gut. I
didn't really do as much research as I would have liked, and really just solely
put all my biases out there. You can find my predictions in the [Monica's
predictions
folder](https://github.com/monimiller/womens_wc_23/tree/main/Monica's%20predictions).
I have all my group winners, and then also have published my personal bracket. I
will check back throughout the tournament to see who's winning - Me or the
Algorithm.
