# Probability of becoming an Instagram influencer
Building AI course project

## Summary
This application allows the user to enter various characteristics describing a person and then estimates the probability of that person becoming an influencer. The characteristics are predefined and some require the input to be a number within a specified range (e.g. age), while others have multiple choices. 

## Background
Per definition, social problems influence many people. But how many get the opportunity to influence the social problems they are enduring? By using this application and trying different combinations of characteristics, the user can explore how different attributes affect the result. Does everyone truly have the same chance of getting their voice heard and to make a change?

To be honest, my idea does not solve any problems on its own. However, my aspiration is to provide a tool for evaluating diversity and to raise awareness of the status quo. I know that this does not give the whole picture, but we need to start somewhere, right? 

The intention is not to put the blame on any single person or group and I am not at all criticizing the current influencers. In fact, I think many of them are doing a great job and that is exactly why I want to make sure that everyone gets the same opportunity to do the same. It was not until recently that I realized how brilliant the concept of being a so-called "influencer" actually is. 

## How is it used?
Truth be told, this is indeed a sensitive subject — and rightly so. Nevertheless, it is an important one and everyone should be able to access the obtained results without any censorship. Thus, I aim for this application to eventually become publicly available. Note that the intentions as well as the limitations will be explicitly stated.  

This application is absolutely not designed to predict the probability for any single individual, instead the purpose is to get an overview of how characteristics and combinations of them affect whether others will listen. 

The objective is not to offend anyone or to tell them that it is not even worth trying to influence their surroundings. To everyone who is reading this: no numbers can ever define you! If you want to, be the exception to the "rule(s)"!

## Data and AI techniques
The following characteristics are included in the prototype:
* Age (18-65) 
* Sex (male/female) 
For the sake of simplicity, the imaginary data set in the prototype only includes individuals who use Instagram. Explanation for why the categorical variable has no more than two alternatives, can be found in the section "Challenges". Given more data, more variables as well as options will become available (e.g. religion, race, sexual orientation, weight, social media platform(s), gender). 

The principal problem is to collect reliable data from a large number of individuals, without any ethical violations. After all, this application relies on personal data. Preferably, research would be conducted solely for the purpose of this application and data would be gathered through surveys or interviews. A research ethics committee would review the process and the data would be anonymized.

From my point of view, this kind of problem (i.e. probabilistic prediction in binary classification) is best solved within the field of machine learning. 

For the time being, I have decided to use logistic regression. As regards this (theoretical) dataset, I am afraid that the assumption of linearity (made when applying logistic regression) is incorrect. Given sufficient data, the optimal approach would be to use neural networks. 

Like I mentioned before: the users should be able to explore the results — from every conceivable angle. Thus, I think interactive data visualization would be a favorable approach. For instance, the user could enter characteristics for a number of persons (or choose random generation) and the application would not only show the probability of them becoming an influencer, but also group them accordingly and show common/unique characteristics for each group. By altering the characteristics for one person, the user can check whether that person switches from one group to another (i.e. increased/decreased probability).

## Creation of application
* Data collection
* Read CSV file into Pandas DataFrame
* Transform categorical variables into dummy variables 
* Split the data to allow cross-validation (done with scikit-learn) 
* Build logistic regression model
* Evaluate the model
* Present the results

## Prototype
To access an interactive version of the code, click on the binder badge: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/the-exceptional-exception/probability-of-becoming-an-influencer/HEAD)

Or you can always look [here!](prototype.ipynb)

## Challenges
In its current state, this application should not be trusted at all and frankly, no application will ever be able to tell in advance what any person will achieve or not. However, the day might come when this application will be able to identify which characteristics that tend to be subject to bias. 

Currently identified limitations:
* Relies on personal data => ethical issues.
* High risk of overfitting given scarce data => requires many participants and/or only a limited number of variables can be included and the options for the categorical ones must be few.
* The assumption of linearity may not hold => non-linear models may be required (very likely).
*  Some might find the results (or the whole idea) offensive.
* When is a person considered to be an influencer? Are there some criterion/criteria that need to be met (e.g. minimum number of followers)?
* As a rule, one must try to become an influencer in order to actually become one. Should a variable like "goal commitment" be included? In the prototype, I only included people having Instagram. However, more factors have influence...
* When evaluating diversity, is it correct to use percentages (i.e. also include non-influencers) or is it best to only look at the distribution of characteristics among influencers? Is it more important that everyone has the same probability of becoming an influencer or that all characteristics are represented among influencers? After all, some characteristics and especially combinations of them are rather uncommon compared to others. I would say that it is a balancing act.

## What next? 
If you have read this far, you know that there is indeed a long way to go for this idea to become reality. Realistically speaking, improvements can always be made and the data would need to be regularly updated. 

The question I have not yet answered is this: Why did I choose "influencers" and not "people in a position of power"? As a matter of fact, being in a position of power is not necessarily equivalent to having the ability to influence and maybe even inspire others. 

At the same time, I would love to get the distribution of characteristics for many positions in society. Importantly, I want people to reflect if certain characteristics (e.g. gender, religion, race) GENUINELY predetermine whether the person has spectacular ideas that might change the world. In an ideal world, everyone would have the same amount of power and influence. Since that is not how it works, we should at least aim for diversity. 

## Acknowledgments
I would like to thank everyone who has taught me that life should be more than surviving and to effectively combat social problems, we need to include everyone.
