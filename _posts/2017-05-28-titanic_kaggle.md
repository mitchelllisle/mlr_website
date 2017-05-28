---
layout: post
title: "Titanic Kaggle Challenge"
date: 2017-05-28
---

I've always been super interested in the [Kaggle](https://www.kaggle.com/c/titanic#tutorials) data challenges and have gone through a number of peoples submissions. It's great to see how people have tackled the problems and so I decided to write a blog post about the titanic competition, which is the beginners one.

I've broken it into three parts.

1. Exploratory Analysis
2. Clean up and Tidying
3. Survival Prediction

First off, I decided to join the train and test datasets together to have all variables together.

## Exploratory Analysis

```r
train <- read.csv("Downloads/titanic-train.csv")
test <- read.csv("Downloads/titanic-test.csv")

all <- bind_rows(test, train)

write.csv(all, "Downloads/all-titanic.csv"
```

The data looks a little something like this:
```
PassengerId Pclass                                         Name    Sex  Age SibSp Parch  Ticket    Fare Cabin Embarked Survived
1         892      3                             Kelly, Mr. James   male 34.5     0     0  330911  7.8292              Q       NA
2         893      3             Wilkes, Mrs. James (Ellen Needs) female 47.0     1     0  363272  7.0000              S       NA
3         894      2                    Myles, Mr. Thomas Francis   male 62.0     0     0  240276  9.6875              Q       NA
4         895      3                             Wirz, Mr. Albert   male 27.0     0     0  315154  8.6625              S       NA
5         896      3 Hirvonen, Mrs. Alexander (Helga E Lindqvist) female 22.0     1     1 3101298 12.2875              S       NA
6         897      3                   Svensson, Mr. Johan Cervin   male 14.0     0     0    7538  9.2250              S       NA
```

Variable Descriptions
```
Variable Name	Description
Survived = Survived (1) or died (0)
Pclass = Passenger’s class
Name = Passenger’s name
Sex = Passenger’s sex
Age = Passenger’s age
SibSp = Number of siblings/spouses aboard
Parch = Number of parents/children aboard
Ticket = Ticket number
Fare = Fare
Cabin =	Cabin
Embarked = Port of embarkation
```
### Titles

The first thing I decided to look at was the titles of those on board. Here are the results of this - nothing particularly telling, but you can see where most people got on the Titanic.

<iframe src="https://exploratory.io/viz/mitchelllisle/7762766613215181?cb=1495970816576&embed=true" width="100%" height="650px" frameborder="0"></iframe>

### Class
Did it make a difference if you paid more on the Titanic? Would you increase your chance of survival if you forked out money for the high class spots? Intuitively you would say that is the case, but when it comes to the Titanic this is not the case. Here you can see that `75% of 'Upper Class'` ticket holders did not survive, whereas `62% of 'Low Class'` ticket holders did. Overall there were a total of 491 people in the 'Upper Class' category, but only 216 in the 'Low Class' category. Perhaps being among more people in the Upper Class meant more people missed out. Obviously more analysis into the Titanic schematics might show you why this may have been the case, but for this dataset at least, it certainly didn't mean you had a higher chance of survival.

<iframe src="https://exploratory.io/viz/mitchelllisle/0674205113100465?cb=1495971751602&embed=true" width="100%" height="650px" frameborder="0"></iframe>

### Families TBC
....
