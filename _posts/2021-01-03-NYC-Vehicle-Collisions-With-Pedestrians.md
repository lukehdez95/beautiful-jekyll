---
layout: post
title: New York City Car-Pedestrian Accidents
subtitle: NYC is known for its pedestrians not needing a car, but does that make the roads safe for them?
date: 2021-01-03
cover-img: 
thumbnail-img: 
share-img: 
tags: [NYC,Accidents,Motor Vehicles,Pedestrians]
---

I've been living in New York City (NYC) all of my life, and, despite having my driver's license, I have never owned a car.

Fortunately for me, one of the things that makes NYC great is the ability to maneuver around the city despite not having a car. Many of the people living in NYC utilize the city's extensive public transit system, or if they need to get somewhere *really* fast, they'd pay for a cab ride.

Despite the city being so friendly to those who choose to travel on foot, [car ownership continues to rise](https://nyc.streetsblog.org/2018/10/03/car-ownership-continues-to-rise-under-mayor-de-blasio/).

With all of these cars on the streets, and the nightmare that parking has become, I wanted to know just how safe the roads are for the pedestrians who continue to  travel without the use of motor vehicles. I wanted to see if I could find a pattern in the time of year and time of day these motor vehicle accidents were happening. 

[I found data with reported motor vehicles accidents in NYC for 2015-2017](https://www.kaggle.com/nypd/vehicle-collisions) this included data for the date, time and locations for when each incident occurred. It also included how many people were injured, and if they were pedestrians, as well as the type of vehicles involved in the accidents.

My original dataset comprised of all motor vehicle collisions which included ones that did not end with people being injured, as well as ones involving only motor vehicles and not pedestrians. I filtered the data to only include collisions that resulted in the injury or the death of pedestrians.

After this I made a feature where I was able to break down the time of day in which these accidents were occurring and graphed it to get the following:

![data_1](/assets/img/MVAccidentTOD.png)

I found to my surprise that despite having better visiblity than evenings, the afternoon time period (from noon to 6pm) had most of the pedestrian involved motor vehicle accidents. I believe that this is due to the sheer number of people who are out and about during this time period, whether it is to get lunch, or to commute from work.

I felt like it wasn't enough to just know when these accidents were happening, I also wanted to know where they were happening as well. So I graphed these occurrences by borough to shed some light on if there was some sort of pattern there:

![data_2](/assets/img/MVAccidentTODBoroughs.png)

I found again to my surprise that most of these collisions were occuring in Brooklyn and not Manhattan, which by the account of many native New Yorkers, is the borough that is most congested with vehicles. Unsurprisingly the smallest borough, Staten Island, has the least amount of accidents by a large margin.

The only time Manhattan actually had more accidents occur was in the morning time. This makes sense since the morning is when many people are commuting to work, and Manhattan is the borough which holds the majority of the employment opportunities for most New Yorkers.

The last thing I wanted to investigate is whether there was a time of year where motor vehicle accidents involving pedestrians occurred more frequently, and created the following graph:

![data_3](/assets/img/MVAccidentMOY.png)

I found that most of these accidents involving pedestrians happen during the fall and winter months. This makes sense, since during the fall and winter months, there are less hours of daylight in a day. This change in visibility may make it more difficult for a driver to notice a pedestrian walking in front of them.

There is much more than can be explored with this dataset such as fatality rates, or the types of cars commonly involved in these accidents. I would like to establish a pattern between the types of vehicles getting into accidents and specific times of the day. I would also like to compare the data year to year to see if the higher ownership of vehicles results in more accidents per year as well.

Fortunately for me; I do not live in the borough where many of these accidents are occuring. But, despite me living in the Bronx, I will continue to be cautious when commuting to and from work.
