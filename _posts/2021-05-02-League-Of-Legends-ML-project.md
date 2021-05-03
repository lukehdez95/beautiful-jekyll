---
layout: post
title: League of Legends
subtitle: The biggest E-Sport wordwide...what should I do to win?
date: 2021-05-02
cover-img: /assets/img/leagueoflegendstitle.jpg
thumbnail-img: /assets/img/League of Legends icon.jpg
share-img: 
tags: [League of Legends, MOBA, e-sports, gaming]
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/BGtROJeMPeE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

League of Legends is an online game known as a MOBA, or Multiplayer Online Battle Arena. A team of 5 players takes on another team of 5 players, in order to capture various objectives around the map known as Summoner's Rift. The ultimate objective? To destroy the opposing team's nexus before they destroy yours.

As of today, League of Legends continues to be the biggest e-sport in the world. In 2018, the [League of Legends World Championship brought in viewers rivalling that of the NFL SuperBowl](https://dotesports.com/league-of-legends/news/league-of-legends-vs-superbowl-viewer-numbers). 

I have played League of Legends for a couple of years now, and have somewhat of a love-hate relationship with the game. Why? Simply because I hate losing. What better way to improve my winrate than to look at the [data from over 50,000 ranked games](https://www.kaggle.com/datasnaek/league-of-legends) and use my Data Science knowledge to see if I could analyze what exactly are the things that leads to victory in a League of Legends game.

After reading in my data, I ran it through pandas profile inspector view some surface level data analysis with the data. 

I noticed that I had some duplicates that I had to deal with, no null values, and a couple ones with zero values but thats okay, in these cases those 0s just mean that no team captured those objectives.

After dealing with the duplicate rows, I established a baseline, where I found that about 50.6% of the time Team1 would win, and 49.4% of the time Team2 would win. Assuming the majority class would give me a baseline percentage of 50.6%, which allows me to use accuracy as my metric. (PIC)

I added 5 features, each tracking whether Team1 or Team2 had captured more of a particular objective than their opponent, with 1 being Team1, 2 being Team2, and 0 meaning that they both had captured the same number of that particular objective. These features were mostTowerKills, mostInhibitorKills, mostBaronKills, mostDragonKills, and mostRiftHeraldKills.

After that I made a Linear, Ridge Classifier model, which was able to correctly predict when a certain Team would win about 95% of the time. (PIC)

I made a Tree-based, Gradient Boosting Classifier model, which was able to correctly predict team victories about 97% of the time. (PIC)

Finally I made a XGBoost Classifier model, which was able to correctly predict team victories around 97% of the time as well. (PIC)

All 3 models showed me that the most important feature, *by a huge margin* was the team with the most tower kills. (Gradient Boosting Pictured)

This makes sense to me, the team with the most towers killed almost always wins. After all, a prerequisite to being able to take the nexus and claim victory is destroying a minimum of 5 towers, and an inhibitor.

I however was unsatisfied with this, I felt it was a foregone conclusion that a team with more objectives would almost always win. I now wanted to see if there was a correlation between who took the *first* objectives of each category.

After removing features save the 'first' features and putting them through a Gradient Boosting Classifier model, I found that I was only able to correctly predict a team's victory about 90% of the time. (PIC)

I found that the largest contributing factor to victories in this case was the team who was first to destroy an inhibitor. (PIC)

This also made sense to me, but again, destroying an inhibitor happens usually very late in a game. In order to destroy an inhibitor you must destroy a minimum of 3 towers. I want to be able to tell even earlier what objectives winning teams usually take, so I did this once again, but without the firstInhibitor feature. 

This time I saw that the firstBaron and firstTower were largely correlated with victory as well, however I could only correctly predict the victor around 81% of the time.


